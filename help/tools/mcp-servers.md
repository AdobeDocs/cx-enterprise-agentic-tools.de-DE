---
title: MCP-Server
description: Verbinden eines beliebigen MCP-kompatiblen KI-Clients mit Adobe CX Enterprise-Workflows mithilfe von Model Context Protocol-Servern.
index: false
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: a580957c41e750578b03688bb7ef980103a97781
workflow-type: tm+mt
source-wordcount: '1965'
ht-degree: 3%

---


# MCP-Server

<!-- last-modified: 2026-06-09 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP-Server bieten jedem kompatiblen KI-Client direkten, gesteuerten Zugriff auf Adobe-Daten und -Workflows. Wenn Sie einmal eine Verbindung herstellen, können Sie die Kampagnenleistung abfragen, Zielgruppen aktivieren, Journey überprüfen, Inhalte verwalten und vieles mehr - alles in einfacher Sprache, ohne Ihre KI-Umgebung verlassen zu müssen. Da sich MCP-Server zwischen Ihrem KI-Client und den zugrunde liegenden Systemen von Adobe befinden, erhalten Sie Flexibilität in natürlicher Sprache, während die Zugriffskontrollen und die Data Governance in Ihrem Unternehmen weiterhin gelten.

Adobe MCP-Server folgen dem Open [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro)-Standard. Jeder MCP-kompatible KI-Client stellt eine Verbindung zu jedem Adobe MCP-Server her.

## CX Enterprise MCP-Server

![Das CX Enterprise MCP verbindet Ihren KI-Client mit Tools der gesamten Adobe CX Enterprise Suite](../assets/mcp-gateway-hero.gif)

Wählen Sie eine Anwendung aus, um den Endpunkt und die Funktionen anzuzeigen.

>[!BEGINTABS]

>[!TAB CX Enterprise MCP]

**Ein Endpunkt. Mehrere CX Enterprise-Anwendungen.**

Verbinden Sie sich einmal, und Ihr KI-Client erhält Zugriff auf CX Enterprise-Anwendungen basierend auf den Lizenzen Ihres Unternehmens.

```
https://cx-enterprise.adobe.io/mcp
```

| CX Enterprise-Anwendung | Mögliche Optionen |
| --- | --- |
| Adobe Analytics | Erkennung von Report Suites, Segmenterstellung und Workspace-Erstellung |
| Adobe Experience Platform | Datensatz-Erkennung, Schema-Browsing und Sandbox-Management |
| Adobe Journey Optimizer | Überprüfen von Journey-, Kampagnen- und Kanalkonfigurationen |
| Adobe Journey Optimizer B2B edition | Verwalten von B2B-Journey, Account-Programmen, Einkaufsgruppen und Personalisierung |
| Customer Journey Analytics | Berichte abfragen, Datenansichten ermitteln und Arbeitsbereiche erstellen |
| Real-Time CDP | Überprüfen des Status der Zielgruppenaktivierung, des Zielstatus und der Datenflussintegrität |

>[!NOTE]
>
>Der Zugriff auf jede CX Enterprise-Anwendung basiert auf den Berechtigungen Ihres Unternehmens und den Benutzerberechtigungen in Adobe Admin Console.

>[!TAB Experience Manager]

