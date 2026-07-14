---
title: Zielgruppen verstehen und wo sie aktiviert werden
description: Verwenden Sie das CX Coworker Gateway, um den Status der Zielgruppenaktivierung zu überwachen, den Zustand des Ziels zu überprüfen und Probleme aufzudecken, bevor sie sich auf Ihre Kampagnen auswirken.
last-substantial-update: 2026-07-14T00:00:00Z
source-git-commit: 4f557937701441bcc34878e3cd13423ce35487ba
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 2%

---


# Zielgruppen verstehen und wo sie aktiviert werden

<!-- last-modified: 2026-06-04 -->

![KI-Client, der eine priorisierte Zielgruppenstrategie mit Aktivierungsempfehlungen bereitstellt](../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png){zoomable="yes"}

*Zum Zoomen auswählen.*

Zu wissen, welche Zielgruppen live sind, wohin sie fließen und ob die Ziele in Ordnung sind, ist entscheidend, bevor eine Kampagne gestartet wird oder wenn eine Kampagne nicht die gewünschte Leistung erbringt. In dieser exemplarischen Vorgehensweise wird gezeigt, wie ein vollständiges Aktivierungsbild über einen KI-Client erstellt wird, indem mit dem CX Coworker Gateway der Zielgruppenstatus und der Zielstatus in Sekunden angezeigt werden, ohne Real-Time CDP zu öffnen.

