---
title: Agent-Tools
description: Vergleichen Sie MCP-Server, Agentenkenntnisse und APIs für Builder und wählen Sie das richtige Agententool für Ihre Adobe CX Enterprise-Workflows aus.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 093448ea6a9840d1d2027b76e177b145400a9202
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 1%

---


# Agent-Tools

<!-- last-modified: 2026-06-08 -->

Nicht jedes Agentenwerkzeug erfüllt den gleichen Bedarf. Erfahren Sie, was jeder Einzelne tut, wann er verwendet wird und wie Sie beginnen können - damit Sie den richtigen Ausgangspunkt für Ihre Situation wählen können.

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="mcp-servers.md" title="MCP-Server" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="MCP-Server"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" target="_blank" rel="referrer" title="MCP-Server">MCP-Server</a>
                    </p>
                    <p class="is-size-6">Verbinden eines beliebigen kompatiblen KI-Clients mit Adobe CX Enterprise-Daten und -Workflows. Keine Codierung erforderlich.</p>
                </div>
                <a href="mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden von MCP-Servern</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="Agent-Kenntnisse" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Agent-Kenntnisse"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" target="_blank" rel="referrer" title="Agent-Kenntnisse">Agentenfertigkeiten</a>
                    </p>
                    <p class="is-size-6">Von Adobe kuratierte Workflow-Anweisungen, die Agenten konsistent durch CX Enterprise-Aufgaben führen.</p>
                </div>
                <a href="agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden von Agentenkenntnissen</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="APIs für Builder" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="APIs für Builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="apis.md" target="_blank" rel="referrer" title="APIs für Builder">APIs für Builder</a>
                    </p>
                    <p class="is-size-6">Erstellen Sie benutzerdefinierte Programme und Integrationen mit denselben APIs, die auch für Adobe-Produkte verwendet werden.</p>
                </div>
                <a href="apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden von APIs für Builder</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## Magento-Tools vergleichen

| | MCP-Server | Agent-Kenntnisse | APIs für Builder |
| --- | --- | --- | --- |
| Geeignet für | CX Enterprise-Anwendungsbenutzer | CX Enterprise-Anwendungsbenutzer und -Entwickler | Entwickler |
| Kodierung erforderlich | Nein | Nein | Ja |
| Rüstzeit | Minutes | Minutes | Stunden bis Tage |
| Was Sie erhalten | Zugriff auf CX Enterprise-Anwendungen über Ihre KI-Clients | Geführte, wiederholbare Workflows | Vollständige programmgesteuerte Steuerung |

## Nicht sicher, wo man anfangen soll?

- Um mithilfe von KI mit CX Enterprise-Anwendungen zu interagieren (Aktionen durchführen, Daten abfragen und die KI durch natürliche Konversation ermitteln lassen, was als Nächstes zu tun ist), [MCP-Server](mcp-servers.md) der flexibelste Ausgangspunkt.
- Um sicherzustellen, dass die Agenten die Best Practices von Adobe für CX Enterprise-Workflows befolgen, ohne zu improvisieren, ](agent-skills.md) (Agentenkenntnisse[ diese Domain-Kenntnisse in wiederverwendbaren Anweisungen kodiert.
- Um ein zielgerichtetes Programm zu erstellen, das einen bestimmten CX Enterprise-Workflow für Ihre Benutzer optimiert oder automatisiert, ](apis.md) Sie mit [APIs für Builder) direkt und programmierbar steuern, was genau passiert.

>[!BEGINTABS]

>[!TAB MCP-Server]

Stellen Sie sich MCP-Server als eine aktive Verbindung zwischen Ihrem KI-Client und CX Enterprise-Anwendungen vor. Verbinden Sie sich einmal und Ihre KI kann Kampagnen abfragen, Zielgruppen abrufen, den Journey-Status überprüfen und mehr - alles in einfacher Sprache, ohne Code zu benötigen.

**MCP-Server verwenden, wenn:**

- Sie möchten KI direkt in Ihre CX Enterprise-Workflows integrieren
- Sie möchten CX Enterprise-Daten in dem bereits verwendeten KI-Client
- Sie führen eine explorative Analyse oder einen Ad-hoc-Datenabruf durch
- Sie möchten schnelle Ergebnisse, ohne ein Projekt zu drehen

[MCP-Server erkunden](mcp-servers.md)

>[!TAB Agentenfertigkeiten]

Agent-Kenntnisse sind Adobes Domain-Kenntnisse, die als Anweisungen kodiert sind, denen Ihr Agent folgen kann. Anstatt zu hoffen, dass Ihr Agent die richtigen Schritte findet, sagt ihm eine Fähigkeit genau, was zu tun ist - zuverlässig, wiederholbar und bereits für CX Enterprise-Workflows optimiert.

**Agent-Kenntnisse verwenden, wenn:**

- Sie sollten die Best Practices von Adobe befolgen, wenn Sie über KI-Clients Arbeiten in CX Enterprise-Apps durchführen
- Sie möchten, dass jedes Mal dieselbe Aufgabe auf die gleiche Weise erledigt wird
- Sie führen wiederholbare Inhalts- oder Medienproduktions-Workflows aus

[Agent-Kenntnisse entdecken](agent-skills.md)

>[!TAB APIs für Builder]

APIs sind die Bausteine. Sie geben Entwicklerinnen und Entwicklern direkten, programmgesteuerten Zugriff auf Adobe-Daten und -Vorgänge, wobei dieselben APIs verwendet werden, die auch Adobes eigene Produkte unterstützen. Verwenden Sie sie, um fokussierte benutzerdefinierte Erlebnisse zu erstellen, die bestimmte Geschäfts-Workflows mit den Leitplanken optimieren, die Ihre Organisation benötigt.

**Verwenden von APIs bei:**

- Sie erstellen eine benutzerdefinierte Anwendung oder Integration für einen bestimmten geschäftlichen Anwendungsfall
- Sie müssen einen Workflow mit bestimmten Leitplanken und Steuerelementen optimieren oder automatisieren
- Sie verwenden Claude Code oder Cursor, um eine vollständige Anwendung zu generieren
- Sie müssen CX Enterprise-Daten in ein anderes System integrieren

[Erkunden von APIs für Builder](apis.md)

>[!ENDTABS]

## Gemeinsam verwenden

Diese Tools sind so konzipiert, dass sie zusammenarbeiten - und sie zu kombinieren, ist der Punkt, an dem Sie das meiste aus Adobe AI herausholen. Agent Skills können zeigen, wie ein KI-Client MCP-Server verwendet, um Agenten auf dem richtigen Weg für CX Enterprise-Workflows zu halten. Kenntnisse können auch darüber informieren, wie und wann APIs aufgerufen werden, indem sie Best Practices für Adobe zu benutzerdefinierten Automatisierungen hinzufügen. Man muss sich nicht nur eine aussuchen.
