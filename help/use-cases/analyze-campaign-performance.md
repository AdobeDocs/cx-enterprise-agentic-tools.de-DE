---
title: Aufdecken von Kampagneneinblicken ohne Erstellen von Berichten
description: Verwenden Sie den CX Enterprise MCP, um Customer Journey Analytics-Leistungsfragen in verständlicher Sprache zu stellen und Antworten zu erhalten, ohne zu Report Builder navigieren zu müssen.
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: 937a3189965f3a3551c730bb27ee0592ae6fca92
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 1%

---


# Aufdecken von Kampagneneinblicken ohne Erstellen von Berichten

<!-- last-modified: 2026-06-02 -->

![KI-Client mit empfohlenen nächsten Schritten zur Verbesserung der Kampagnenleistung](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png){zoomable="yes"}

*Zum Zoomen auswählen.*

Die Kampagnenanalyse, die früher die Erstellung von Berichten in einem separaten Tool erforderte, wird jetzt zur Diskussion gestellt. In dieser exemplarischen Vorgehensweise wird gezeigt, wie Sie einen KI-Client mit Customer Journey Analytics (CJA) verbinden und Leistungsfragen in einfacher Sprache stellen. Das Ergebnis ist eine schnellere insight-Bereitstellung, ohne dass manuelle Berichtserstellungen erforderlich sind.

