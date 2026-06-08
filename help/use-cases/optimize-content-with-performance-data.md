---
title: Optimieren von Inhalten basierend auf Leistungsdaten
description: Verwenden Sie CJA- und AEM-MCP-Server gemeinsam, um leistungsschwache Inhalte zu identifizieren und zu aktualisieren, ohne zwischen Tools zu wechseln.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# Optimieren von Inhalten basierend auf Leistungsdaten

<!-- last-modified: 2026-05-21 -->

![Optimieren von Inhalten basierend auf Leistungsdaten](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

Das Schließen des Kreislaufs zwischen Inhaltsleistungsdaten und Inhaltsaktualisierungen bedeutet normalerweise, dass zwischen Analytics und Ihrer CMS gewechselt wird. In dieser exemplarischen Vorgehensweise wird gezeigt, wie Customer Journey Analytics und AEM in derselben KI-Sitzung verbunden werden, sodass Sie unterdurchschnittliche Seiten aufdecken und aktualisieren können, ohne Ihr Gespräch verlassen zu müssen.

| | |
| --- | --- |
| CX Enterprise-Anwendungen | Customer Journey Analytics, Adobe Experience Manager as a Cloud Service |
| Agent-Tools | CX Enterprise MCP Gateway, AEM Content MCP Server |
| Zielgruppe | Kampagnen-Manager, Inhaltsstrategen, Marketing-Abläufe |
| Voraussetzung | MCP-kompatibler KI-Client, Zugriff auf CJA, Zugriff auf AEM as a Cloud Service |

Jeder Schritt zeigt eine repräsentative Eingabeaufforderung und eine Beispiel-KI-Antwort. Ein **Mehr können Sie erreichen** Abschnitt folgt für weitere Untersuchungen in derselben Sitzung.

## Voraussetzungen

>[!BEGINTABS]

>[!TAB Claude.ai]

Schließen Sie beide MCP-Server als benutzerdefinierte Connectoren an. Jede einzeln hinzufügen.

1. Gehen Sie **Claude.ai zu Einstellungen** Integrationen.
2. Wählen Sie **Benutzerdefinierten Connector hinzufügen**, geben Sie eine Server-URL ein und klicken Sie auf **Verbinden**.
3. Melden Sie sich mit Ihrer Adobe ID an und wiederholen Sie den Vorgang für den zweiten Server.

| Server | Endpunkt |
| --- | --- |
| CX Enterprise MCP-Gateway | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Vollständiges Setup: [Claude.ai Custom Connectors-Dokumentation](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Verbinden Sie beide MCP-Server über den ChatGPT-Entwicklermodus (Pro-, Plus-, Business-, Enterprise- oder Education-Plan erforderlich). Jeden Server separat hinzufügen.

1. Aktivieren Sie **Entwicklermodus** in **ChatGPT-Einstellungen**.
2. Navigieren Sie zu **Einstellungen > Integrationen** und wählen Sie **Benutzerdefinierten Connector hinzufügen > Remote-MCP-Server**.
3. Geben Sie eine Server-URL ein **wählen Sie &quot;**&quot; aus und melden Sie sich mit Ihrer Adobe ID an.
4. Wiederholen Sie diesen Vorgang für den zweiten Server.

| Server | Endpunkt |
| --- | --- |
| CX Enterprise MCP-Gateway | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Vollständiges Setup: [ChatGPT MCP-Dokumentation](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Andere KI-Clients]

Verwenden Sie Gemini, Microsoft Copilot, Cursor, Claude Code oder eine andere MCP-kompatible Umgebung? Verbinden Sie sich mit beiden MCP-Servern mithilfe der folgenden Endpunkte:

| Server | Endpunkt |
| --- | --- |
| CX Enterprise MCP-Gateway | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Vollständige Setup-Anweisungen für alle unterstützten Clients: [Verbinden mit Ihrem KI-Client](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Melden Sie sich bei Aufforderung mit Ihrer Adobe ID an und wählen Sie die mit Ihrer CJA- und AEM-Umgebung verknüpfte IMS-Organisation aus. Die Wahl der falschen Organisation ist die häufigste Ursache für Authentifizierungsfehler.
>
>Bei der ersten Verbindung kann Ihr KI-Client Sie auffordern, eine IMS-Organisation auszuwählen oder eine Sandbox anzugeben. Sobald dieser Kontext festgelegt ist, verwendet ihn der MCP-Server für den Rest der Sitzung.
>
>Einige Tools fordern Sie vor der Ausführung zur Genehmigung auf. Überprüfen Sie die Anfrage und genehmigen oder ablehnen Sie - es wird keine Aktion ohne Ihre Bestätigung durchgeführt.

## Schritt 1: Identifizieren Sie leistungsschwache Inhalte

Verwenden Sie das CX Enterprise MCP-Gateway, um die Seiten in Customer Journey Analytics nach Interaktions- und Konversionsmetriken zu ordnen. Das Ziel ist eine klare, priorisierte Liste von Inhalten, die Aufmerksamkeit erfordern.

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++Siehe eine Beispielantwort

Seiten mit der niedrigsten Interaktion (22. März bis 21. Mai 2026):

| Rang | Seite | Interaktionsrate | Bounce-Rate | Durchschnitt Zeit auf Seite |
| --- | --- | --- | --- | --- |
| 1 | /en/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /de/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /de/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recap | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12,3-14,1 % | 63-67 % | 0:35-1:10 |

Die durchschnittliche Interaktionsrate Ihrer Site beträgt 34,7 %. Diese Seiten sind 2-4x unter dem Durchschnitt.

+++

## Schritt 2: Inhalt in AEM überprüfen

Rufen Sie, ohne die KI-Sitzung zu verlassen, den aktuellen Status dieser Seiten aus AEM ab. Zu verstehen, was der Inhalt sagt, ist der erste Schritt zu wissen, was zu ändern ist.

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++Siehe eine Beispielantwort

**Seite:** `/en/products/analytics`
**Zuletzt geändert:** 30. April 2026 von T. MacMillan
**status:** veröffentlicht

**Hero-Abschnitt:**
Headline: „Datengesteuerte Entscheidungen für jedes Team“
Unterüberschrift: &quot;Adobe Analytics gibt Ihrem Unternehmen die nötigen Erkenntnisse, um zu handeln.“
CTA: „Demo anfordern“ → /contact/demo

**Body:** 3 Funktionsblöcke, gefolgt von einem Kundenlogo-Streifen und einer sekundären CTA. Kein Video oder interaktives Element. Die Seite wurde in 21 Tagen nicht aktualisiert.

**Meta-Beschreibung:** &quot;Adobe Analytics: Echtzeit-Reporting und KI-Einblicke für Unternehmens-Teams“

+++

## Schritt 3: Gezielte Aktualisierungen vornehmen

Nehmen Sie anhand der angezeigten Leistungsdaten und aktuellen Inhalte Aktualisierungen vor, die auf den enthüllten Daten basieren.

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++Siehe eine Beispielantwort

**Vorgeschlagene Änderung:**

| Feld | Aktueller Wert | Neuer Wert |
| --- | --- | --- |
| Hero-Überschrift | Datengesteuerte Entscheidungen für jedes Team | Schnellere Entscheidungen mit KI-gestützten Analysen |

Seite: `/en/products/analytics`

Diese Änderung bestätigen? Wenn Sie mit „Ja“ antworten, wird das Update in AEM geschrieben. Die Seite bleibt in ihrem aktuellen Status veröffentlicht, bis Sie sie erneut veröffentlichen.

+++

>[!CAUTION]
>
>Bestätigen Sie bei Aufforderung jede Inhaltsänderung. Überprüfen Sie den vollständigen Unterschied, bevor Sie Aktualisierungen an Live-Seiten genehmigen.

## Schritt 4: Überprüfen und veröffentlichen

Schließen Sie die Schleife, indem Sie alle Änderungen bestätigen und Inhalte hochstufen, wenn Sie mit den Aktualisierungen zufrieden sind.

```
Show me a summary of all changes made in this session.
```

+++Siehe eine Beispielantwort

**Sitzungszusammenfassung - 21. Mai 2026:**

| Seite | Ändern | Status |
| --- | --- | --- |
| /en/products/analytics | Hero-Überschrift aktualisiert | Gespeichert, Veröffentlichung aufgehoben |

1 Seite aktualisiert. Bereit zur Veröffentlichung, wenn bestätigt.

**Verbleibend aus Ihrer Low-Engagement-Liste:** 9 Seiten wurden in dieser Sitzung nicht aktualisiert. Möchten Sie mit der nächsten Seite fortfahren oder einen Launch zur Batch-Überprüfung vor der Veröffentlichung erstellen?

+++

## Was Sie erreicht haben

Sie haben Customer Journey Analytics und AEM in einer einzigen KI-Sitzung verbunden und Leistungsdaten verwendet, um Inhaltsänderungen direkt zu beeinflussen. Durch den Wechsel von der Metrik zur Aktualisierung ohne Wechsel der Tools haben Sie die Feedback-Schleife zwischen Analytics insight und veröffentlichten Inhalten verkürzt. Dies ist am wichtigsten im Kampagnenkalender, wo Dutzende von Seiten möglicherweise Aufmerksamkeit benötigen und manuelle, Tool-übergreifende Workflows zu Verzögerungen führen.

## Mehr können Sie erreichen

Die CJA- und AEM-MCP-Server unterstützen den gesamten Zyklus von der Problemidentifizierung bis hin zu Versandkorrekturen. Erweitern Sie ein unten stehendes Szenario, um Eingabeaufforderungen anzuzeigen, die Sie in derselben Sitzung versuchen können.

+++Suchen Sie nach Inhalten, die Ihre Leistung beeinträchtigen

Hoher Traffic mit geringer Interaktion signalisiert ein Inhaltsproblem, kein Verkehrsproblem. Mithilfe dieser Eingabeaufforderungen können Sie die spezifischen Seiten und Muster erkennen, die Ihrer Aufmerksamkeit bedürfen, bevor eine Kampagnentermine das Problem erzwingt.

**Eingabeaufforderungen**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++Korrigieren, was die Daten von Ihnen verlangen

Sobald man weiß, was hinter den Erwartungen zurückbleibt, ist der nächste Schritt, gezielte Änderungen vorzunehmen. Mit diesen Eingabeaufforderungen können Sie Überschriften, CTAs und Meta-Beschreibungen basierend auf den enthüllten Leistungsdaten aktualisieren.

**Eingabeaufforderungen**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++Versandverbesserungen vor der nächsten Kampagne

Änderungen, die während der Sitzung vorgenommen wurden, können sich schnell stapeln. Mithilfe dieser Eingabeaufforderungen können Sie die fertigen Elemente überprüfen, Aktualisierungen zu einem überprüfbaren Launch gruppieren und vor der Live-Schaltung einer Kampagne sauber weiterleiten.

**Eingabeaufforderungen**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Promote everything in the current launch to production.
```

+++

## Weitere Informationen

| Ressource | Was Sie finden werden |
| --- | --- |
| [Analytics-MCP-Dokumentation](https://developer.adobe.com/analytics-mcp/docs/) | CJA MCP-Setup und Tool-Referenz |
| [Dokumentation von AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service) | Vollständige Dokumentation zu AEM |
| [CJA MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP Server-Tools und Verfügbarkeit |
| [AEM Content MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | AEM Content MCP Server-Tools und -Verfügbarkeit |
| [MCP-Server](../tools/mcp-servers.md) | Verbinden eines KI-Clients mit Adobe MCP-Servern |
