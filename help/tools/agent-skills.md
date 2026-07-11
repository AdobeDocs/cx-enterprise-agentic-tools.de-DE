---
title: Agent-Kenntnisse
description: Von Adobe kuratierte Workflows und Anweisungen, die KI-Agenten durchgängig durch CX Enterprise-Aufgaben führen.
last-substantial-update: 2026-05-19T00:00:00Z
source-git-commit: 40d93f878ba9f48c9daffd3beccb4bf829113a36
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 1%

---


# Agent-Kenntnisse

<!-- last-modified: 2026-06-11 -->

![Agentenkenntnisse für Adobe CX Enterprise](../assets/hero-agent-skills.png)

Agent Skills sind von Adobe kuratierte Workflows, die KI-Agenten schrittweise Anweisungen für die zuverlässige Durchführung von Adobe CX Enterprise-Aufgaben geben. Für jede Agentenkompetenz werden Domain-Kenntnisse und Best Practices kodiert, sodass Agenten konsistente, validierte Ergebnisse erzielen, ohne improvisieren zu müssen. Agent Skills sind sinnvoll, wenn Sie wiederholbares, geführtes Verhalten über Konversationen hinweg wünschen, insbesondere für Aufgaben, die andernfalls jedes Mal eine detaillierte Aufforderung erfordern würden. Sie ergänzen MCP-Server und APIs: Agent Skills definieren, wie ein Agent funktioniert; MCP-Server und APIs bieten den zugrunde liegenden Zugriff.

## Adobe CX Enterprise Agent-Kenntnisse

Wählen Sie unten einen Funktionsbereich aus, um die Fähigkeiten für diesen Workflow zu erkunden.

>[!BEGINTABS]

>[!TAB Adobe Experience Manager]

Agent-Kenntnisse für Experience Manager-Entwicklung, -Inhalte, -Design und -Projektmanagement in AEM as a Cloud Service, Edge Delivery Services und AEM 6.5 LTS.

[Agent-Fähigkeiten anzeigen](https://github.com/adobe/skills/tree/main/plugins/aem)

>[!TAB Adobe Analytics]

Agent-Kenntnisse für KPI-Überwachung, funnel-Analyse und Reporting-Workflows in Adobe Analytics.

[Agent-Fähigkeiten anzeigen](https://github.com/adobe/skills/tree/main/plugins/adobe-analytics)

>[!TAB Customer Journey Analytics]

Agent-Kenntnisse für Leistungsvergleich, Dimensionsanalyse und Arbeitsbereich-Authoring in Customer Journey Analytics.

[Agent-Fähigkeiten anzeigen](https://github.com/adobe/skills/tree/main/plugins/adobe-cja)

>[!TAB Adobe App Builder]

Agent-Kenntnisse für Strukturvorlage, Tests und Bereitstellung benutzerdefinierter Anwendungen mit Adobe App Builder.

[Agent-Fähigkeiten anzeigen](https://github.com/adobe/skills/tree/main/plugins/app-builder)

>[!TAB Creative Cloud]

Agentenkenntnisse für die Batch-Fotobearbeitung, das Design aus Vorlagen, die Videobearbeitung und Social-Media-Varianten mit Creative Cloud.

[Agent-Fähigkeiten anzeigen](https://github.com/adobe/skills/tree/main/plugins/creative-cloud)

>[!ENDTABS]

## Agent-Kenntnisse hinzufügen

![Funktionsweise von Agentenkenntnissen](../assets/hero-connect-agent-skills.gif)

Eine Agentenfertigkeit ist ein Satz von Anweisungen, die einem KI-Agenten mitteilen, wie eine Aufgabe mithilfe der Adobe-Agententools abgeschlossen werden soll. Wenn ein Agent eine Qualifikation lädt, folgt dieser Workflow, anstatt zu improvisieren.

### Agent-Kenntnisse installieren

Agent-Kenntnisse werden basierend auf dem verwendeten KI-Client installiert. Einige Clients unterstützen die direkte Installation über die Befehlszeile:

- **Claude-Code**: `/plugin install adobe/skills`
- **Knotenumgebungen**: `npx skills add adobe/skills`
- **GitHub-CLI**: `gh upskill adobe/skills`

Andere Clients erfordern, dass Sie die SKILL-Dateien herunterladen und direkt zu Ihrem KI-Client hinzufügen. In der [Adobe Skills README auf GitHub](https://github.com/adobe/skills#installation) finden Sie vollständige Installationsanweisungen nach Client.

### Agent-Kenntnisse suchen

Durchsuchen Sie die vollständige Liste der verfügbaren Kenntnisse im [Adobe Skills GitHub-Repository](https://github.com/adobe/skills). Zu jeder Agentenkompetenz gehört eine `SKILL.md` mit detaillierten Anleitungen, Referenzen und Beispielen.

Nach der Installation oder dem Hinzufügen des `adobe/skills` können Sie mit einigen KI-Clients alle verfügbaren Fähigkeiten direkt auflisten:

- **Claude-Code**: `claude /plugin list`
- **Knotenumgebungen**: `npx skills list`
- **GitHub-CLI**: `gh upskill list`

## Agent-Fähigkeiten in Aktion

Agent Skills bringen Adobe Domain-Fachwissen in Ihren KI-Client ein, sodass Agenten bewährte Workflows befolgen, anstatt zu improvisieren. Jede der folgenden exemplarischen Vorgehensweisen zeigt eine bestimmte Geschäftsaufgabe, die zuverlässig abgeschlossen wurde und sich von Anfang bis Ende an den Best Practices von Adobe orientiert.

<!--
CARDS

* https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="Entwickeln von AEM-Komponenten mit KI" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Entwickeln von AEM-Komponenten mit KI"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="Entwickeln von AEM-Komponenten mit KI">Entwickeln von AEM-Komponenten mit KI</a>
                    </p>
                    <p class="is-size-6">Verwenden Sie Claude Code oder Cursor mit Agentenkenntnissen, um gemäß den Best Practices von Adobe Strukturvorlagen zu erstellen, zu codieren und AEM-Komponenten zu verfeinern.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Mit Agent-Kenntnissen ausprobieren</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