| Szenario-Details | |
| --- | --- |
| CX Enterprise-Anwendungen | [Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-overview/cja-overview) |
| Agent-Tools | [CX Enterprise MCP](../tools/mcp-servers.md#cx-enterprise-mcp-servers) |
| Zielgruppe | Analysten, Kampagnen-Manager |
| Voraussetzung | MCP-kompatibler KI-Client, Zugriff auf CJA |

Jeder Schritt zeigt eine repräsentative Eingabeaufforderung und eine Beispiel-KI-Antwort. Ein **Mehr können Sie erreichen** Abschnitt folgt für weitere Untersuchungen in derselben Sitzung.

## Voraussetzungen

>[!BEGINTABS]

>[!TAB Claude.ai]

Verbinden Sie den CX Enterprise MCP als benutzerdefinierten Connector, um auf Customer Journey Analytics-Tools zuzugreifen.

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
>Melden Sie sich bei Aufforderung mit Ihrer Adobe ID an und wählen Sie die mit Ihren CJA-Datenansichten verknüpfte IMS-Organisation aus. Die Wahl der falschen Organisation ist die häufigste Ursache für Authentifizierungsfehler.
>
>Bei der ersten Verbindung kann Ihr KI-Client Sie auffordern, eine IMS-Organisation auszuwählen oder eine Sandbox anzugeben. Sobald dieser Kontext festgelegt ist, verwendet ihn der MCP-Server für den Rest der Sitzung.
>
>Einige Tools fordern Sie vor der Ausführung zur Genehmigung auf. Überprüfen Sie die Anfrage und genehmigen oder ablehnen Sie. Ohne Ihre Bestätigung wird keine Aktion durchgeführt.

## Schritt 1: Verfügbare Datenansichten entdecken

Bitten Sie zunächst Ihren KI-Client, die in Ihrem CJA-Konto verfügbaren Datenansichten aufzulisten. Auf diese Weise erfahren Sie, welche Datensätze Sie abfragen können, bevor Sie Berichte ausführen.

```
What data views are available in my CJA account?
```

+++Siehe eine Beispielantwort

![AI-Client mit den verfügbaren CJA-Datenansichten](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step1-data-views.png){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


## Schritt 2: Abrufen der Kampagnenleistungsdaten

Nachdem eine Datenansicht identifiziert wurde, können Sie die Kampagnenleistung nach Umsatz und Konversionsrate abfragen. Die KI löst Metrik- und Dimensionsnamen aus der Datenansicht auf, ohne dass technische IDs erforderlich sind.

```
For '[data view name]', show me the top campaigns by revenue and conversion rate for the last 30 days.
```

+++Siehe eine Beispielantwort

![KI-Client, der die Top-Kampagnen nach Umsatz und Konversionsrate aus der Omni-Channel-/Multi-Industry-Datenansicht anzeigt](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step2.gif){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


>[!NOTE]
>
>Ersetzen Sie `[data view name]` durch den Namen Ihrer Datenansicht aus Schritt 1. Führen Sie vor der Freigabe für Stakeholder einen Abgleich der Ergebnisse in Analysis Workspace mit derselben Datenansicht und demselben Datumsbereich durch.

## Schritt 3: Identifizieren, was die Leistung steigert

Bitten Sie Ihren KI-Client zu erklären, was die Leistungsunterschiede zwischen Kampagnengruppen verursacht. Dies wird von den Überschriftennummern zu den unten stehenden Variablen verschoben.

```
What factors are driving the results for these campaign groups?
```

+++Siehe eine Beispielantwort

![KI-Client - Erläuterung der Faktoren, die die Leistung von Kampagnengruppen bestimmen](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step3.gif){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


## Schritt 4: Aufschlüsselung nach einem bestimmten Kampagnentyp

Follow-up zu einem bestimmten Ergebnis, indem Sie nach einer Aufschlüsselung auf Segmentebene fragen. Dadurch wird deutlich, welche Kundentypen die Leistung innerhalb eines Kampagnentyps steigern.

```
Break down Promotional Email Campaigns by Customer Segment and explain what's driving the high conversion rate.
```

+++Siehe eine Beispielantwort

![KI-Client für die Aufschlüsselung der Leistung von Werbe-E-Mail-Kampagnen nach Kundensegment](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step4-segment-breakdown.png){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


## Schritt 5: Ergreifen Sie Maßnahmen bezüglich Ihrer gefundenen Inhalte.

Fordern Sie nach priorisierten Empfehlungen, die auf allem basieren, was in der Sitzung aufgetaucht ist. Die Anforderung von Schätzungen des Unternehmenswerts hilft Ihnen bei der Entscheidung, wo Sie zuerst handeln sollten.

```
Based on these findings, recommend the highest-impact actions to increase revenue and conversion rates. Prioritize recommendations by expected business value and estimate the potential uplift.
```

+++Siehe eine Beispielantwort

![KI-Kunde, der priorisierte Aktionen mit geschätztem Geschäftswert empfiehlt](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5.gif){zoomable="yes"}

*Zum Zoomen auswählen.*

+++


>[!NOTE]
>
>CJA-Tools, auf die über den CX Enterprise MCP zugegriffen wird, können in derselben Sitzung Segmente, berechnete Metriken und Workspace-Projekte in CJA erstellen. Um Kampagnen, Journey oder Inhalte in anderen Anwendungen zu aktualisieren, verbinden Sie den entsprechenden MCP-Server oder gehen Sie direkt zur Anwendung.

## Was Sie erreicht haben

Sie haben einen KI-Client mit Customer Journey Analytics verbunden und in fünf Eingabeaufforderungen von der Ermittlung von Datenansichten zu priorisierten Geschäftsempfehlungen gewechselt. Sie haben die wichtigsten Kampagnen nach Umsatz und Konversionsrate identifiziert, die Faktoren für die Leistung zwischen Kampagnengruppen angezeigt, Details auf Segmentebene für einen bestimmten Kampagnentyp aufgeschlüsselt und Rangfolgenempfehlungen mit geschätzter Steigerung erhalten. Dieser Ansatz ersetzt die Berichterstellung durch ein direktes Gespräch, wodurch die Zeit zwischen einer geschäftlichen Frage und einem datengestützten Aktionsplan verkürzt wird.

## Mehr können Sie erreichen

Der CX Enterprise MCP kann weit mehr Customer Journey Analytics-Einblicke liefern als in der Anleitung beschrieben. Erweitern Sie ein unten stehendes Szenario, um Eingabeaufforderungen anzuzeigen, die Sie in derselben Sitzung versuchen können.

+++Finden Sie heraus, was funktioniert und was nicht

Ein kurzer Überblick darüber, welche Kampagnen durchgeführt werden und welche nicht, hilft Ihnen, Ihren Aufwand zu konzentrieren, bevor Sie detaillierte Berichte lesen. Diese Eingabeaufforderungen geben Ihnen das Bild in einer Sitzung.

**Eingabeaufforderungen**

```
Which campaigns are driving the most revenue and conversions?
```

```
Show me the campaigns that need attention this month.
```

```
What channels are outperforming expectations?
```

```
Identify the biggest performance changes compared to last month.
```

```
Show me conversion performance by traffic source.
```

+++

+++Die treibenden Ergebnisse verstehen

Überschriftenmetriken sagen Ihnen, was passiert ist. Diese Eingabeaufforderungen helfen Ihnen zu verstehen, warum: welche Segmente, Kanäle und Touchpoints hinter den Zahlen liegen.

**Eingabeaufforderungen**

```
What factors are driving revenue growth?
```

```
Explain why conversion rates changed this quarter.
```

```
Break down campaign performance by customer segment.
```

```
Which customer segments are growing fastest?
```

```
Which touchpoints contribute most to conversions?
```

+++

+++Wachstumschancen entdecken

Zu wissen, wo die Leistung stark ist, ist nur die Hälfte. Anhand dieser Eingabeaufforderungen können Sie erkennen, wo Sie mehr investieren können, welche Zielgruppen über Reserven verfügen und welche Kampagnen skalierbar sind.

**Eingabeaufforderungen**

```
Where should we invest more marketing budget?
```

```
Which audiences have the greatest growth potential?
```

```
Which campaigns should we scale?
```

```
What would have the biggest impact on revenue?
```

+++

+++Erkenntnisse in Maßnahmen umsetzen

CJA-Tools, auf die über den CX Enterprise MCP zugegriffen wird, können Segmente, Zielgruppen, berechnete Metriken und Workspace-Projekte direkt in CJA erstellen, ohne die KI-Sitzung verlassen zu müssen. Verwenden Sie diese Eingabeaufforderungen, um auf das zu reagieren, was Sie gefunden haben.

**Eingabeaufforderungen**

```
Create a segment for high-value customers.
```

```
Build an audience from recent purchasers.
```

```
Create a calculated metric for conversion efficiency.
```

```
Save this analysis as a Workspace project for executive reporting.
```

+++


## Weitere Informationen

| Ressource | Was Sie finden werden |
| --- | --- |
| [CJA MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | CJA MCP Server-Tools und Verfügbarkeit |
| [Dokumentation zu Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing){target="_blank"} | Vollständige Dokumentation zu CJA-Programmen |