| Szenario-Details | |
| --- | --- |
| CX Enterprise-Anwendungen | [Real-Time Customer Data Platform (Real-Time CDP)](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/home) |
| Agent-Tools | [CX Coworker Gateway](../tools/mcp-servers.md#cx-coworker-gateway) |
| Zielgruppe | Marketing-Experten, Analysten, Benutzer |
| Voraussetzung | MCP-kompatibler KI-Client, Zugriff auf Real-Time CDP |

Jeder Schritt zeigt eine repräsentative Eingabeaufforderung und eine Beispiel-KI-Antwort. Ein **Mehr können Sie erreichen** Abschnitt folgt für weitere Untersuchungen in derselben Sitzung.

## Voraussetzungen

>[!BEGINTABS]

>[!TAB Claude.ai]

Verbinden Sie das CX Coworker Gateway als benutzerdefinierten Connector, um auf Real-Time CDP-Tools zuzugreifen.

1. Gehen Sie **Claude.ai zu Einstellungen** Integrationen.
2. Wählen Sie **Benutzerdefinierten Connector hinzufügen** und geben Sie die Server-URL ein: `https://cx-coworker-gateway.adobe.io/mcp`
3. Wählen Sie **Verbinden** aus und melden Sie sich mit Ihrer Adobe ID an.

Vollständiges Setup: [Claude.ai Custom Connectors-Dokumentation](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Verbinden Sie das CX Coworker Gateway mithilfe des ChatGPT-Entwicklermodus (Pro-, Plus-, Business-, Enterprise- oder Education-Plan erforderlich).

1. Aktivieren Sie **Entwicklermodus** in **ChatGPT-Einstellungen**.
2. Navigieren Sie zu **Einstellungen > Integrationen** und wählen Sie **Benutzerdefinierten Connector hinzufügen > Remote-MCP-Server**.
3. Server-URL eingeben: `https://cx-coworker-gateway.adobe.io/mcp`
4. Wählen Sie **Verbinden** aus und melden Sie sich mit Ihrer Adobe ID an.

Vollständiges Setup: [ChatGPT MCP-Dokumentation](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Andere KI-Clients]

Verwenden Sie Gemini, Microsoft Copilot, Cursor, Claude Code oder eine andere MCP-kompatible Umgebung? Stellen Sie mithilfe dieses Endpunkts eine Verbindung zum CX Coworker Gateway her:

```
https://cx-coworker-gateway.adobe.io/mcp
```

Vollständige Setup-Anweisungen für alle unterstützten Clients: [Verbinden mit Ihrem KI-Client](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Melden Sie sich bei Aufforderung mit Ihrer Adobe ID an und wählen Sie die mit Ihrer Real-Time CDP-Instanz verknüpfte IMS-Organisation aus. Die Wahl der falschen Organisation ist die häufigste Ursache für Authentifizierungsfehler.

## Schritt 1: Entdecken Sie Ihre Audiences und ihre Bedeutung

Fragen Sie zunächst nach einer Aufstellung der verfügbaren Zielgruppen und der von ihnen erfassten Kundenverhaltensweisen. Dadurch erhalten Sie die vollständige Landschaft, bevor Sie in ein bestimmtes Segment bohren.

```
What audiences are currently available and what customer behaviors do they represent?
```

+++Siehe eine Beispielantwort

![Der KI-Client listet die verfügbaren Zielgruppen und das von ihnen dargestellte Kundenverhalten auf](../assets/use-cases/query-audiences/query-audiences-step1-audience-list.png){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


## Schritt 2: Identifizieren Sie Ihre wertvollsten Segmente

Fragen Sie sich angesichts der Zielgruppenlandschaft, welche Segmente am größten sind und was sie strategisch wertvoll macht.

```
Which audiences are the largest and what makes them valuable?
```

+++Siehe eine Beispielantwort

![KI-Client, der die größten Zielgruppen identifiziert und erklärt, was sie wertvoll macht](../assets/use-cases/query-audiences/query-audiences-step2.gif){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


## Schritt 3: Überprüfen Sie Aktivierung und Ziele

Fragen Sie, wohin Ihre Zielgruppen derzeit fließen und für welche Ziele sie aktiviert sind.

```
Where are our audiences currently being activated and to which destinations?
```

+++Siehe eine Beispielantwort

![KI-Client, der den Status der Zielgruppenaktivierung und die Zielzuordnung anzeigt](../assets/use-cases/query-audiences/query-audiences-step3.gif){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


## Schritt 4: Abrufen strategischer Empfehlungen

Die RTCDP-Tools des CX Coworker Gateways sind schreibgeschützt. Sie ermöglichen einen Aktivierungsstatus, einen Zielzustand und Datenflussdaten, ändern jedoch nicht die Konfiguration. Nachdem Sie ein Problem identifiziert haben, erfolgt die Fehlerbehebung in der Anwendung.

```
If you were our audience strategist, what would you prioritize next and why?
```

+++Siehe eine Beispielantwort

![KI-Client, der priorisierte Empfehlungen für Zielgruppenstrategien gibt](../assets/use-cases/query-audiences/query-audiences-step4.gif){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


>[!NOTE]
>
>Die Ziel- und Aktivierungsdaten der RTCDP-Tools des CX-Coworker-Gateways können zwar die Zielkonfiguration, Segmentdefinitionen oder Datenflusseinstellungen ändern, jedoch nicht. In der Real-Time CDP-Anwendung werden Behebungsschritte ausgeführt.

## Was Sie erreicht haben

Sie haben einen KI-Client mit Real-Time CDP verbunden und an vier Eingabeaufforderungen ein strategisches Bild Ihres Zielgruppenportfolios erstellt. Sie haben die verfügbaren Zielgruppen den Kundenverhaltensweisen zugeordnet, die sie erfasst haben, Ihre größten und wertvollsten Segmente identifiziert, bestätigt, wo jede Zielgruppe hinfließt und zu welchen Zielen sie wechselt, und bei Ihrer nächsten Aktivierung priorisierte Empfehlungen erhalten. Dadurch wird die Navigation auf mehreren Real-Time CDP-Bildschirmen durch eine direkte, strategische Konversation ersetzt.

## Mehr können Sie erreichen

Die Real-Time CDP-Tools des CX Coworker Gateways unterstützen eine Vielzahl von Zielgruppen- und Aktivierungsabfragen. Erweitern Sie ein unten stehendes Szenario, um Eingabeaufforderungen anzuzeigen, die Sie in derselben Sitzung versuchen können.

+++Vor dem Versand einer Kampagne genau wissen, was wo fließt

Aktivierungsfehler sind unauffällig. Zielgruppen können ohne Warnung nicht mehr weitergeleitet werden und senden Kampagnen an veraltete Listen. Diese Eingabeaufforderungen geben Ihnen ein klares Bild darüber, welche Segmente welche Ziele wann erreichen.

**Eingabeaufforderungen**

```
Which audiences are activated to Google Ads?
```

```
Show me the activation history for the [audience name] audience.
```

```
What is the last refresh time for the [audience name] audience?
```

+++

+++Aktivierungsprobleme erkennen, bevor sie eine Kampagne betreffen

Ein Ziel, das einen Lauf verpasst hat, oder ein Segment ohne aktives Ziel, bedeutet, dass Ihre Kampagne möglicherweise weniger Personen erreicht als beabsichtigt. Diese Eingabeaufforderungen decken diese Lücken proaktiv auf.

**Eingabeaufforderungen**

```
Are there any audiences with no active destinations?
```

```
Are any destination dataflows showing errors right now?
```

```
Which audiences have not been updated in the last 30 days?
```

+++

+++Auditieren und Verstehen der Zielgruppenlandschaft

Wenn sich die Zielgruppengröße ändert oder neue Segmente erstellt werden, hilft Ihnen ein klarer Bestand bei der Planung und Vermeidung der Aktivierung der falschen Liste. Diese Eingabeaufforderungen geben Ihnen diese Sichtbarkeit auf Anfrage.

**Eingabeaufforderungen**

```
How many profiles are in the [segment name] segment?
```

```
Show me all audiences created in the last 30 days.
```

```
Which audience has grown the most in the last 60 days?
```

```
How many total profiles are in my Real-Time CDP instance?
```

+++

+++Identitäten und Datenqualität verstehen

Identitäts-Namespaces und Zusammenführungsrichtlinien wirken sich direkt darauf aus, welche Profile in einer Zielgruppe enthalten sind und wie sie aufgelöst werden. Dies zeigt Details zur Oberflächenkonfiguration an, die unerwartete Zielgruppengrößen oder Profilüberschneidungen erklären können.

**Eingabeaufforderungen**

```
What identity namespaces are configured and which are most commonly used?
```

```
What merge policies are defined and which audiences use each one?
```

```
Are there any audiences using a non-default merge policy that could cause profile overlap?
```

+++


## Weitere Informationen

| Ressource | Was Sie finden werden |
| --- | --- |
| [Adobe AI-Registrierung](https://developer.adobe.com/ai-registry/?type=mcp){target="_blank"} | Verwaltete Connectoren und Serverdetails für ausgewählte Adobe MCP-Server |
| [Dokumentation zu Real-Time CDP](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/home){target="_blank"} | Vollständige Dokumentation zu Real-Time CDP-Programmen |
