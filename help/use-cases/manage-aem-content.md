---
title: Halten Sie Inhalte aktuell und versenden Sie Updates schneller
description: Verwenden Sie den AEM Content MCP Server zum Suchen, Überprüfen, Aktualisieren und Veröffentlichen von AEM-Inhalten, ohne zwischen Tools zu wechseln.
last-substantial-update: 2026-05-22T00:00:00Z
index: false
source-git-commit: 270aed67540f7347850aece70cebddc9b40b9de8
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 1%

---


# Halten Sie Inhalte aktuell und versenden Sie Updates schneller

<!-- last-modified: 2026-05-22 -->

![KI-Client, der bestätigt, dass die Seite veröffentlicht wurde, und die Live-URL zurückgibt](../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png)

Für Inhaltsvorgänge in Adobe Experience Manager, vom Suchen nach Seiten und Überprüfen von Inhalten bis hin zu Aktualisierungen und Veröffentlichungen, ist in der Regel die direkte Navigation in der AEM-Oberfläche erforderlich. In dieser exemplarischen Vorgehensweise wird gezeigt, wie diese Vorgänge über einen KI-Client mithilfe des AEM Content MCP Servers verarbeitet werden können, damit Content-Teams schneller arbeiten können, ohne zwischen Tools wechseln zu müssen.

| | |
| --- | --- |
| CX Enterprise-Anwendungen | Adobe Experience Manager as a Cloud Service |
| Agent-Tools | AEM Content MCP Server |
| Zielgruppe | Content-Manager, Marketing-Teams |
| Voraussetzung | MCP-kompatibler KI-Client, Zugriff auf AEM as a Cloud Service |

Jeder Schritt zeigt eine repräsentative Eingabeaufforderung und eine Beispiel-KI-Antwort. Ein **Mehr können Sie erreichen** Abschnitt folgt für weitere Untersuchungen in derselben Sitzung.

## Voraussetzungen

>[!BEGINTABS]

>[!TAB Claude.ai]

Verbinden Sie den AEM Content MCP Server als benutzerdefinierten Connector.

1. Gehen Sie **Claude.ai zu Einstellungen** Integrationen.
2. Wählen Sie **Benutzerdefinierten Connector hinzufügen** und geben Sie die Server-URL ein: `https://mcp.adobeaemcloud.com/adobe/mcp/content`
3. Wählen Sie **Verbinden** aus und melden Sie sich mit Ihrer Adobe ID an.

