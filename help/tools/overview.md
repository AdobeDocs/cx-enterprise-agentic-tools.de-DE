---
title: Agent-Tools
description: Vergleichen Sie MCP-Server, Agentenkenntnisse und APIs für Builder und wählen Sie das richtige Agententool für Ihre Adobe CX Enterprise-Workflows aus.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 2%

---


# Agent-Tools

<!-- last-modified: 2026-05-08 -->

Nicht jeder Ansatz mit agenten Werkzeugen erfüllt den gleichen Bedarf. MCP-Server bieten Ihnen sofortigen, natürlichen Sprachzugriff auf Adobe-Daten von jedem kompatiblen KI-Client, ohne dass eine Codierung erforderlich ist. Agent Skills kodieren das Adobe Domain-Know-how in wiederholbare Agent-Workflows, sodass Aufgaben jedes Mal konsistent ausgeführt werden. APIs geben Entwicklern die volle programmgesteuerte Kontrolle über das Erstellen benutzerdefinierter Programme und Integrationen. Auf dieser Seite werden die Kompromisse erläutert, sodass Sie den richtigen Ausgangspunkt für Ihre Situation wählen können.

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

## Magento-Tools vergleichen

| | MCP-Server | Agent-Kenntnisse | APIs für Builder |
| --- | --- | --- | --- |
| Geeignet für | KI-Client-Benutzer | Alle Anwender | Entwickler |
| Kodierung erforderlich | Nein | Nein | Ja |
| Rüstzeit | Minutes | Minutes | Stunden bis Tage |
| Was Sie erhalten | Zugriff auf Adobe über Ihr KI-Tool | Geführte, wiederholbare Workflows | Vollständige programmgesteuerte Steuerung |
| KI-Client erforderlich | Ja | Ja | Optional |

## Nicht sicher, wo man anfangen soll?

- Um mithilfe von KI mit Adobe CX Enterprise-Anwendungen zu interagieren (Aktionen durchführen, Daten abfragen und die KI durch natürliche Konversation ermitteln lassen, was zu tun ist), sind [MCP-Server](mcp-servers.md) der flexibelste Ausgangspunkt.
- Damit Agenten konsistent Adobe-native Workflows ausführen können, ohne zu improvisieren[&#x200B; kodieren &#x200B;](agent-skills.md) diese Domain-Kenntnisse in wiederverwendbaren Anweisungen.
- Um ein fokussiertes Programm zu erstellen, das einen bestimmten Adobe-Workflow für Ihre Benutzerinnen und Benutzer optimiert oder automatisiert, [&#128279;](apis.md) Sie mit APIs für Builder) direkt und programmierbar steuern können, was genau passiert.

>[!BEGINTABS]

>[!TAB MCP-Server]

Stellen Sie sich MCP-Server als eine aktive Verbindung zwischen Ihrem KI-Tool und Adobe vor. Verbinden Sie sich einmal und Ihre KI kann Kampagnen abfragen, Zielgruppen abrufen, den Journey-Status überprüfen und mehr. Alles in einfacher Sprache, kein Code erforderlich.

**MCP-Server verwenden, wenn:**

- Sie möchten Adobe-Daten in dem bereits verwendeten KI-Tool speichern
- Sie führen eine explorative Analyse oder einen Ad-hoc-Datenabruf durch
- Sie möchten schnelle Ergebnisse, ohne ein Projekt zu drehen

**Probieren Sie es aus:** Bitten Sie Claude, Ihre aktiven Journey zusammenzufassen. Rufen Sie die Zielgruppengrößen von Real-Time CDP aus ChatGPT ab. Überprüfen Sie CJA-Kampagnenmetriken, ohne ein Dashboard zu öffnen.

[MCP-Server erkunden](mcp-servers.md)

>[!TAB Agentenfertigkeiten]

Agent-Kenntnisse sind Adobes Domain-Kenntnisse, die als Anweisungen kodiert sind, denen Ihr Agent folgen kann. Anstatt zu hoffen, dass Ihr Agent die richtigen Schritte findet, sagt ihm eine Fähigkeit genau, was zu tun ist. Zuverlässig, wiederholbar und bereits für Adobe-Workflows optimiert.

**Agent-Kenntnisse verwenden, wenn:**

- Sie möchten, dass jedes Mal dieselbe Aufgabe auf die gleiche Weise erledigt wird
- Sie führen wiederholbare Inhalts- oder Medienproduktions-Workflows aus
- Sie möchten einen Agenten, der Adobe kennt, ohne es Ihnen erklären zu müssen

**Probieren Sie es aus:** Bearbeiten Sie einen Satz von Fotos, um zusammenhaltend auszusehen. Erzeugen von plattformfähigen Social-Media-Varianten aus einem Quell-Asset. Entwerfen Sie in wenigen Eingabeaufforderungen aus einer Adobe Express-Vorlage.

[Agent-Kenntnisse entdecken](agent-skills.md)

>[!TAB APIs für Builder]

APIs sind die Bausteine. Sie geben Entwicklerinnen und Entwicklern direkten, programmgesteuerten Zugriff auf Adobe-Daten und -Vorgänge, wobei dieselben APIs verwendet werden, die auch Adobes eigene Produkte unterstützen. Verwenden Sie sie, um etwas zu erstellen, das nach Ihrem Zeitplan, Ihren Bedingungen, Ihrem Stack läuft.

**Verwenden von APIs bei:**

- Sie erstellen ein benutzerdefiniertes Programm oder Dashboard
- Sie müssen Adobe-Daten in ein anderes System integrieren
- Sie verwenden Claude Code oder Cursor, um eine vollständige Anwendung zu generieren
- Sie benötigen die vollständige Kontrolle über Erstellen, Aktualisieren oder Löschen

**Probieren Sie es aus** Erstellen Sie ein benutzerdefiniertes Kampagnen-Dashboard. Automatisieren einer Daten-Pipeline. Generieren Sie eine Anwendung mit Claude-Code, der in Adobe Experience Platform liest und schreibt.

[Erkunden von APIs für Builder](apis.md)

>[!ENDTABS]

## Gemeinsam verwenden

MCP-Server, Agentenkenntnisse und APIs ergänzen sich. Viele Workflows kombinieren alle drei:

- Agent-Kenntnisse definieren den Workflow und leiten den Agenten
- MCP-Server gewähren dem Agenten Lesezugriff auf den Mid-Workflow der Adobe-Daten
- APIs verarbeiten Aktionen, die direkte Systemschreibvorgänge oder benutzerdefinierte Anwendungslogik erfordern
