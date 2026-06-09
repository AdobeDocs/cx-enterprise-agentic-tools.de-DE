---
title: Optimieren von Inhalten basierend auf Leistungsdaten
description: Verwenden Sie CJA und AEM gemeinsam in einer KI-Sitzung, um Kampagnen mit Konversionslücken zu finden, die Ursache zu diagnostizieren und den Inhalt zu aktualisieren, ohne die Tools zu wechseln.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: ed47f1547e6949fc71417e7d99d83802ae3c2134
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 2%

---


# Optimieren von Inhalten basierend auf Leistungsdaten
<!-- last-modified: 2026-06-08 -->

![KI-Client, der den ursprünglichen und den aktualisierten Seiteninhalt nebeneinander vergleicht](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png)

Das Schließen des Kreislaufs zwischen Kampagnenleistungsdaten und Inhaltsaktualisierungen bedeutet normalerweise, dass zwischen Ihrem Analytics-Tool und Ihrer CMS gewechselt wird. In dieser exemplarischen Vorgehensweise wird gezeigt, wie Customer Journey Analytics und AEM in derselben KI-Sitzung verbunden werden: Aufdecken von Kampagnen mit Konversionslücken, Diagnostizieren der Ursachen, Überprüfen der Inhalte, Abrufen zielgerichteter Empfehlungen und Anwenden von Änderungen, ohne das Gespräch zu verlassen.

