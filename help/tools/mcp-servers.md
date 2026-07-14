---
title: MCP-Server
description: Verbinden eines beliebigen MCP-kompatiblen KI-Clients mit Adobe CX Enterprise-Workflows mithilfe von Model Context Protocol-Servern.
last-substantial-update: 2026-07-14T00:00:00Z
source-git-commit: 4f557937701441bcc34878e3cd13423ce35487ba
workflow-type: tm+mt
source-wordcount: '2421'
ht-degree: 6%

---


# MCP-Server

<!-- last-modified: 2026-06-11 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe MCP-Server bieten jedem kompatiblen KI-Client direkten, gesteuerten Zugriff auf Adobe-Daten und -Workflows. Wenn Sie einmal eine Verbindung herstellen, können Sie die Kampagnenleistung abfragen, Zielgruppen aktivieren, Journey überprüfen, Inhalte verwalten und vieles mehr - alles in einfacher Sprache, ohne Ihre KI-Umgebung verlassen zu müssen. Da sich MCP-Server zwischen Ihrem KI-Client und den zugrunde liegenden Systemen von Adobe befinden, erhalten Sie Flexibilität in natürlicher Sprache, während die Zugriffskontrollen und die Data Governance in Ihrem Unternehmen weiterhin gelten.

Adobe MCP-Server folgen dem Open [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro)-Standard. Jeder MCP-kompatible KI-Client stellt eine Verbindung zu jedem Adobe MCP-Server her.

## CX Coworker Gateway {#cx-coworker-gateway}

>[!CONTEXTUALHELP]
>id="cx-enterprise-agentic-tools_mcp_servers_cx-enterprise"
>title="CX Coworker Gateway"
>abstract="Ihre CX Enterprise-Anwendungen, auf die über einen einzigen MCP-Endpunkt zugegriffen werden kann. Fragen, analysieren und ergreifen Sie Maßnahmen in einfacher Sprache über Ihre KI-Clients."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview" text="Dokumentation zu CX Coworker Gateway"

![Das CX Coworker Gateway verbindet Ihren KI-Client mit Tools der gesamten Adobe CX Enterprise Suite](../assets/mcp-gateway-hero.gif)

Wählen Sie eine Anwendung aus, um den Endpunkt und die Funktionen anzuzeigen.

>[!BEGINTABS]

>[!TAB CX Coworker Gateway]

**Ein Endpunkt. Mehrere CX Enterprise-Anwendungen.**

Verbinden Sie sich einmal, und Ihr KI-Client erhält Zugriff auf CX Enterprise-Anwendungen basierend auf den Lizenzen Ihres Unternehmens. Um Ihre Organisation zu aktivieren, senden Sie eine E-Mail an [](mailto:cx-coworker-gateway-support@adobe.com)cx-coworker-gateway-support@adobe.com), um den Zugriff anzufordern.

```
https://cx-coworker-gateway.adobe.io/mcp
```

