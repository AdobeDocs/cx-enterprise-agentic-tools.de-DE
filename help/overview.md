---
title: Adobe CX Enterprise Agent-Tools
description: Verbinden von KI-Agenten und Entwicklungs-Tools mit Adobe CX Enterprise-Funktionen mithilfe von MCP-Servern, Agent-Kenntnissen und APIs.
index: false
source-git-commit: d6c236f5405fac4b9813280d9fac2d4a60968924
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---


# Adobe CX Enterprise Agent-Tools

<!-- last-modified: 2026-05-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491235/?learn=on&enablevpops)

Stellen Sie Ihrer KI eine direkte Verbindung zu **Daten, Workflows** Automatisierung von Adobe CX Enterprise zur Verfügung. Abfragen von Kampagnen, Aktivieren von Audiences und Verwalten von Journey-**in** Sprache über jeden kompatiblen KI-Client oder Entwicklungs-Tool.

<!--
CARDS

* tools/mcp-servers.md
  {title = MCP Servers}
  {description = Connect any MCP-compatible AI client to Adobe CX Enterprise workflows. Query data, analyze campaigns, and access audiences without leaving your AI tool.}
  {cta = Explore MCP Servers}
  {image = assets/mcp-servers-card.png}

* tools/agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflows that guide agents through CX Enterprise tasks. Domain expertise encoded once, applied consistently.}
  {cta = Explore Agent Skills}
  {image = assets/agent-skills-card.png}

