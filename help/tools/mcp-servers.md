---
title: MCP-Server
description: Verbinden eines beliebigen MCP-kompatiblen KI-Clients mit Adobe CX Enterprise-Workflows mithilfe von Model Context Protocol-Servern.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 2%

---


# MCP-Server

<!-- last-modified: 2026-05-19 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP-Server bieten jedem kompatiblen KI-Client direkten, gesteuerten Zugriff auf Adobe-Daten und -Workflows. Wenn Sie einmal eine Verbindung herstellen, können Sie die Kampagnenleistung abfragen, Zielgruppen aktivieren, Journey überprüfen, Inhalte verwalten und vieles mehr - alles in einfacher Sprache, ohne Ihre KI-Umgebung verlassen zu müssen. Da sich MCP-Server zwischen Ihrem KI-Client und den zugrunde liegenden Systemen von Adobe befinden, erhalten Sie Flexibilität in natürlicher Sprache, während die Zugriffskontrollen und die Data Governance in Ihrem Unternehmen weiterhin gelten.

Adobe MCP-Server folgen dem Open Model Context Protocol-Standard. Jeder MCP-kompatible KI-Client stellt eine Verbindung zu jedem Adobe MCP-Server her.

## CX Enterprise MCP-Gateway

![Das CX Enterprise MCP Gateway verbindet Ihren KI-Client mit den MCP-Tools der gesamten Adobe CX Enterprise Suite](../assets/mcp-gateway-hero.gif)

**Ein Endpunkt. Jeder Adobe CX Enterprise MCP-Server.**

Das CX Enterprise Gateway leitet Ihren KI-Client zu Tools über Analytics, Kampagnen, Inhalte und Daten hinweg - ohne separate Verbindung für jede Anwendung. Stellen Sie eine Verbindung her, und das Gateway zeigt nur die Tools an, für die Ihr Unternehmen lizenziert ist, basierend auf Ihren Adobe-Berechtigungen.

>[!BEGINTABS]

>[!TAB CX Enterprise-Anwendungen]

Die Tools der einzelnen Programme sind basierend auf den Adobe-Lizenzen Ihres Unternehmens verfügbar.

| Anwendung | Mögliche Optionen |
| --- | --- |
| Adobe Journey Optimizer | [Überprüfen Sie die Journey-, Kampagnen- und Kanalkonfigurationen](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [Berichte abfragen, Datenansichten ermitteln, Arbeitsbereiche erstellen](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [Überprüfen von Zielen, Aktivierungsstatus und Datenflusszustand](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) (geschlossene Beta-Version) |

>[!TAB Verbinden]

Verwenden Sie den CX Enterprise Gateway-Endpunkt überall dort, wo Sie einen anwendungsspezifischen MCP-Endpunkt verwenden würden.

```
https://cx-enterprise.adobe.io/mcp
```

>[!NOTE]
>Verwenden Sie für AEM den direkten AEM-Endpunkt . AEM wird nicht über das CX Enterprise MCP-Gateway geroutet.

Melden Sie sich bei Ihrer Adobe ID an, wenn Sie dazu aufgefordert werden, und wählen Sie die mit Ihren Adobe-Programmen verknüpfte IMS-Organisation aus. Die Wahl der falschen Organisation ist die häufigste Ursache für fehlende Tools oder Authentifizierungsfehler.

Eine vollständige Setup-Anleitung finden Sie [Verbinden mit Ihrem KI-Client](#connect-to-your-ai-client) unten.

>[!ENDTABS]

## Adobe CX Enterprise MCP-Server

Die unten aufgeführten Server stellen eine direkte Verbindung her und werden nicht über das CX Enterprise MCP Gateway geleitet. Verwenden Sie für den Zugriff auf AJO, Customer Journey Analytics und Real-Time CDP das [CX Enterprise MCP Gateway](#cx-enterprise-mcp-gateway) oben.

<!--
CARDS

* #cx-enterprise-mcp-gateway
  {title = CX Enterprise MCP Gateway}
  {description = One connection to AJO, CJA, and Real-Time CDP tools. The gateway surfaces only the tools your organization is licensed for.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/analytics-mcp/docs/aa/
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->

### MCP-Server-Endpunkte

| Server | Endpunkt | Tools |
| --- | --- | --- |
| [CX Enterprise MCP-Gateway](#cx-enterprise-mcp-gateway) | `https://cx-enterprise.adobe.io/mcp` | ・ [Adobe Journey Optimizer-Tools](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>・ [Customer Journey Analytics-Tools](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>・ [Real-Time CDP-Tools](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [Tools anzeigen](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [Tools anzeigen](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [AEM-Inhalte](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [Tools anzeigen](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [AEM-Inhalt (schreibgeschützt)](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [Tools anzeigen](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

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

Führen Sie `claude mcp add` aus, um das CX Enterprise MCP-Gateway zu registrieren. Eine Verbindung bietet Zugriff auf die Tools AJO, CJA und Real-Time CDP, die auf den Lizenzen Ihres Unternehmens basieren.

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

Fügen Sie das CX Enterprise MCP Gateway zu Ihrer Cursor `mcp.json`-Konfigurationsdatei hinzu und stellen Sie dann eine Verbindung über **Einstellungen > MCP** her.

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

Ein Gateway-Eintrag ermöglicht Ihnen Zugriff auf AJO, CJA und Real-Time CDP basierend auf den Lizenzen Ihres Unternehmens.

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

Hinzufügen des CX Enterprise MCP Gateway:

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

## Agent-Instrumente in Aktion

Siehe Adobe CX Enterprise MCP-Server auf echte Unternehmens-Workflows angewendet.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine the CX Enterprise MCP Gateway and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use the CX Enterprise MCP Gateway for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->