| CX Enterprise-Anwendung | Mögliche Optionen | Zusätzliche Berechtigung erforderlich |
| --- | --- | --- |
| [Adobe Analytics](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/analytics-mcp) | Erkennung von Report Suites, Segmenterstellung und Workspace-Erstellung | Nein |
| Campaign Classic | Erkennung der Campaign-Instanz, Schemabrowser, Abfrageausführung, Workflow-Kontrolle und SOAP/JS-Ausführung | Ja |
| [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/aep-mcp) | Datensatz-Erkennung, Schema-Browsing und Sandbox-Management | Nein |
| Experimentieren | A/B-, MVT- und MAB-Experimentberichte, Metriken, Einblicke, Opportunities und Planung des Stichprobenumfangs | Nein |
| GenStudio for Performance Marketing | Zugriff auf Daten zur Anzeigenleistung und kreative Einblicke | Ja |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/ajo-mcp) | Überprüfen von Journey-, Kampagnen- und Kanalkonfigurationen | Nein |
| Adobe Journey Optimizer B2B edition | Verwalten von B2B-Journey, Account-Programmen, Einkaufsgruppen und Personalisierung | Nein |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp) | Überprüfen von Aktivitäten, Angeboten, Zielgruppen, Mboxes, Leistungsberichten und Vorschau-URLs | [Ja](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp-get-started#mcp-security) |
| [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/cja-mcp) | Berichte abfragen, Datenansichten ermitteln und Arbeitsbereiche erstellen | Nein |
| [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server) | Programme, Kampagnen, Leads, Smart Lists, E-Mails und Formulare verwalten | [Ja](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server#get-marketo-credentials) |
| [Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/rtcdp-mcp) | Überprüfen des Status der Zielgruppenaktivierung, des Zielstatus und der Datenflussintegrität | Nein |

Eine vollständige Dokumentation finden Sie unter [CX Coworker Gateway](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview).

>[!NOTE]
>
>Der Zugriff auf das Gateway basiert auf den bestehenden CX Enterprise-Anwendungslizenzen Ihres Unternehmens und den Benutzerberechtigungen in Adobe Admin Console. Eine CX Coworker-Lizenz ist nicht erforderlich - Sie benötigen aktive Lizenzen für mindestens eine der CX Enterprise-Anwendungen hinter dem Gateway. Um CX Coworker Gateway für Ihr Unternehmen zu aktivieren, senden Sie eine E-Mail an [cx-coworker-gateway-support@adobe.com](mailto:cx-coworker-gateway-support@adobe.com).

>[!TAB Experience Manager]

Adobe Experience Manager verfügt über mehrere MCP-Server für verschiedene Workflows.

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [AEM Cloud Manager](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Programme, Umgebungen, Pipelines und Repositorys verwalten |
| [AEM-Inhalte](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | Verwalten von Seiten, Inhaltsfragmenten, Assets und Launches |
| [AEM-Inhalt (schreibgeschützt)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | Erkennung und Abfrage von Seiten, Inhaltsfragmenten und Launches ohne Schreibzugriff |
| [AEM Experience Governance](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | Bewertung von Inhalten und Bildern anhand von Markenrichtlinien und Compliance-Regeln |

>[!NOTE]
>
>Der Zugriff auf jede AEM-Umgebung hängt von den Berechtigungen Ihres Unternehmens für AEM Cloud Service und den Benutzerberechtigungen in dieser Umgebung ab.

>[!TAB Experience Platform]

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | Orchestrieren von Zielgruppenanalysen, AEP-Diagnosen und AJO B2B-Journey-Erstellung in allen AEP-Anwendungen |

>[!NOTE]
>
>Der Zugriff hängt von den Adobe Experience Platform-Berechtigungen Ihres Unternehmens und den Berechtigungen Ihres Benutzers ab.

>[!TAB Target]

Adobe Target MCP befindet sich in der öffentlichen Betaversion. Alle derzeit verfügbaren Tools sind schreibgeschützt. Schreib-Tools sind für eine allgemeine Verfügbarkeit geplant.

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Überprüfen von Aktivitäten, Angeboten, Zielgruppen, Mboxes, Leistungsberichten und Vorschau-URLs |

>[!NOTE]
>
>Der Zugriff hängt von Ihren Adobe Target-Berechtigungen und den Berechtigungen Ihrer Benutzenden ab.

>[!TAB Workfront]

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [Adobe Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Arbeiten, Projekte, Planungsdatensätze, Einblicke und Inhaltsgenehmigungen verwalten |

>[!NOTE]
>
>Der Zugriff hängt von Ihren Adobe Workfront-Lizenzen und den Berechtigungen Ihrer Benutzenden ab.

>[!ENDTABS]

## Herstellen einer Verbindung zu Ihrem KI-Client

Die meisten Adobe MCP-Server verwenden OAuth mit Adobe Identity Management Service (IMS). Wählen Sie bei Aufforderung die richtige IMS-Organisation aus. Die Wahl des falschen ist die häufigste Ursache für Authentifizierungsfehler.

![Ein KI-Agent, der eine Verbindung zu einem Adobe MCP-Server herstellt](../assets/hero-connect-mcp-servers.gif)

In den folgenden Schritten wird der Endpunkt „CX Coworker Gateway“ als Beispiel verwendet. Derselbe Prozess gilt für jeden Adobe MCP-Server: Tauschen Sie die Endpunkt-URL gegen den Server aus, zu dem Sie eine Verbindung herstellen möchten.

>[!BEGINTABS]

>[!TAB Claude.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Empfohlen"> Verwenden eines verwalteten Connectors

Wechseln Sie zur [Adobe AI-](https://developer.adobe.com/ai-registry/?type=connector) und suchen Sie nach Ihrer Adobe-Anwendung. Wenn ein Claude-Connector aufgeführt ist (z. B. der [Adobe Experience Manager-Connector](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), befolgen Sie dessen Einrichtungsanweisungen anstelle der folgenden Schritte.

### Verbinden über einen benutzerdefinierten Connector

Claude.ai unterstützt Remote-MCP-Server über benutzerdefinierte Connectoren in den Kontoeinstellungen.

1. Navigieren Sie **Einstellungen > Integrationen**.
2. Klicken Sie **Benutzerdefinierten Connector hinzufügen**.
3. Geben Sie den Server-Endpunkt als URL (z. B. `https://cx-coworker-gateway.adobe.io/mcp` für das CX Coworker Gateway) und einen Anzeigenamen Ihrer Wahl ein.
4. Klicken Sie auf **Verbinden** und melden Sie sich mit Ihrer Adobe ID an. Wählen Sie die richtige IMS-Organisation aus.

Vollständiges Setup: [Claude.ai Custom Connectors-Dokumentation](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Claude Code]

### Verwenden der CLI

Führen Sie `claude mcp add` aus, um einen Adobe MCP-Server zu registrieren. Ersetzen Sie den Servernamen und die URL durch die Werte für den Server, zu dem Sie eine Verbindung herstellen möchten. In diesem Beispiel wird das CX Coworker Gateway verwendet:

```bash
claude mcp add --transport http adobe-cx-coworker-gateway https://cx-coworker-gateway.adobe.io/mcp
```

### Bearbeiten der Einstellungsdatei

Fügen Sie den Server zu `~/.claude.json` (global) oder `.mcp.json` in Ihrem Projektstamm (Projektebene) hinzu. Ersetzen Sie den Schlüssel und die URL durch die Werte für den Server, den Sie verbinden möchten:

```json
{
  "mcpServers": {
    "adobe-cx-coworker-gateway": {
      "type": "http",
      "url": "https://cx-coworker-gateway.adobe.io/mcp"
    }
  }
}
```

Adobe MCP-Server verwenden OAuth. Claude Code fordert Sie auf, sich beim ersten Aufruf eines Tools bei Ihrer Adobe ID zu authentifizieren. Wählen Sie bei Aufforderung die richtige IMS-Organisation aus.

Vollständiges Setup: [Claude Code MCP-Dokumentation](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursor]

Fügen Sie einen Adobe MCP-Server zu Ihrer Cursor `mcp.json`-Konfigurationsdatei hinzu und stellen Sie dann eine Verbindung über **Einstellungen > MCP** her. Ersetzen Sie den Schlüssel und die URL durch die Werte für den Server, zu dem Sie eine Verbindung herstellen möchten. In diesem Beispiel wird das CX Coworker Gateway verwendet:

- **Global (alle Projekte):** `~/.cursor/mcp.json`
- **Projektebene:** `.cursor/mcp.json` im Projektstamm

```json
{
  "mcpServers": {
    "adobe-cx-coworker-gateway": {
      "type": "http",
      "url": "https://cx-coworker-gateway.adobe.io/mcp"
    }
  }
}
```

Nach dem Hinzufügen werden MCP-Server unter **Installierte MCP-Server** in den Cursor-Einstellungen angezeigt. Wählen Sie **Verbinden** neben einem Server aus, der **Authentifizierung** erfordert) anzeigt, und melden Sie sich mit Ihrer Adobe ID an. Wählen Sie die IMS-Organisation aus, die Zugriff auf das Programm hat.

![Cursor-MCP-Server-Konfiguration mit installierten Adobe-MCP-Servern und mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Vollständiges Setup: [Cursor-MCP-Dokumentation](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Empfohlen"> Verwenden eines verwalteten Connectors

Wechseln Sie zur [Adobe AI-](https://developer.adobe.com/ai-registry/?type=connector) und suchen Sie nach Ihrer Adobe-Anwendung. Wenn ein ChatGPT-Connector aufgeführt wird, befolgen Sie die Setup-Anweisungen anstelle der folgenden Schritte.

### Verbindung über Remote-MCP-Server herstellen

ChatGPT unterstützt Remote-MCP-Server über [Entwicklermodus](https://developers.openai.com/api/docs/guides/developer-mode), verfügbar in Pro-, Plus-, Business-, Enterprise- und Education-Plänen.

1. Aktivieren Sie den Entwicklermodus in **ChatGPT-Einstellungen**.
2. Navigieren Sie **Einstellungen > Integrationen**.
3. Klicken Sie **Benutzerdefinierten Connector hinzufügen** und wählen Sie **Remote-MCP-Server**.
4. Geben Sie den Server-Endpunkt als URL (z. B. `https://cx-coworker-gateway.adobe.io/mcp` für das CX Coworker Gateway) und einen Anzeigenamen Ihrer Wahl ein.
5. Legen Sie die Authentifizierung auf **OAuth** fest.
6. Klicken Sie auf **Verbinden** und melden Sie sich mit Ihrer Adobe ID an. Wählen Sie die richtige IMS-Organisation aus.

Vollständiges Setup: [ChatGPT MCP-Dokumentation](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI Codex CLI]

OpenAI Codex CLI unterstützt Remote-MCP-Server über die TOML-Konfiguration.

**Konfigurationsdateispeicherorte:**

- **Benutzerebene (alle Projekte):** `~/.codex/config.toml`
- **Projektumfang:** `.codex/config.toml` im Projektstamm

Ersetzen Sie den Abschnittsnamen und die URL durch die Werte für den Server, zu dem Sie eine Verbindung herstellen möchten. In diesem Beispiel wird das CX Coworker Gateway verwendet:

```toml
[mcp_servers.adobe-cx-coworker-gateway]
url = "https://cx-coworker-gateway.adobe.io/mcp"
enabled = true
```

Adobe MCP-Server verwenden OAuth. Die Codex-CLI verarbeitet den OAuth-Fluss bei der ersten Verwendung automatisch. Wählen Sie bei Aufforderung die richtige IMS-Organisation aus.

Vollständiges Setup: [OpenAI Codex CLI MCP-Dokumentation](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio stellt mithilfe des MCP Onboarding Wizard, der automatisch einen benutzerdefinierten Power Platform-Connector erstellt, eine Verbindung zu Remote-MCP-Servern her.

1. Öffnen Sie den Agenten in Copilot Studio.
2. Navigieren Sie zur Seite **Tools**.
3. Wählen Sie **Tool hinzufügen > Neues Tool > Modellkontext-Protokoll**.
4. Geben Sie im MCP Onboarding-Assistenten die Serverdetails ein. Beispiel: für das CX Coworker Gateway:
   - **Server-Name:** `CX Coworker Gateway`
   - **Server-URL:** `https://cx-coworker-gateway.adobe.io/mcp`
5. Legen Sie die Authentifizierung auf **OAuth 2.0** fest und konfigurieren Sie mit Ihren Adobe IMS-Autorisierungs- und Token-URLs.
6. Wählen **Erstellen** und dann **Zum Agenten hinzufügen**.

>[!NOTE]
>
>MCP-Server-Verbindungen in Copilot Studio durchlaufen Power Platform. Es gelten die DLP-Richtlinien (Data Loss Prevention) Ihres Unternehmens.

Vollständiges Setup: [Copilot Studio MCP-Dokumentation](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## MCP-Server in Aktion

Nutzen Sie das CX Coworker Gateway, um echte Geschäftsprobleme zu lösen. Jede exemplarische Vorgehensweise beginnt mit einer echten betrieblichen Herausforderung und zeigt, wie ein KI-Client sie in einfacher Sprache löst, ohne Tools zu wechseln oder Code zu schreiben.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* ../use-cases/manage-ajo-journeys.md
  {title = Catch journey issues early}
  {description = Monitor active journeys and surface operational issues before they reach your audience.}
  {cta = Monitor your journeys}

* ../use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Close content performance gaps}
  {description = Surface conversion gaps in CJA, trace them to underperforming content in AEM, and apply the fix in a single AI session.}
  {cta = Close performance gaps}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Kampagneneinblicke ohne Berichte">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Kampagneneinblicke ohne Berichte"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" title="Kampagneneinblicke ohne Berichte">Kampagneneinblicke ohne Berichte</a>
                    </p>
                    <p class="is-size-6">Stellen Sie Leistungsfragen in einfacher Sprache und erhalten Sie Antworten von Customer Journey Analytics, ohne einen einzigen Bericht zu erstellen.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Ermitteln von Kampagneneinblicken</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Zielgruppenaktivierung auf einen Blick">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Zielgruppenaktivierung auf einen Blick"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="Zielgruppenaktivierung auf einen Blick">Zielgruppenaktivierung auf einen Blick</a>
                    </p>
                    <p class="is-size-6">Sehen Sie, welche Zielgruppen live sind, wo sie fließen und ob Ziele in Ordnung sind, ohne Real-Time CDP zu navigieren.</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Zielgruppenaktivierung überprüfen</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Catch journey issues early">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Frühzeitiges Erkennen von Journey-Problemen">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="Frühzeitiges Erkennen von Journey-Problemen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" title="Frühzeitiges Erkennen von Journey-Problemen">Erkennen Sie Journey-Probleme frühzeitig</a>
                    </p>
                    <p class="is-size-6">Überwachen Sie aktive Journey und decken Sie betriebliche Probleme auf, bevor sie Ihre Zielgruppe erreichen.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Überwachen Sie Ihre Journey</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Schnellere Bereitstellung von Inhaltsaktualisierungen">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Schnellere Bereitstellung von Inhaltsaktualisierungen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" title="Schnellere Bereitstellung von Inhaltsaktualisierungen">Inhalte werden schneller aktualisiert</a>
                    </p>
                    <p class="is-size-6">Schnelleres Suchen, Aktualisieren und Veröffentlichen von AEM-Seiten und Inhaltsfragmenten, ohne zur AEM-Benutzeroberfläche zu wechseln.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inhalte schneller bereitstellen</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Close content performance gaps">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Schließen von Inhaltsleistungslücken">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Schließen von Inhaltsleistungslücken"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" title="Schließen von Inhaltsleistungslücken">Schließen Sie Lücken bei der Inhaltsleistung</a>
                    </p>
                    <p class="is-size-6">Lücken bei der Oberflächenkonvertierung in CJA aufdecken, diese auf leistungsschwache Inhalte in AEM zurückführen und die Korrektur in einer einzigen KI-Sitzung anwenden.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Schließen Sie Leistungsunterschiede</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Benötigen Sie weitere Hilfe?

MCP-Verbindungen umfassen Authentifizierung, Organisationsauswahl und Berechtigungen auf Anwendungsebene. Wenn etwas nicht wie erwartet funktioniert, decken diese Schritte die häufigsten Ursachen ab.

+++Wechsel zwischen Adobe-Organisationen

Wenn Ihr Adobe-Benutzer mehreren IMS-Organisationen angehört und Sie Tools oder Daten für das falsche sehen, trennen Sie den MCP-Server, melden Sie sich von Ihrer Adobe-Sitzung im Browser ab und stellen Sie dann die Verbindung wieder her. Während der Anmeldung werden Sie aufgefordert, eine Organisation auszuwählen.

Ein Adobe MCP-Server kann jeweils nur für eine IMS-Organisation authentifiziert werden, auch wenn Ihr Benutzerkonto Zugriff auf mehr als ein Konto hat.

+++

+++Angeben einer Sandbox, Report Suite, Umgebung oder einer anderen Sitzungsressource

Bei einigen Adobe MCP-Servern müssen Sie eine Ressource angeben, bevor sie Ergebnisse zurückgeben können. Je nach Programm kann es sich um eine Sandbox, ein Programm, eine Umgebung, eine Report Suite oder eine Datenansicht handeln.

Wenn Sie sich nicht sicher sind, auf welche Ressourcen Sie Zugriff haben, fragen Sie den KI-Client. Beispiel: „Liste der verfügbaren Sandboxes“ oder „Auf welche Report Suites habe ich Zugriff?“ Adobe MCP-Server können häufig eine vollständige Liste der verfügbaren Ressourcen an Ihre Benutzerinnen und Benutzer zurückgeben.

Nachdem eine Sitzungsressource festgelegt wurde, können Sie sie jederzeit wechseln, indem Sie dem KI-Client mitteilen, welche Ressource verwendet werden soll.

+++

+++Berechtigungen und Zugriffsfehler

KI-Clients agieren mithilfe von OAuth im Namen Ihres Adobe-Benutzerkontos. Bei der Verwendung eines MCP-Servers gelten dieselben Berechtigungen und Zugriffssteuerungen wie bei der Anmeldung bei einer Adobe-Anwendung.

Wenn eine Aktion fehlschlägt oder keine Ergebnisse zurückgibt, überprüfen Sie, ob Ihr Benutzer in Adobe Admin Console und in der entsprechenden CX Enterprise-Anwendung über die erforderlichen Berechtigungen verfügt. Wenden Sie sich an Ihren Adobe-Systemadministrator, wenn der Zugriff angepasst werden muss.

+++

+++Erneute Authentifizierung nach einer verlorenen Sitzung

Adobe MCP-Server verwenden OAuth zur Authentifizierung Ihres Adobe-Benutzerkontos. Wenn der Authentifizierungsstatus verloren geht, werden keine weiteren Tool-Aufrufe erfolgreich sein, bis Sie sich erneut authentifizieren.

Erneute Authentifizierung: Öffnen Sie die MCP-Server-Konfiguration Ihres KI-Clients, wählen Sie den Adobe MCP-Server-Eintrag aus und stellen Sie eine neue Verbindung her. Sie werden aufgefordert, sich erneut mit Ihrer Adobe ID anzumelden.

+++