| Szenario-Details | |
| --- | --- |
| CX Enterprise-Anwendungen | [Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-overview/cja-overview), [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/overview/introduction) |
| Agent-Tools | [CX Enterprise MCP](../tools/mcp-servers.md#cx-enterprise-mcp-servers), [AEM Content MCP Server](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) |
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
| CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
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
| CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Vollständiges Setup: [ChatGPT MCP-Dokumentation](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Andere KI-Clients]

Verwenden Sie Gemini, Microsoft Copilot, Cursor, Claude Code oder eine andere MCP-kompatible Umgebung? Verbinden Sie sich mit beiden MCP-Servern mithilfe der folgenden Endpunkte:

| Server | Endpunkt |
| --- | --- |
| CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Vollständige Setup-Anweisungen für alle unterstützten Clients: [Verbinden mit Ihrem KI-Client](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Melden Sie sich bei Aufforderung mit Ihrer Adobe ID an und wählen Sie die mit Ihrer CJA- und AEM-Umgebung verknüpfte IMS-Organisation aus. Die Wahl der falschen Organisation ist die häufigste Ursache für Authentifizierungsfehler.
>
>Bei der ersten Verbindung kann Ihr KI-Client Sie auffordern, eine IMS-Organisation auszuwählen oder eine Sandbox anzugeben. Sobald dieser Kontext festgelegt ist, verwendet ihn der MCP-Server für den Rest der Sitzung.
>
>Einige Tools fordern Sie vor der Ausführung zur Genehmigung auf. Überprüfen Sie die Anfrage und genehmigen oder ablehnen Sie. Ohne Ihre Bestätigung wird keine Aktion durchgeführt.


## Schritt 1: Suchen von Kampagnen mit einer Konversionslücke

Verwenden Sie CJA, um Kampagnen aufzudecken, bei denen der Clickthrough hoch, die Konversionsrate jedoch niedrig ist. Dieses Muster (hoher Intent, geringer Abschluss) verweist in der Regel auf ein Inhalts- oder Erlebnisproblem auf der Landingpage.

```
Which campaigns have strong click-through but low conversion in the last 30 days?
```

+++Siehe eine Beispielantwort

![KI-Client-Kampagnen mit hohem Clickthrough, aber geringer Konversion von CJA](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step1-campaigns.png)

+++



## Schritt 2: Diagnose der Grundursache

Folgen Sie, um zu verstehen, was die Lücke verursacht. Fragen Sie, ob sich der Abbruch auf einen bestimmten Gerätetyp, ein bestimmtes Zielgruppensegment oder eine bestimmte Inhaltsinteraktion konzentriert.

```
What's causing the conversion drop-off, is it device, segment, or content?
```

+++Siehe eine Beispielantwort

![KI-Client, der den Konversionsrückgang nach Geräte-, Segment- und Inhaltsfaktoren diagnostiziert](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step2-diagnosis.png)

+++



## Schritt 3: Inhalt in AEM überprüfen

Ziehen Sie bei identifizierter schwacher Kampagne in derselben Sitzung die Landingpage aus AEM. Wenn Sie sehen, was auf der Seite derzeit steht, können Sie verstehen, was geändert werden muss.

```
Show me the Bali Surf Camp page.
```

+++Siehe eine Beispielantwort

![KI-Client, der den aktuellen Inhalt der Landingpage aus AEM anzeigt](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step3-page-content.png)

+++



## Schritt 4: Abrufen zielgerichteter Empfehlungen

Bitten Sie Ihren KI-Client, die angezeigten Daten mit dem zu verbinden, was sich auf der Seite befindet. Die KI-Gründe für beide Quellen identifizieren, welche Inhaltsabschnitte wahrscheinlich den Abbruch verursachen und was sich ändern sollte.

```
Which content sections are underperforming, and what changes would you recommend?
```

+++Siehe eine Beispielantwort

![KI-Client, der leistungsschwache Inhaltsabschnitte identifiziert und spezifische Änderungen empfiehlt](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step4.gif)

+++



## Schritt 5: Änderungen anwenden und überprüfen

Bitten Sie Ihren KI-Client, eine optimierte Version der Seite basierend auf den Empfehlungen zu erstellen, und fassen Sie zusammen, was sich geändert hat und warum.

```
Create an optimized version of the Bali Surf Camp page and summarize the proposed changes.
```

+++Siehe eine Beispielantwort

![KI-Client, der eine optimierte Version der Seite erstellt und die Änderungen zusammenfasst](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5.gif)

+++


>[!CAUTION]
>
>Überprüfen Sie die vollständige Zusammenfassung der vorgeschlagenen Änderungen, bevor Sie sie bestätigen. Der AEM Content MCP Server schreibt Änderungen in Ihre AEM-Umgebung. Die Seiten verbleiben in ihrem veröffentlichten Status, bis Sie sie erneut veröffentlichen.


## Was Sie erreicht haben

Sie haben Customer Journey Analytics und AEM in einer einzigen KI-Sitzung verbunden und von Kampagnendaten zu bereitgestellten Inhaltsänderungen verschoben, ohne die Tools zu wechseln. Sie haben Kampagnen mit Konversionslücken identifiziert, die Grundursache diagnostiziert, die Landingpage geprüft, zielgerichtete Empfehlungen erhalten, die sowohl auf Daten als auch auf Inhalten basieren, und die Änderungen in derselben Konversation angewendet. Dadurch wird die Feedback-Schleife zwischen Analytics insight und veröffentlichten Inhalten verkürzt und auf eine beliebige Anzahl leistungsschwacher Seiten in derselben Sitzung skaliert.


## Mehr können Sie erreichen

Wenn CJA und AEM in derselben Sitzung verbunden sind, können Sie den gesamten Zyklus von der Identifizierung von Problemen bis hin zu Versandkorrekturen abdecken. Erweitern Sie ein unten stehendes Szenario, um Eingabeaufforderungen anzuzeigen, die Sie ausprobieren können.

+++Suchen nach Inhalten, die die Leistung beeinträchtigen

Hoher Traffic mit geringer Interaktion signalisiert ein Inhaltsproblem, kein Verkehrsproblem. Mithilfe dieser Eingabeaufforderungen können bestimmte Seiten und Muster angezeigt werden, die bearbeitet werden müssen, bevor eine Kampagnentermine das Problem erzwingt.

**Eingabeaufforderungen**

```
Which campaigns have the highest traffic but lowest conversion rate this quarter?
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for landing pages across email and paid social campaigns.
```

```
Find AEM pages linked from active campaigns that haven't been updated in over 60 days.
```

+++

+++Korrigieren, was die Daten von Ihnen verlangen

Sobald Sie wissen, was hinter den Erwartungen zurückbleibt, sollten Sie zielgerichtete Änderungen vornehmen, die auf den Leistungsdaten basieren. Mit diesen Eingabeaufforderungen können Sie bestimmte Abschnitte basierend auf der Diagnose aktualisieren.

**Eingabeaufforderungen**

```
Update the CTA on the [page name] page to better match the campaign audience.
```

```
Rewrite the hero headline on the [page name] page to address the mobile drop-off.
```

```
Add a trust signal to the [page name] page above the conversion form.
```

```
Which pages updated in this session still need to be published?
```

+++

+++Versandverbesserungen vor der nächsten Kampagne

Änderungen, die während der Sitzung vorgenommen wurden, können sich schnell stapeln. Mit diesen Eingabeaufforderungen können Sie überprüfen, was bereit ist, Aktualisierungen zur Überprüfung gruppieren und sauber weiterleiten, bevor eine Kampagne live geschaltet wird.

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
Publish all confirmed changes and share the updated URLs.
```

+++



## Weitere Informationen

| Ressource | Was Sie finden werden |
| --- | --- |
| [Dokumentation zum CJA MCP-Server](https://developer.adobe.com/analytics-mcp/docs/cja/) | CJA MCP-Setup und Tool-Referenz |
| [Dokumentation zu AEM Content MCP Server](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | AEM Content MCP-Setup- und -Benutzerhandbuch |
| [CJA MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP Server-Tools und Verfügbarkeit |
| [AEM Content MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | AEM Content MCP Server-Tools und -Verfügbarkeit |
| [MCP-Server](../tools/mcp-servers.md) | Verbinden eines KI-Clients mit Adobe MCP-Servern |