Vollständiges Setup: [Claude.ai Custom Connectors-Dokumentation](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Verbinden Sie den AEM Content MCP Server mit dem ChatGPT-Entwicklermodus (Pro-, Plus-, Business-, Enterprise- oder Education-Plan erforderlich).

1. Aktivieren Sie **Entwicklermodus** in **ChatGPT-Einstellungen**.
2. Navigieren Sie zu **Einstellungen > Integrationen** und wählen Sie **Benutzerdefinierten Connector hinzufügen > Remote-MCP-Server**.
3. Server-URL eingeben: `https://mcp.adobeaemcloud.com/adobe/mcp/content`
4. Wählen Sie **Verbinden** aus und melden Sie sich mit Ihrer Adobe ID an.

Vollständiges Setup: [ChatGPT MCP-Dokumentation](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Andere KI-Clients]

Verwenden Sie Gemini, Microsoft Copilot, Cursor, Claude Code oder eine andere MCP-kompatible Umgebung? Stellen Sie mithilfe dieses Endpunkts eine Verbindung zum AEM Content MCP Server her:

```
https://mcp.adobeaemcloud.com/adobe/mcp/content
```

Vollständige Setup-Anweisungen für alle unterstützten Clients: [Verbinden mit Ihrem KI-Client](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Melden Sie sich bei Aufforderung mit Ihrer Adobe ID an und wählen Sie die mit Ihrer AEM as a Cloud Service-Umgebung verknüpfte IMS-Organisation aus. Berechtigungen werden auf AEM-Ebene erzwungen. Ihr KI-Client kann nur Vorgänge ausführen, für die Ihr Konto autorisiert ist.
>
>Wenn Sie nur Inhalte durchsuchen oder überprüfen müssen, ohne Änderungen vorzunehmen, verwenden Sie stattdessen den schreibgeschützten Server-Endpunkt: `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly`. Alle Erkennungs- und Überprüfungsaufforderungen auf dieser Seite funktionieren mit beiden Servern.
>
>Bei der ersten Verbindung fordert Sie Ihr KI-Client möglicherweise auf, Ihre Organisation oder AEM-Umgebung zu bestätigen. Sobald dieser Kontext festgelegt ist, verwendet ihn der MCP-Server für den Rest der Sitzung.
>
>Einige Tools fordern Sie vor der Ausführung zur Genehmigung auf. Überprüfen Sie die vorgeschlagene Aktion und genehmigen oder ablehnen Sie diese. Es wird keine Änderung ohne Ihre Bestätigung vorgenommen.

## Schritt 1: Suchen von Inhalten in Ihrer AEM-Umgebung

Bitten Sie zunächst Ihren KI-Client, Ihre AEM-Umgebungen zu entdecken und nach Inhalten zu suchen. Sie können nach Thema, Keyword oder Inhaltstyp suchen, ohne genaue Pfade zu kennen.

```
From WKND Dev environment, find all ski related content.
```

+++Siehe eine Beispielantwort

![KI-Client, der Suchergebnisse für Skiinhalte aus der WKND Dev AEM-Umgebung anzeigt](../assets/use-cases/manage-aem-content/manage-aem-content-step1-find-ski.png)

+++


## Schritt 2: Überprüfen einer bestimmten Seite

Sobald Sie relevante Inhalte gefunden haben, bitten Sie Ihren KI-Client, Ihnen eine bestimmte Seite anzuzeigen. Sie können Seiten nach Name oder Pfad referenzieren. Der MCP-Server löst die Referenz auf und gibt die Inhaltsstruktur zurück.

```
Show me the US English Home Page.
```

+++Siehe eine Beispielantwort

![KI-Client, der die Inhaltsstruktur der US-englischen Startseite von AEM anzeigt](../assets/use-cases/manage-aem-content/manage-aem-content-step2-home-page.png)

+++


## Schritt 3: Inhalt verbessern

Bitten Sie angesichts des angezeigten Seiteninhalts Ihren KI-Client, Verbesserungen vorzuschlagen oder anzuwenden. Die KI kann Kopieränderungen vorschlagen, die auf dem basieren, was die Seite aktuell sagt, und um Bestätigung bitten, bevor sie etwas schreibt.

```
Improve the Hero CTAs.
```

+++Siehe eine Beispielantwort

![KI-Client, der eine verbesserte Hero CTA-Kopie mit einer Bestätigungsaufforderung vor dem Anwenden von Änderungen vorschlägt](../assets/use-cases/manage-aem-content/manage-aem-content-step3.gif)

+++


>[!CAUTION]
>
>Bestätigen Sie jede Änderung bei Aufforderung. Der AEM Content MCP Server kann Inhalte erstellen, aktualisieren und löschen. Überprüfen Sie die vorgeschlagene Änderung vor der Genehmigung, insbesondere auf Live-Seiten.

## Schritt 4: Veröffentlichen und freigeben

Nach Bestätigung der Aktualisierung veröffentlichen Sie die Seite und rufen eine freigabefähige URL ab - alles im selben Gespräch.

```
Publish the changes and share the URL.
```

+++Siehe eine Beispielantwort

![KI-Client, der bestätigt, dass die Seite veröffentlicht wurde, und die Live-URL zurückgibt](../assets/use-cases/manage-aem-content/manage-aem-content-step4.gif)

+++


## Was Sie erreicht haben

Sie haben den AEM Content MCP-Server verwendet, um Inhalte zu finden, eine Live-Seite zu überprüfen, von KI vorgeschlagene Verbesserungen anzuwenden und das Ergebnis zu veröffentlichen, ohne die AEM-Benutzeroberfläche zu öffnen. Durch die Kombination von Inhaltserkennung, -bearbeitung und -veröffentlichung in einer einzigen KI-Sitzung können Content-Teams von der Identifizierung einer Lücke zur schnelleren Bereitstellung einer Aktualisierung mit weniger Kontextwechseln übergehen. Derselbe Workflow kann auf mehrere Seiten, Inhaltsfragmente und koordinierte Kampagnen-Launches skaliert werden.

## Mehr können Sie erreichen

Der AEM Content MCP Server verarbeitet weit mehr als in der Anleitung beschrieben. Erweitern Sie ein unten stehendes Szenario, um Eingabeaufforderungen anzuzeigen, die Sie in derselben Sitzung versuchen können.

+++Vor einer Site-Überprüfung oder einem Neustart

Inhaltsüberwachungen sind zeitaufwendig, wenn sie manuell durchgeführt werden. Mit diesen Eingabeaufforderungen können Sie schnell veraltete Inhalte, Entwürfe, die nie bereitgestellt wurden, und Lücken, die vor einem größeren Push korrigiert werden müssen, aufdecken.

**Eingabeaufforderungen**

```
Show me everything updated in the last two weeks.
```

```
What content is sitting in draft and hasn't been published yet?
```

```
Find pages that haven't been touched in over a year.
```

```
Which pages are missing their description field?
```

```
We're reorganizing the taxonomy. Find all articles missing tags or categories.
```

+++

+++Beheben von SEO- und Barrierefreiheitsproblemen im benötigten Umfang

Lücken in Bezug auf SEO und Barrierefreiheit verstärken sich schnell auf großen Websites. Diese Eingabeaufforderungen helfen Ihnen, die Probleme zu finden und zu priorisieren, die vor einem Audit oder Launch am wichtigsten sind.

**Eingabeaufforderungen**

```
Pull a list of all pages with an empty meta description.
```

```
Which pages have thin content that's likely to underperform for SEO?
```

```
Find all images missing alt text.
```

```
Our CTAs aren't consistent. Scan the site and flag anywhere the call-to-action wording differs from "Book now."
```

```
The homepage was updated yesterday. Show me what changed compared to the version before.
```

+++

+++Halten Sie Ihre Asset-Bibliothek gut organisiert und bereit

Beschädigte Asset-Verweise und nicht verarbeitete Uploads verlangsamen die Inhaltserstellung. Mithilfe dieser Eingabeaufforderungen können Sie Assets suchen und verwalten, bevor sie eine Seitenaktualisierung oder Kampagne blockieren.

**Eingabeaufforderungen**

```
We're building a biking content series. What image assets do we already have?
```

```
Can you upload a placeholder asset from https://placehold.co/800x450/png to the wknd folder and save it as placeholder.png?
```

```
That asset was just uploaded. Is it processed and ready to use in a page?
```

```
I need to replace the hero image across the site. Which fragments are currently using it?
```

+++

+++Koordinieren eines Inhaltsstarts über mehrere Seiten hinweg

Der Start einer Kampagne bedeutet häufig, dass Änderungen über mehrere Inhaltsfragmente und Seiten hinweg koordiniert werden müssen. Diese Eingabeaufforderungen helfen Ihnen, Aktualisierungen zu gruppieren, zu überprüfen, bevor Sie sie bewerben, und sauber zu versenden.

**Eingabeaufforderungen**

```
I need to update the surfing adventure. Show me its content and all its fields.
```

```
Create an EMEA market variation of the ski adventure fragment.
```

```
Bundle everything we changed in this session into a launch called May Updates.
```

```
What launches are open right now, and which ones are ready to promote?
```

```
Before I promote, show me exactly what changed between May Updates and what is currently live.
```

```
Promote the May Updates launch to production.
```

+++


## Weitere Informationen

| Ressource | Was Sie finden werden |
| --- | --- |
| [Dokumentation zu AEM Content MCP Server](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | Setup- und Benutzerhandbuch für MCP-Server |
| [AEM Content MCP-Server in der KI-Registrierung](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | Toolliste und Verfügbarkeit |
| [Dokumentation von AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service) | Vollständige Dokumentation zu AEM-Programmen |
| [AEM-Inhaltsfragmente](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments) | Authoring-Referenz für Inhaltsfragmente |
| [MCP-Server](../tools/mcp-servers.md) | Verbinden eines KI-Clients mit Adobe MCP-Servern |
