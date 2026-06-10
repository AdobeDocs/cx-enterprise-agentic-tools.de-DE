---
title: Zuverlässige Bereitstellung für AEM as a Cloud Service
description: Prüfen Sie die Konsistenz der Umgebung, prüfen Sie den Pipeline-Verlauf, prüfen Sie den Trigger oder verwalten Sie Bereitstellungen, ohne Ihren KI-Client verlassen zu müssen.
last-substantial-update: 2026-06-10T00:00:00Z
index: false
source-git-commit: 8735d40a6bee547608a3c0efea7f942b813f2d41
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 2%

---


# Zuverlässige Bereitstellung für AEM as a Cloud Service

<!-- last-modified: 2026-05-21 -->

>[!VIDEO](https://video.tv.adobe.com/v/3480340/?learn=on&enablevpops)

Zuversicht bei der Bereitstellung hängt davon ab, dass Ihre Umgebung in Ordnung ist, bevor Sie Push-Benachrichtigungen senden. In dieser exemplarischen Vorgehensweise wird gezeigt, wie der AEM-Umgebungsstatus überprüft wird, der Pipeline-Verlauf überprüft wird und Trigger-Bereitstellungen von einem KI-Client aus mithilfe des AEM Cloud Manager MCP-Servers ausgeführt werden können, damit Teams schnell arbeiten können, ohne an Sichtbarkeit zu verlieren.

| Szenario-Details | |
| --- | --- |
| CX Enterprise-Anwendungen | [Adobe Experience Manager Cloud Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/introduction-to-cloud-manager) |
| Agent-Tools | [AEM Cloud Manager MCP-Server](https://experienceleague.adobe.com/de/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) |
| Zielgruppe | Entwickler, DevOps, Operations-Teams |
| Voraussetzung | MCP-kompatibler KI-Client, Zugriff auf AEM Cloud Manager |

Jeder Schritt zeigt eine repräsentative Eingabeaufforderung und eine Beispiel-KI-Antwort. Ein **Weitere Eingabeaufforderungen zum**) folgt, um in derselben Sitzung weitere Informationen zu erhalten.

## Voraussetzungen

>[!BEGINTABS]

>[!TAB Claude Code]

Navigieren Sie zuerst zu Ihrem Projektverzeichnis und fügen Sie dann den Cloud Manager MCP-Server über die CLI hinzu:

```bash
claude mcp add --transport http adobe-cloud-manager https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

Oder fügen Sie sie manuell zu `.mcp.json` in Ihrem Projektstamm hinzu:

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Starten Sie den Claude-Code neu. Die Cloud Manager-Tools stehen in Ihrer nächsten Sitzung zur Verfügung.

Vollständiges Setup: [Claude Code MCP-Dokumentation](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursor]

Fügen Sie den Cloud Manager-MCP-Server zu `~/.cursor/mcp.json` (global) oder `.cursor/mcp.json` in Ihrem Projektstamm hinzu:

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Öffnen Sie **Einstellungen > MCP**, wählen Sie **Verbinden** neben dem Server aus und melden Sie sich mit Ihrer Adobe ID an.

Vollständiges Setup: [Cursor-MCP-Dokumentation](https://cursor.com/docs/mcp)

>[!TAB GitHub-Copilot]

Fügen Sie den Cloud Manager-MCP-Server zum `.vscode/mcp.json` in Ihrem Projektstamm hinzu:

```json
{
  "servers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Hinweis: VS-Code verwendet `"servers"` als Schlüssel der obersten Ebene, nicht `"mcpServers"`.

Öffnen Sie das Bedienfeld **GitHub Copilot Chat**, wechseln Sie in den **Agent-Modus** und wählen Sie **Verbinden** neben dem Server aus. MCP-Tools sind nur im Agent-Modus verfügbar.

Vollständiges Setup: [VS Code MCP-Server-Dokumentation](https://code.visualstudio.com/docs/copilot/customization/mcp-servers)

>[!TAB Andere KI-Clients]

Verwenden Sie eine andere MCP-kompatible Umgebung? Stellen Sie mithilfe dieses Endpunkts eine Verbindung zum Cloud Manager MCP-Server her:

```
https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

Vollständige Setup-Anweisungen für alle unterstützten Clients: [Verbinden mit Ihrem KI-Client](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Melden Sie sich bei Aufforderung mit Ihrer Adobe ID an und wählen Sie die mit Ihrem AEM as a Cloud Service-Programm verknüpfte IMS-Organisation aus. Berechtigungen werden auf Cloud Manager-Ebene erzwungen. Ihr KI-Client kann nur Vorgänge ausführen, für die Ihr Konto autorisiert ist.
>
>Bei der ersten Verbindung kann Ihr KI-Client Sie auffordern, Ihr Unternehmen oder AEM-Programm zu bestätigen. Sobald dieser Kontext festgelegt ist, verwendet ihn der MCP-Server für den Rest der Sitzung.
>
>Einige Tools fordern Sie vor der Ausführung zur Genehmigung auf. Überprüfen Sie die vorgeschlagene Aktion und genehmigen oder ablehnen Sie sie. Ohne Ihre Bestätigung wird keine Aktion durchgeführt.

## Schritt 1: Überprüfen des Umgebungsstatus

Bevor Sie eine Version starten, überprüfen Sie, ob Ihre Umgebungen in Ordnung sind und aktiv sind.

```
What is the status of the production environment?
```

+++Siehe eine Beispielantwort

![KI-Client, der den Status der Produktionsumgebung von Cloud Manager anzeigt](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step1-01-ai.png)

+++


## Schritt 2: Pipeline-Ausführungen überprüfen

Lesen Sie den aktuellen Pipeline-Verlauf, um Bereitstellungsmuster und Fehler zu verstehen, bevor sie Ihre nächste Version blockieren.

```
Show me the last five pipeline runs for the production pipeline.
```

+++Siehe eine Beispielantwort

![KI-Client, der die letzten fünf Pipeline-Ausführungen für die Produktions-Pipeline anzeigt](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step2-01-ai.png)

+++


## Schritt 3: Pipeline-Trigger

Starten einer Pipeline-Ausführung direkt von Ihrem KI-Client aus. Der Server bestätigt die Zielumgebung und fordert vor dem Start eine Genehmigung an.

```
Run the Fullstack pipeline against dev environment of WKND sandbox program.
```

+++Siehe eine Beispielantwort

![KI-Client mit Pipeline-Trigger-Bestätigung und Cloud Manager-Benutzeroberfläche, die die laufende Pipeline widerspiegelt](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step3.gif)

+++


>[!CAUTION]
>
>Der KI-Client fordert Sie auf, den Pipeline-Namen zu bestätigen, bevor eine Ausführung ausgelöst wird. Geben Sie den genauen Pipeline-Namen ein, um fortzufahren. Überprüfen Sie die Zielumgebung sorgfältig, bevor Sie sie bestätigen, insbesondere für Pipelines, die in der Produktion bereitgestellt werden.

## Schritt 4: Pipeline-Status überprüfen

Bitten Sie nach dem Auslösen eines Durchgangs Ihren KI-Client um eine Statusaktualisierung, ohne zur Cloud Manager-Oberfläche zu wechseln.

```
What is the status of the triggered pipeline?
```

+++Siehe eine Beispielantwort

![KI-Client, der den Status der ausgelösten Pipeline-Ausführung anzeigt](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step4-01-ai.png)

+++


## Was Sie erreicht haben

Sie haben den AEM Cloud Manager-MCP-Server verwendet, um den Zustand der Umgebung zu überprüfen, den Pipeline-Verlauf zu überprüfen, eine Bereitstellung zu testen und den Trigger zu überprüfen, ohne die Cloud Manager-Benutzeroberfläche zu öffnen. Durch die Kombination von Umgebungstransparenz und Bereitstellungssteuerung in einer einzigen KI-Sitzung können Entwicklungs- und Operations-Teams schneller auf Probleme reagieren und ihren Workflow in den Tools belassen, die sie bereits verwenden.

## Mehr können Sie erreichen

Der Cloud Manager MCP-Server verarbeitet weit mehr als die obige Anleitung behandelt. Erweitern Sie ein unten stehendes Szenario, um Eingabeaufforderungen anzuzeigen, die Sie in derselben Sitzung versuchen können.

+++Probleme erkennen, bevor eine Version veröffentlicht wird

Bereitstellungen schlagen oft aus Gründen fehl, die vor der Ausführung der Pipeline sichtbar waren. Mit diesen Eingabeaufforderungen können Sie den Zustand der Umgebung überprüfen, auf widersprüchliche Ausführungen prüfen und die Versionsausrichtung über Umgebungen hinweg überprüfen, bevor Sie sich zu einer Version verpflichten.

**Eingabeaufforderungen**

```
We're about to kick off a production release. Give me a full status check on all environments first.
```

```
Is there anything currently running in the staging pipeline? I don't want to queue on top of an active run.
```

```
Before I promote main branch to production, confirm main was deployed to Dev and all environments are on the same AEM version.
```

```
What repositories are connected to the WKND program?
```

+++

+++Kurskorrektur - Eine Bereitstellung, die bereits im Flug ist

Ein versehentlicher Trigger oder ein gestopptes Validierungstor kann in eine blockierte Pipeline oder eine unerwünschte Bereitstellung kaskadieren. Mit diesen Eingabeaufforderungen können Sie eine laufende Pipeline abbrechen oder erweitern, ohne zur Cloud Manager-Benutzeroberfläche zu wechseln.

**Eingabeaufforderungen**

```
The staging pipeline kicked off by mistake. Cancel it before it deploys.
```

```
The release pipeline is waiting at the approval gate. Advance it to continue the deployment.
```

+++

+++Grundlegendes zur Erfolgsbilanz bei der Bereitstellung

Wenn Sie wissen, wann etwas erfolgreich war, wie lange Pipelines ausgeführt werden und ob sich Muster ändern, können Sie Versionen planen und die langsame Beeinträchtigung abfangen, bevor sie zu einem Vorfall wird. Verwenden Sie diese Eingabeaufforderungen, um diesen Verlauf bei Bedarf abzurufen.

**Eingabeaufforderungen**

```
What is the status of the last production pipeline execution? If it failed, explain why.
```

```
When was the last successful deployment to the staging environment?
```

```
Our pipeline times are creeping up. What's the longest run we've had in the last 30 days?
```

+++

+++Holen Sie sich einen kaputten Build zurück auf die Spur

Wenn eine Pipeline fehlschlägt, besteht der schnellste Weg zur Lösung darin, genau zu verstehen, wo und warum sie kaputt ging. Dadurch werden Details zu Oberflächenfehlern, Änderungsverlauf und Quality Gate-Problemen angezeigt, sodass Ihr Team Probleme diagnostizieren und beheben kann, ohne die Protokolle manuell durchsuchen zu müssen.

**Eingabeaufforderungen**

```
We're seeing a regression on the live site. What changed in production over the last week?
```

```
Which pipelines have failed in the last 7 days, and at what stage did they fail?
```

```
The last pipeline failed at the code quality step. What specific issues need to be fixed before I can retry?
```

```
Pull the step logs for the last failed run. I need to see exactly what the quality gate flagged.
```

+++


## Weitere Informationen

| Ressource | Was Sie finden werden |
| --- | --- |
| [Dokumentation von AEM as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service){target="_blank"} | Vollständige Dokumentation zu AEM-Programmen |