* tools/apis.md
  {title = APIs for Builders}
  {description = Build custom Adobe CX Enterprise applications using agentic coding tools like Claude Code and Cursor.}
  {cta = Explore APIs for Builders}
  {image = assets/apis-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/mcp-servers.md" title="MCP-Server" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="MCP-Server"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" target="_blank" rel="referrer" title="MCP-Server">MCP-Server</a>
                    </p>
                    <p class="is-size-6">Verbinden eines beliebigen MCP-kompatiblen KI-Clients mit Adobe CX Enterprise-Workflows. Abfragen von Daten, Analysieren von Kampagnen und Zugreifen auf Audiences, ohne das KI-Tool verlassen zu müssen.</p>
                </div>
                <a href="tools/mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden von MCP-Servern</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="Agent-Kenntnisse" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="Agent-Kenntnisse"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" target="_blank" rel="referrer" title="Agent-Kenntnisse">Agentenfertigkeiten</a>
                    </p>
                    <p class="is-size-6">Von Adobe kuratierte Workflows, die Agenten durch CX Enterprise-Aufgaben führen. Einmal kodierte Domain-Expertise, konsistent angewendet.</p>
                </div>
                <a href="tools/agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden von Agentenkenntnissen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="APIs für Builder" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="APIs für Builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/apis.md" target="_blank" rel="referrer" title="APIs für Builder">APIs für Builder</a>
                    </p>
                    <p class="is-size-6">Erstellen Sie benutzerdefinierte Adobe CX Enterprise-Anwendungen mit agenten Kodierungstools wie Claude Code und Cursor.</p>
                </div>
                <a href="tools/apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden von APIs für Builder</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Agent-Tools für jedes Team

>[!BEGINTABS]

>[!TAB Business Leaders]

Erfahren Sie mehr über den geschäftlichen Nutzen von Adobe Agent-Tools und wie sich diese auf Ihre Adobe-Investition auswirken.

- Agenten beschleunigen Marketing- und Operations-Workflows, ohne Ihr Team zu ersetzen
- Zugriffssteuerungen, Audit-Trails und Workflows, die von Person zu Person ausgeführt werden, sind von Anfang an integriert
- Agent-Tools funktionieren auf allen kompatiblen KI-Clients, nicht nur auf Adobe-Oberflächen
- Ihre Daten bleiben in Ihrer Umgebung und werden durch Ihre Berechtigungen geregelt.

Unter [Exemplarische Vorgehensweisen für die reale Welt](agentic-tools-in-action.md) erfahren Sie, was Teams heute mit diesen agenten Tools tun.

>[!TAB Geschäftsbenutzer]

Erfahren Sie, wie Agent-Tools Ihre täglichen Adobe-Workflows beschleunigen.

- Verbinden Sie Ihren KI-Client mit Adobe-Daten in Minutenschnelle mit [MCP-Servern](tools/mcp-servers.md)
- Folgen Sie den schrittweisen Anleitungen für häufige [Kampagne](use-cases/analyze-campaign-performance.md), [Audience](use-cases/query-audiences.md) und [Journey](use-cases/manage-ajo-journeys.md)Aufgaben
- Arbeiten in der von Ihnen bereits verwendeten KI-Umgebung

>[!TAB Builder und Entwickler]

Integrieren von Adobe CX Enterprise-Funktionen in benutzerdefinierte Programme und Agenten.

- Durchsuchen Sie [APIs für Builder](tools/apis.md) nach Funktionsbereich und verbinden Sie sich mit [MCP-Servern](tools/mcp-servers.md) in Ihrer Entwicklungsumgebung
- Verwenden Sie KI-unterstützte Kodierungstools wie [Claude Code](https://docs.anthropic.com/en/docs/claude-code/mcp) und [Cursor](https://cursor.com/docs/mcp) zusammen mit Adobe-APIs
- Einrichten der Authentifizierung und der Anmeldeinformationen in der [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)
- Unter [MCP-Server](tools/mcp-servers.md) finden Sie eine vollständige Liste der unterstützten KI-Clients und Installationsanweisungen

>[!TAB Admins]

Verwalten Sie den Zugriff, steuern Sie genehmigte Agent-Tools und behalten Sie die Aufsicht über Ihr gesamtes Unternehmen bei.

- Konfigurieren der Authentifizierung für MCP-Server und APIs über die [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)
- Richten Sie Berechtigungen auf der Ebene der Identity Management-Systeme (IMS) ein, um zu steuern, welche Benutzenden und Teams auf Agententools zugreifen können
- Definieren und Erzwingen, welche KI-Clients und MCP-Server für die Verwendung in Ihrer Organisation genehmigt sind
- Überwachen Sie die Nutzung, überprüfen Sie Audit-Trails und stellen Sie sicher, dass die Agentenaktivität Ihren Compliance-Anforderungen entspricht

Siehe [MCP-Server](tools/mcp-servers.md) für die Authentifizierung und [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) für die Verwaltung von Berechtigungen und Projekten.

>[!ENDTABS]

## Agent-Instrumente in Aktion

Erfahren Sie, wie Adobe CX Enterprise Agent Tools in der Praxis aussehen. Jede exemplarische Vorgehensweise behandelt ein reales Geschäftsszenario vom Setup bis zum Ergebnis und zeigt genau auf, wie ein KI-Client verbunden wird, was gefragt werden soll und was zurückgegeben wird.

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CJA and AEM MCP Servers to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Connect AJO, CJA, and Real-Time CDP in one AI session for a unified view of campaign health.}
  {cta = Start walkthrough}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="Analysieren der Kampagnenleistung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="Analysieren der Kampagnenleistung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analysieren der Kampagnenleistung">Analysieren der Kampagnenleistung</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie das CX Enterprise MCP-Gateway, um Customer Journey Analytics-Metriken und Einblicke von jedem KI-Client zu erhalten.</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/query-audiences.md" title="Audiences abfragen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="Audiences abfragen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" title="Audiences abfragen">Audiences abfragen</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie das CX Enterprise MCP-Gateway, um Zielgruppen- und Zieldaten von Real-Time CDP mit einfachen Eingabeaufforderungen abzufragen.</p>
                </div>
                <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-ajo-journeys.md" title="AJO-Journey überprüfen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="AJO-Journey überprüfen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="AJO-Journey überprüfen">AJO Journey</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie das CX Enterprise MCP-Gateway, um über Ihren KI-Client auf AJO-Journey, den Kampagnenstatus und die Journey-Bedingungen zuzugreifen.</p>
                </div>
                <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="AEM-Inhalte mit KI verwalten" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="AEM-Inhalte mit KI verwalten"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="AEM-Inhalte mit KI verwalten">Verwalten von AEM-Inhalten mit KI</a>
                    </p>
                    <p class="is-size-6">Entdecken, aktualisieren und veröffentlichen Sie Seiten und Inhaltsfragmente in AEM in natürlicher Sprache.</p>
                </div>
                <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/optimize-content-with-performance-data.md" title="Optimieren von Inhalten basierend auf Leistungsdaten" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="Optimieren von Inhalten basierend auf Leistungsdaten"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Optimieren von Inhalten basierend auf Leistungsdaten">Optimieren von Inhalten basierend auf Leistungsdaten</a>
                    </p>
                    <p class="is-size-6">Kombinieren Sie CJA- und AEM-MCP-Server, um leistungsschwache Inhalte zu finden und sie in einer Sitzung zu aktualisieren.</p>
                </div>
                <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/cross-channel-campaign-review.md" title="Ausführen einer Cross-Channel-Kampagnenüberprüfung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="Ausführen einer Cross-Channel-Kampagnenüberprüfung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="Ausführen einer Cross-Channel-Kampagnenüberprüfung">Führen Sie eine kanalübergreifende Kampagnenüberprüfung durch</a>
                    </p>
                    <p class="is-size-6">AJO, CJA und Real-Time CDP in einer KI-Sitzung verbinden, um eine einheitliche Ansicht des Kampagnenzustands zu erhalten.</p>
                </div>
                <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Anleitung starten</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Adobe-Ressourcen

| Ressource | Was Sie finden werden |
| --- | --- |
| [Adobe AI-Registrierung](https://developer.adobe.com/ai-registry/?type=mcp) | Vollständiger Katalog der verfügbaren MCP-Server und Agentenkenntnisse |
| [Adobe API-Katalog](https://developer.adobe.com/apis) | Vollständige Adobe CX Enterprise API-Referenz |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | Einrichten und Authentifizieren von API-Projekten |
| [Experience League](https://experienceleague.adobe.com/de/docs/experience-cloud-ai/experience-cloud-ai/home) | Vollständige Dokumentation und Tutorials zu Adobe-Programmen |
