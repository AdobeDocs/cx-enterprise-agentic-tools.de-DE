---
title: Agent-Kenntnisse
description: Von Adobe kuratierte Workflows und Anweisungen, die KI-Agenten durchgängig durch CX Enterprise-Aufgaben führen.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 3%

---


# Agent-Kenntnisse

<!-- last-modified: 2026-05-19 -->

![Agentenkenntnisse für Adobe CX Enterprise](../assets/hero-agent-skills.png)

Agent Skills sind von Adobe kuratierte Workflows, die KI-Agenten schrittweise Anweisungen für die zuverlässige Durchführung von Adobe CX Enterprise-Aufgaben geben. Für jede Agentenkompetenz werden Domain-Kenntnisse und Best Practices kodiert, sodass Agenten konsistente, validierte Ergebnisse erzielen, ohne improvisieren zu müssen. Agent Skills sind sinnvoll, wenn Sie wiederholbares, geführtes Verhalten über Konversationen hinweg wünschen, insbesondere für Aufgaben, die andernfalls jedes Mal eine detaillierte Aufforderung erfordern würden. Sie ergänzen MCP-Server und APIs: Agent Skills definieren, wie ein Agent funktioniert; MCP-Server und APIs bieten den zugrunde liegenden Zugriff.

Alle Agentenkenntnisse werden im [Adobe Skills GitHub-Repository](https://github.com/adobe/skills) verwaltet, das die Hauptquelle für die Dokumentation zu Agentenkenntnissen sowie für Installations- und Implementierungsdetails ist.

## Adobe CX Enterprise Agent - Kenntnisse

Alle Agentenkenntnisse werden im [Adobe Skills GitHub-Repository gepflegt](https://github.com/adobe/skills). Wählen Sie unten einen Funktionsbereich aus, um die Fähigkeiten für diesen Workflow zu erkunden.

### Adobe-Anwendungen

<!--
CARDS

* https://github.com/adobe/skills/tree/main/plugins/aem
  {title = Adobe Experience Manager}
  {description = Agent Skills for Experience Manager development, content, design, and project management across AEM as a Cloud Service, Edge Delivery Services, and AEM 6.5 LTS.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-aem-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-analytics
  {title = Adobe Analytics}
  {description = Agent Skills for KPI monitoring, funnel analysis, and executive reporting workflows in Adobe Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-analytics-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-cja
  {title = Customer Journey Analytics}
  {description = Agent Skills for performance comparison, dimension analysis, and workspace authoring in Customer Journey Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cja-card.png}

* https://github.com/adobe/skills/tree/main/plugins/app-builder
  {title = Adobe App Builder}
  {description = Agent Skills for scaffolding, testing, and deploying custom applications with Adobe App Builder.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cxenterprise-card.png}

* https://github.com/adobe/skills/tree/main/plugins/creative-cloud
  {title = Creative Cloud}
  {description = Agent Skills for batch photo editing, design from templates, video editing, and social media variants with Creative Cloud.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-creative-cloud.png}

-->

Umfassende Informationen zu Kenntnissen, Installationsmethoden und Quell-Code finden Sie im [Adobe Skills GitHub-Repository](https://github.com/adobe/skills).

## Funktionsweise von Agentenfähigkeiten

![Funktionsweise von Agentenkenntnissen](../assets/hero-connect-agent-skills.gif)

Eine Agentenfertigkeit ist ein Satz von Anweisungen, die einem KI-Agenten mitteilen, wie eine Aufgabe mithilfe der Adobe-Agententools abgeschlossen werden soll. Wenn ein Agent eine Qualifikation lädt, folgt dieser Workflow, anstatt zu improvisieren.

- Agenten führen Aufgaben jedes Mal auf die gleiche Weise aus
- Domain-Fachwissen wird einmal kodiert und in allen Konversationen wiederverwendet
- Kenntnisse können mehrere agentische Tools und Aktionen in einem einzigen Workflow verketten

## Erste Schritte

Agent-Kenntnisse werden basierend auf dem verwendeten KI-Client installiert. Einige Clients unterstützen die direkte Installation über die Befehlszeile:

- **Claude-Code**: `/plugin install adobe/skills`
- **Knotenumgebungen**: `npx skills add adobe/skills`
- **GitHub-CLI**: `gh upskill adobe/skills`

Andere Clients erfordern, dass Sie die SKILL-Dateien herunterladen und direkt zu Ihrem KI-Client hinzufügen. In der [Adobe Skills README auf GitHub](https://github.com/adobe/skills#installation) finden Sie vollständige Installationsanweisungen nach Client.

### Ermitteln von Agentenfähigkeiten

Durchsuchen Sie die vollständige Liste der verfügbaren Kenntnisse im [Adobe Skills GitHub-Repository](https://github.com/adobe/skills). Zu jeder Agentenkompetenz gehört eine `SKILL.md` mit detaillierten Anleitungen, Referenzen und Beispielen.

Nach der Installation oder dem Hinzufügen des `adobe/skills` können Sie mit einigen KI-Clients alle verfügbaren Fähigkeiten direkt auflisten:

- **Claude-Code**: `claude /plugin list`
- **Knotenumgebungen**: `npx skills list`
- **GitHub-CLI**: `gh upskill list`

## Agent-Kenntnisse vs. MCP-Server vs. APIs für Builder

| | Agent-Kenntnisse | MCP-Server | APIs für Builder |
| --- | --- | --- | --- |
| Zweck | Geführte Workflows und Best Practices | Zugriff auf Adobe-Daten und -Workflows | Direkte Systemintegration |
| Kodiert das Domain-Fachwissen | Ja | Nein | Nein |
| Kodierung erforderlich | Nein | Nein | Ja |
| Geeignet für | Wiederholbare, geführte Aufgaben | Datenabfragen und Workflow-Aktionen | Entwicklung benutzerdefinierter Anwendungen |