Adobe Experience Manager verfügt über mehrere MCP-Server für verschiedene Workflows.

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [AEM (Code-Modus)](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | Direkter REST-API-Zugriff auf AEM über Suche, Lesen, Schreiben und Löschen in natürlicher Sprache |
| [AEM Cloud Manager](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Programme, Umgebungen, Pipelines und Repositorys verwalten |
| [AEM-Inhalte](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | Verwalten von Seiten, Inhaltsfragmenten, Assets und Launches |
| [AEM-Inhalt (schreibgeschützt)](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | Erkennung und Abfrage von Seiten, Inhaltsfragmenten und Launches ohne Schreibzugriff |
| [AEM-Dokumenterstellung]&#x200B;(TODO: validate) | `https://mcp.adobeaemcloud.com/adobe/mcp/da` | Verwalten von Dateien, Versionsverlauf und Medienverweisen beim Erstellen von Dokumenten |
| [AEM Experience Governance](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | Bewertung von Inhalten und Bildern anhand von Markenrichtlinien und Compliance-Regeln |
| [AEM Experience Production](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/experience-production/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-production` | Transformieren und Erstellen von AEM-Seiten in großem Maßstab mithilfe von KI-gesteuerten Inhaltsbeschreibungen |

>[!NOTE]
>
>Der Zugriff auf jede AEM-Umgebung hängt von den Berechtigungen Ihres Unternehmens für AEM Cloud Service und den Benutzerberechtigungen in dieser Umgebung ab.

>[!TAB Experience Platform]

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [Adobe Marketing Agent] (TODO: validate) | `https://aep-ai-ama.adobe.io/mcp` | Orchestrieren von Zielgruppenanalysen, AEP-Diagnosen und AJO B2B-Journey-Erstellung in allen AEP-Anwendungen |

>[!NOTE]
>
>Der Zugriff hängt von den Adobe Experience Platform-Berechtigungen Ihres Unternehmens und den Berechtigungen Ihres Benutzers ab.

>[!TAB Marketo Engage]

>[!NOTE]
>
>Marketo Engage MCP verwendet Marketo-native Service-Anmeldeinformationen, nicht Adobe IMS. Anweisungen zur Einrichtung der Authentifizierung finden Sie in der [&#128279;](https://experienceleague.adobe.com/de/docs/marketo-developer/marketo/mcp-server) zum Marketo Engage MCP-Server .

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [Marketo Engage](https://experienceleague.adobe.com/de/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | Programme, Kampagnen, Leads, Smart Lists, E-Mails und Formulare verwalten |

>[!NOTE]
>
>Der Zugriff hängt von Ihrem Marketo Engage-Abonnement und den Berechtigungen Ihres API-Benutzers ab.

>[!TAB Target]

Adobe Target MCP befindet sich in der öffentlichen Betaversion. Alle derzeit verfügbaren Tools sind schreibgeschützt. Schreib-Tools sind für eine allgemeine Verfügbarkeit geplant.

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/de/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Überprüfen von Aktivitäten, Angeboten, Zielgruppen, Mboxes und Leistungsberichten |

>[!NOTE]
>
>Der Zugriff hängt von Ihren Adobe Target-Berechtigungen und den Berechtigungen Ihrer Benutzenden ab.

>[!TAB Workfront]

| MCP-Server | Endpunkt | Mögliche Optionen |
| --- | --- | --- |
| [Adobe Workfront] (TODO: validate) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Arbeiten, Projekte, Planungsdatensätze, Einblicke und Inhaltsgenehmigungen verwalten |

>[!NOTE]
>
>Der Zugriff hängt von Ihren Adobe Workfront-Lizenzen und den Berechtigungen Ihrer Benutzenden ab.

>[!ENDTABS]

## Herstellen einer Verbindung zu Ihrem KI-Client

Alle Adobe MCP-Server verwenden OAuth mit Adobe Identity Management Service (IMS). Wählen Sie bei Aufforderung die richtige IMS-Organisation aus. Die Wahl des falschen ist die häufigste Ursache für Authentifizierungsfehler.

Überprüfen Sie vor der manuellen Konfiguration die [Adobe AI-Registrierung](https://developer.adobe.com/ai-registry/?type=connector) auf einen verwalteten Connector für Ihren KI-Client und Ihre Adobe-Anwendung. Verwaltete Connectoren verarbeiten die Authentifizierung automatisch. Wenn für Ihren Client und Ihre Anwendung ein Connector verfügbar ist, verwenden Sie ihn anstelle der folgenden manuellen Schritte.

![Ein KI-Agent, der eine Verbindung zu einem Adobe MCP-Server herstellt](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB Claude.ai]

### ![Empfohlen](../assets/badge-recommended.svg) Verwenden eines verwalteten Connectors

Wechseln Sie zur [Adobe AI-](https://developer.adobe.com/ai-registry/?type=connector) und suchen Sie nach Ihrer Adobe-Anwendung. Wenn ein Claude-Connector aufgeführt ist (z. B. der [Adobe Experience Manager-Connector](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), befolgen Sie dessen Einrichtungsanweisungen anstelle der folgenden Schritte.

### Verbinden über einen benutzerdefinierten Connector

Claude.ai unterstützt Remote-MCP-Server über benutzerdefinierte Connectoren in den Kontoeinstellungen.

1. Navigieren Sie **Einstellungen > Integrationen**.
2. Klicken Sie **Benutzerdefinierten Connector hinzufügen**.
3. Geben Sie `https://cx-enterprise.adobe.io/mcp` als URL und einen Anzeigenamen wie `Adobe CX Enterprise` ein.
4. Klicken Sie auf **Verbinden** und melden Sie sich mit Ihrer Adobe ID an. Wählen Sie die richtige IMS-Organisation aus.

Vollständiges Setup: [Claude.ai Custom Connectors-Dokumentation](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Claude Code]

### Verwenden der CLI

Führen Sie `claude mcp add` aus, um CX Enterprise MCP zu registrieren. Eine Verbindung ermöglicht den Zugriff auf AJO, CJA und Real-Time CDP basierend auf den Lizenzen Ihres Unternehmens.

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### Bearbeiten der Einstellungsdatei

Fügen Sie den Server zu `~/.claude.json` (global) oder `.mcp.json` in Ihrem Projektstamm (Projektebene) hinzu:

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Adobe MCP-Server verwenden OAuth. Claude Code fordert Sie auf, sich beim ersten Aufruf eines Tools bei Ihrer Adobe ID zu authentifizieren. Wählen Sie bei Aufforderung die richtige IMS-Organisation aus.

Vollständiges Setup: [Claude Code MCP-Dokumentation](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursor]

Fügen Sie CX Enterprise MCP zu Ihrer Cursor `mcp.json`-Konfigurationsdatei hinzu und stellen Sie dann eine Verbindung über **Einstellungen > MCP** her.

- **Global (alle Projekte):** `~/.cursor/mcp.json`
- **Projektebene:** `.cursor/mcp.json` im Projektstamm

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Eine Verbindung ermöglicht den Zugriff auf AJO, CJA und Real-Time CDP basierend auf den Lizenzen Ihres Unternehmens.

Nach dem Hinzufügen werden MCP-Server unter **Installierte MCP-Server** in den Cursor-Einstellungen angezeigt. Wählen Sie **Verbinden** neben einem Server aus, der **Authentifizierung** erfordert) anzeigt, und melden Sie sich mit Ihrer Adobe ID an. Wählen Sie die IMS-Organisation aus, die Zugriff auf das Programm hat.

![Cursor-MCP-Server-Konfiguration mit installierten Adobe-MCP-Servern und mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Vollständiges Setup: [Cursor-MCP-Dokumentation](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### ![Empfohlen](../assets/badge-recommended.svg) Verwenden eines verwalteten Connectors

Wechseln Sie zur [Adobe AI-](https://developer.adobe.com/ai-registry/?type=connector) und suchen Sie nach Ihrer Adobe-Anwendung. Wenn ein ChatGPT-Connector aufgeführt wird, befolgen Sie die Setup-Anweisungen anstelle der folgenden Schritte.

### Verbindung über Remote-MCP-Server herstellen

ChatGPT unterstützt Remote-MCP-Server über [Entwicklermodus](https://developers.openai.com/api/docs/guides/developer-mode), verfügbar in Pro-, Plus-, Business-, Enterprise- und Education-Plänen.

1. Aktivieren Sie den Entwicklermodus in **ChatGPT-Einstellungen**.
2. Navigieren Sie **Einstellungen > Integrationen**.
3. Klicken Sie **Benutzerdefinierten Connector hinzufügen** und wählen Sie **Remote-MCP-Server**.
4. Geben Sie `https://cx-enterprise.adobe.io/mcp` als URL und `Adobe CX Enterprise` als Name ein.
5. Legen Sie die Authentifizierung auf **OAuth** fest.
6. Klicken Sie auf **Verbinden** und melden Sie sich mit Ihrer Adobe ID an. Wählen Sie die richtige IMS-Organisation aus.

Vollständiges Setup: [ChatGPT MCP-Dokumentation](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI Codex CLI]

OpenAI Codex CLI unterstützt Remote-MCP-Server über die TOML-Konfiguration.

**Konfigurationsdateispeicherorte:**

- **Benutzerebene (alle Projekte):** `~/.codex/config.toml`
- **Projektumfang:** `.codex/config.toml` im Projektstamm

CX Enterprise MCP hinzufügen:

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

Adobe MCP-Server verwenden OAuth. Die Codex-CLI verarbeitet den OAuth-Fluss bei der ersten Verwendung automatisch. Wählen Sie bei Aufforderung die richtige IMS-Organisation aus.

Vollständiges Setup: [OpenAI Codex CLI MCP-Dokumentation](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio stellt mithilfe des MCP Onboarding Wizard, der automatisch einen benutzerdefinierten Power Platform-Connector erstellt, eine Verbindung zu Remote-MCP-Servern her.

1. Öffnen Sie den Agenten in Copilot Studio.
2. Navigieren Sie zur Seite **Tools**.
3. Wählen Sie **Tool hinzufügen > Neues Tool > Modellkontext-Protokoll**.
4. Geben Sie im MCP Onboarding-Assistenten Folgendes ein:
   - **Server-Name:** `Adobe CX Enterprise`
   - **Server-URL:** `https://cx-enterprise.adobe.io/mcp`
5. Legen Sie die Authentifizierung auf **OAuth 2.0** fest und konfigurieren Sie mit Ihren Adobe IMS-Autorisierungs- und Token-URLs.
6. Wählen **Erstellen** und dann **Zum Agenten hinzufügen**.

>[!NOTE]
>
>MCP-Server-Verbindungen in Copilot Studio durchlaufen Power Platform. Es gelten die DLP-Richtlinien (Data Loss Prevention) Ihres Unternehmens.

Vollständiges Setup: [Copilot Studio MCP-Dokumentation](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Agent-Instrumente in Aktion

Siehe Adobe CX Enterprise MCP-Server auf echte Unternehmens-Workflows angewendet.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use CX Enterprise MCP to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use CX Enterprise MCP to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CX Enterprise MCP and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use CX Enterprise MCP for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Analysieren der Kampagnenleistung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Analysieren der Kampagnenleistung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analysieren der Kampagnenleistung">Analysieren der Kampagnenleistung</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie CX Enterprise MCP, um Customer Journey Analytics-Metriken und Einblicke von einem beliebigen KI-Client aus darzustellen.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Audiences abfragen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Audiences abfragen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" title="Audiences abfragen">Audiences abfragen</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie CX Enterprise MCP, um Zielgruppen- und Zieldaten von Real-Time CDP mit einfachen Eingabeaufforderungen abzufragen.</p>
                </div>
                <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="AJO-Journey überprüfen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="AJO-Journey überprüfen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="AJO-Journey überprüfen">AJO Journey</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie CX Enterprise MCP, um über Ihren KI-Client auf AJO-Journey, Kampagnenstatus und Journey-Bedingungen zuzugreifen.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="AEM-Inhalte mit KI verwalten" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="AEM-Inhalte mit KI verwalten"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="AEM-Inhalte mit KI verwalten">Verwalten von AEM-Inhalten mit KI</a>
                    </p>
                    <p class="is-size-6">Entdecken, aktualisieren und veröffentlichen Sie Seiten und Inhaltsfragmente in AEM in natürlicher Sprache.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Optimieren von Inhalten basierend auf Leistungsdaten" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Optimieren von Inhalten basierend auf Leistungsdaten"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Optimieren von Inhalten basierend auf Leistungsdaten">Optimieren von Inhalten basierend auf Leistungsdaten</a>
                    </p>
                    <p class="is-size-6">Kombinieren Sie CX Enterprise MCP und AEM Content MCP Server, um leistungsschwache Inhalte zu finden und sie in einer Sitzung zu aktualisieren.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/cross-channel-campaign-review.md" title="Ausführen einer Cross-Channel-Kampagnenüberprüfung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="Ausführen einer Cross-Channel-Kampagnenüberprüfung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="Ausführen einer Cross-Channel-Kampagnenüberprüfung">Führen Sie eine kanalübergreifende Kampagnenüberprüfung durch</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie CX Enterprise MCP, um eine einheitliche Ansicht des AJO-, CJA- und Real-Time CDP-Kampagnenzustands in einer KI-Sitzung zu erhalten.</p>
                </div>
                <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Fehlerbehebung

+++Wechsel zwischen Adobe-Organisationen

Wenn Ihr Adobe-Benutzer mehreren IMS-Organisationen angehört und Sie Tools oder Daten für das falsche sehen, trennen Sie den MCP-Server, melden Sie sich von Ihrer Adobe-Sitzung im Browser ab und stellen Sie dann die Verbindung wieder her. Während der Anmeldung werden Sie aufgefordert, eine Organisation auszuwählen.

Ein Adobe CX Enterprise MCP-Server kann jeweils nur für eine IMS-Organisation authentifiziert werden, auch wenn Ihr Benutzerkonto Zugriff auf mehr als ein Konto hat.

+++

+++Angeben einer Sandbox, Report Suite, Umgebung oder einer anderen Sitzungsressource

Bei einigen Adobe CX Enterprise MCP-Servern müssen Sie eine Ressource angeben, bevor sie Ergebnisse zurückgeben können. Je nach Programm kann es sich um eine Sandbox, ein Programm, eine Umgebung, eine Report Suite oder eine Datenansicht handeln.

Wenn Sie sich nicht sicher sind, auf welche Ressourcen Sie Zugriff haben, fragen Sie den KI-Client. Beispiel: „Liste der verfügbaren Sandboxes“ oder „Auf welche Report Suites habe ich Zugriff?“ Adobe CX Enterprise MCP-Server können häufig eine vollständige Liste der verfügbaren Ressourcen zurückgeben.

Nachdem eine Sitzungsressource festgelegt wurde, können Sie sie jederzeit wechseln, indem Sie dem KI-Client mitteilen, welche Ressource verwendet werden soll.

+++

+++Berechtigungen und Zugriffsfehler

KI-Clients agieren mithilfe von OAuth im Namen Ihres Adobe-Benutzerkontos. Bei der Verwendung eines MCP-Servers gelten dieselben Berechtigungen und Zugriffssteuerungen wie bei der Anmeldung bei einer Adobe-Anwendung.

Wenn eine Aktion fehlschlägt oder keine Ergebnisse zurückgibt, überprüfen Sie, ob Ihr Benutzer in Adobe Admin Console und in der entsprechenden CX Enterprise-Anwendung über die erforderlichen Berechtigungen verfügt. Wenden Sie sich an Ihren Adobe-Systemadministrator, wenn der Zugriff angepasst werden muss.

+++

+++Erneute Authentifizierung nach einer verlorenen Sitzung

Adobe CX Enterprise MCP-Server verwenden OAuth zur Authentifizierung Ihres Adobe-Benutzerkontos. Wenn der Authentifizierungsstatus verloren geht, werden keine weiteren Tool-Aufrufe erfolgreich sein, bis Sie sich erneut authentifizieren.

Um sich erneut zu authentifizieren, öffnen Sie die MCP-Server-Konfiguration Ihres KI-Clients, wählen Sie den MCP-Server-Eintrag für Adobe CX Enterprise aus und verbinden Sie sich erneut. Sie werden aufgefordert, sich erneut mit Ihrer Adobe ID anzumelden.

+++
