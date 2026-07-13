---
title: Ausführen einer Cross-Channel-Kampagnenüberprüfung
description: Verwenden Sie das CX Enterprise MCP in einer einzigen KI-Sitzung, um eine einheitliche Ansicht des AJO-, CJA- und Real-Time CDP-Kampagnenzustands für Journey, Zielgruppen und Leistung zu erhalten.
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: 937a3189965f3a3551c730bb27ee0592ae6fca92
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 5%

---


# Ausführen einer Cross-Channel-Kampagnenüberprüfung

<!-- last-modified: 2026-05-21 -->

![Führen Sie eine kanalübergreifende Kampagnenüberprüfung durch](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review){zoomable="yes"}

*Zum Zoomen auswählen.*

Ein vollständiges Bild des Kampagnenzustands erfordert Daten aus mehreren Systemen: aktive Journey aus AJO, den Status der Zielgruppenaktivierung aus Real-Time CDP und Leistungsmetriken aus CJA. In dieser exemplarischen Vorgehensweise wird gezeigt, wie alle drei Komponenten in einer einzigen KI-Sitzung verbunden werden. So können Sie statt mit drei separaten Tools in einem Gespräch vom Journey-Status zum Zustand der Zielgruppe zu Leistungstrends wechseln.

| Szenario-Details | |
| --- | --- |
| CX Enterprise-Anwendungen | [Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/ajo-home), [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), [Real-Time CDP](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/home) |
| Agent-Tools | [CX Enterprise MCP](../tools/mcp-servers.md#cx-enterprise-mcp-servers) |
| Zielgruppe | Kampagnen-Manager, Marketing-Vorgänge |
| Voraussetzung | MCP-kompatibler KI-Client, Zugriff auf AJO, CJA und Real-Time CDP |

Jeder Schritt zeigt eine repräsentative Eingabeaufforderung und eine Beispiel-KI-Antwort. Ein **Mehr können Sie erreichen** Abschnitt folgt für weitere Untersuchungen in derselben Sitzung.

## Voraussetzungen

>[!BEGINTABS]

>[!TAB Claude.ai]

Verbinden des CX Enterprise MCP als benutzerdefinierter Connector. Über eine Verbindung erhalten Sie Zugriff auf AJO-, CJA- und Real-Time CDP-Tools.

1. Gehen Sie **Claude.ai zu Einstellungen** Integrationen.
2. Wählen Sie **Benutzerdefinierten Connector hinzufügen** und geben Sie die Server-URL ein: `https://cx-enterprise.adobe.io/mcp`
3. Wählen Sie **Verbinden** aus und melden Sie sich mit Ihrer Adobe ID an.

Vollständiges Setup: [Claude.ai Custom Connectors-Dokumentation](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Verbinden Sie den CX Enterprise MCP mit dem ChatGPT-Entwicklermodus (Pro-, Plus-, Business-, Enterprise- oder Education-Plan erforderlich).

1. Aktivieren Sie **Entwicklermodus** in **ChatGPT-Einstellungen**.
2. Navigieren Sie zu **Einstellungen > Integrationen** und wählen Sie **Benutzerdefinierten Connector hinzufügen > Remote-MCP-Server**.
3. Server-URL eingeben: `https://cx-enterprise.adobe.io/mcp`
4. Wählen Sie **Verbinden** aus und melden Sie sich mit Ihrer Adobe ID an.

Vollständiges Setup: [ChatGPT MCP-Dokumentation](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Andere KI-Clients]

Verwenden Sie Gemini, Microsoft Copilot, Cursor, Claude Code oder eine andere MCP-kompatible Umgebung? Stellen Sie mithilfe dieses Endpunkts eine Verbindung zum CX Enterprise MCP her:

```
https://cx-enterprise.adobe.io/mcp
```

Vollständige Setup-Anweisungen für alle unterstützten Clients: [Verbinden mit Ihrem KI-Client](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Melden Sie sich bei Ihrer Adobe ID an, wenn Sie dazu aufgefordert werden, und wählen Sie die IMS-Organisation aus, die mit Ihren AJO-, CJA- und Real-Time CDP-Umgebungen verknüpft ist. Die Wahl der falschen Organisation ist die häufigste Ursache für Authentifizierungsfehler.
>
>Bei der ersten Verbindung kann Ihr KI-Client Sie auffordern, eine IMS-Organisation auszuwählen oder eine Sandbox anzugeben. Sobald dieser Kontext festgelegt ist, verwendet ihn der MCP-Server für den Rest der Sitzung.
>
>Einige Tools fordern Sie vor der Ausführung zur Genehmigung auf. Überprüfen Sie die Anfrage und genehmigen oder ablehnen Sie. Ohne Ihre Bestätigung wird keine Aktion durchgeführt.

## Schritt 1: Überprüfen der aktiven Journey und Kampagnen

Beginnen Sie mit AJO, um festzustellen, was derzeit ausgeführt wird. Zu wissen, welche Journey live sind und vor kurzem geändert wurden, bildet die Grundlage für die weitere Überprüfung.

```
What journeys are currently active in AJO?
```

+++Siehe eine Beispielantwort

In Ihrer AJO-Organisation wurden 8 aktive Journey gefunden:

| Journey | Kanal/Kanäle | Last modified |
| --- | --- | --- |
| Begrüßungsreihe: Neue Mitglieder | E-Mail, Push | &#x200B;18. Mai 2026 |
| Follow-up nach dem Kauf | E-Mail, SMS | &#x200B;14. Mai 2026 |
| Erneute Interaktion mit den Treueprogrammen | E-Mail | &#x200B;20. Mai 2026 |
| Transaktionsabbruch: 24 Stunden | E-Mail, SMS | &#x200B;10. Mai 2026 |
| Frühjahrsaktion | E-Mail, Push | &#x200B;19. Mai 2026 |
| Win-back: 90 Tage inaktiv | E-Mail | &#x200B;28. April 2026 |
| Geburtstagsgeld | E-Mail | &#x200B;15. April 2026 |
| Rückgewinnung: Push-Opt-out | SMS | &#x200B;12. Mai 2026 |

3 Journey wurden in den letzten 7 Tagen geändert. Möchten Sie Einzelheiten zu diesen?

+++


## Schritt 2: Überprüfen des Zielgruppen-Aktivierungsstatus

Stellen Sie im Hinblick auf die Journey sicher, dass die Zielgruppen, die diese Kampagnen unterstützen, korrekt zu ihren Zielen fließen.

```
Show me the activation status for the high-value loyalty segment.
```

+++Siehe eine Beispielantwort

**Hochwertiges Treuesegment**: Aktivierungsstatus für alle Ziele:

| Ziel | Status | Letzter erfolgreicher Durchgang | Zielgruppengröße |
| --- | --- | --- | --- |
| Google Ads | Aktiv | &#x200B;21. Mai 2026 :14:02 Uhr | 48,320 |
| Meta Ads | Aktiv | &#x200B;21. Mai :58 01 Uhr | 48,295 |
| Salesforce Marketing Cloud | Aktiv | &#x200B;20. Mai 2026 11:30 PM | 47,940 |
| Adobe Target | Aktiv | &#x200B;21. Mai 2026 :00:00 Uhr | 48,320 |

Keine Datenflussfehler erkannt. Alle Aktivierungen wurden innerhalb der letzten 3 Stunden abgeschlossen.

+++


## Schritt 3: Abrufen von Leistungsmetriken aus CJA

Wenn der Journey- und Zielgruppenkontext etabliert ist, verwenden Sie CJA , um zu bewerten, wie diese Kampagnen konvertieren und wo die Interaktion abbricht.

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++Siehe eine Beispielantwort

**Kampagne zur Rückgewinnung aus dem Treueprogramm**: 21. April bis 21. Mai 2026:

| Kanal | Sendungen | CTR | Konversionen | Konv. Rate |
| --- | --- | --- | --- | --- |
| E-Mail | 48,320 | 8.4% | 1,973 | 4.1% |
| Push-Benachrichtigung | 31,200 | 12.1% | 987 | 3.2% |

Kombinierte Konversionsrate: 3,8 %. E-Mail-CTR ist um 1,2 % höher als im Zeitraum vor 30 Tagen. Push-Konversionen sind flach.

+++


## Schritt 4: Zusammenfassen einer Kampagnenzustandszusammenfassung

Bitten Sie Ihren KI-Client, das Bild über alle drei Quellen hinweg zusammenzuführen und alles aufzudecken, was Aufmerksamkeit erfordert.

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++Siehe eine Beispielantwort

Hier finden Sie die aktuelle Zusammenfassung des Kampagnenzustands in AJO, Real-Time CDP und CJA:

**Aktive Journey:** 8 live, 3 diese Woche geändert. Die Journey zur Rückgewinnung aus dem Treueprogramm ist die neueste Aktualisierung.

**Zielgruppenaktivierung:** Alle Segmente fließen korrekt zu 4 Zielen. Keine Datenflussfehler erkannt.

**Leistung:** E-Mail-CTR ist für alle Treuekampagnen aktiviert. Push-Konvertierung ist flach. Keine Kanäle weisen einen signifikanten Rückgang auf.

**Fahnen zur Aufmerksamkeit:**

- Win-Back-Journey (90 Tage inaktiv) wurde zuletzt vor 23 Tagen geändert und vor Kurzem nicht geprüft.
- Die Push-Konversionsrate war in drei aufeinander folgenden Zeiträumen gleich, was eine Überprüfung der Nachrichten oder des Timings lohnt.

Keine kritischen Probleme erkannt. Zwei der oben genannten Punkte erfordern eine Überprüfung vor dem nächsten Kampagnenstart.

+++


Hier zahlt sich der Multi-Server-Ansatz aus: Ihre KI-Client-Gründe für Journey-Konfiguration, Zielgruppenstatus und Leistungsdaten in einem einzigen Gespräch.

## Schritt 5: Ergreifen Sie Maßnahmen bezüglich Ihrer gefundenen Inhalte.

Die Überprüfung zeigte zwei Punkte. Bitten Sie Ihren KI-Client, Ihnen bei der Priorisierung und Route jedes einzelnen zu helfen.

```
For each flag you identified, what should I do and where should I go to do it?
```

+++Siehe eine Beispielantwort

Im Folgenden finden Sie einen nach Prioritäten gestaffelten Aktionsplan für die beiden Flaggen:

**1. Win-Back-Journey - Überprüfung der Bedingungen für den erneuten Eintritt (AJO MCP, dann AJO-Anwendung, falls erforderlich)**

Die Win-Back-Journey wurde in 23 Tagen nicht geändert. Bitten Sie mich, die aktuellen Wiedereintrittsbedingungen zu durchlaufen und die Logik zu verlassen. Wenn die Bedingungen veraltet oder falsch aussehen, erfordern strukturelle Änderungen am Journey-Fluss das Öffnen von AJO. Die Häufigkeitsbegrenzung und Zielgruppenaktualisierungen können hier vorgenommen werden.

**2. Flache Push-Konvertierung für 3 Zeiträume - Aktualisieren von Nachrichten oder Testen einer Variante**

Eine flache Konvertierung signalisiert in der Regel Nachrichtenermüdung oder eine Diskrepanz zwischen dem Angebot und der Zielgruppe. Zwei Pfade:

- **Push-Inhalt jetzt aktualisieren (AEM MCP):** Wenn Push-Benachrichtigungen mit einer Landingpage verknüpft sind, fügen Sie den AEM Content MCP-Server hinzu und aktualisieren Sie die Seitenkopie oder CTA, ohne die Tools zu wechseln.
- **Push-A/B-Test durchführen (AJO-Anwendung):** Erstellen Sie eine Variante auf Kampagnenebene mit unterschiedlichen Nachrichten, um zu isolieren, ob es sich um Inhalte oder Zielgruppen handelt. Dazu müssen Sie direkt zu AJO gehen.

Womit möchten Sie beginnen?

+++


## Was Sie erreicht haben

Sie haben eine kanalübergreifende Konsistenzprüfung der Kampagne durchgeführt, indem Sie AJO, Real-Time CDP und CJA mit einer einzigen KI-Sitzung verbunden haben. Anstatt drei Anwendungen zu öffnen und manuell ein Bild zusammenzustellen, haben Sie sich in einem Gespräch durch den Journey-Status, die Zielgruppenaktivierung und die Leistungsdaten bewegt. Die zusammengesetzte Zusammenfassung bietet Kampagnen-Managern einen schnelleren Weg zu ermitteln, was funktioniert, was angepasst werden muss und worauf sie sich als Nächstes konzentrieren müssen.

## Mehr können Sie erreichen

Wenn AJO, CJA und Real-Time CDP in derselben Sitzung verbunden sind, können Sie die exemplarische Vorgehensweise deutlich übertreffen. Erweitern Sie ein unten stehendes Szenario, um Eingabeaufforderungen anzuzeigen, die Sie ausprobieren können.

+++Erfahren Sie genau, was läuft, bevor Sie etwas Neues starten

Überlappende Journey, kürzlich geänderte Kampagnen und nicht überprüfte Kanäle können sich auf einen neuen Launch auswirken. Diese Eingabeaufforderungen geben Ihnen ein klares Bild des aktuellen Status, bevor Sie etwas hinzufügen.

**Eingabeaufforderungen**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++Stellen Sie sicher, dass die Zielgruppen die richtigen Ziele erreichen

Aktivierungsprobleme verlaufen stumm - ein Segment hört auf zu fließen, und Ihre Kampagne wird ohne Warnung an eine kleinere Liste gesendet. Dadurch werden Oberflächenlücken und Fehler angezeigt, bevor sie die Ergebnisse beeinflussen.

**Eingabeaufforderungen**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++Wissen, was funktioniert und worauf wir uns als Nächstes konzentrieren sollten

Die Leistungstrends auf allen Kanälen sagen Ihnen, wo Sie investieren und was Sie zurückholen sollten. Anhand dieser Eingabeaufforderungen können Sie die treibenden Ergebnisse ermitteln und erkennen, wohin die Aufmerksamkeit des nächsten Quartals gehen sollte.

**Eingabeaufforderungen**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++


## Weitere Informationen

| Ressource | Was Sie finden werden |
| --- | --- |
| [Dokumentation zu AJO](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/ajo-home){target="_blank"} | Vollständige Dokumentation zu AJO-Programmen |
| [AJO MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server){target="_blank"} | AJO MCP Server-Tools und Verfügbarkeit |
| [CJA MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | CJA MCP Server-Tools und Verfügbarkeit |
