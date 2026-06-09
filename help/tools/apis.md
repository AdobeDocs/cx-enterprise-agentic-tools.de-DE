---
title: APIs für Builder
description: Erstellen benutzerdefinierter Anwendungen und Integrationen mithilfe von Adobe CX Enterprise-APIs.
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: a130fc470e97f2316e2ea72ebda47b9fc4ad9b33
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 12%

---


# APIs für Builder

<!-- last-modified: 2026-06-02 -->

![Adobe CX Enterprise-APIs](../assets/hero-apis.png)

Adobe CX Enterprise-APIs bieten Entwicklern und Entwicklern von KI-unterstützten Codierungsagenten-Tools direkten Zugriff auf Adobe-Daten und -Workflows. Verwenden Sie sie, um benutzerdefinierte Programme zu erstellen, Integrationen zu automatisieren und Adobe-Funktionen in Ihre eigenen Systeme einzubetten. APIs sind die richtige Wahl, wenn Sie die vollständige programmgesteuerte Kontrolle über eine Systemintegration benötigen oder eine Anwendung auf Adobe-Daten aufbauen. Informationen zum agentengesteuerten, konversativen Zugriff auf Adobe-Workflows finden Sie unter [MCP-Server](mcp-servers.md).

## Adobe CX Enterprise-APIs

>[!BEGINTABS]

>[!TAB Adobe Analytics]

Berichte, Daten-Feeds, berechnete Metriken und Segmentverwaltung.

[Explore API](https://developer.adobe.com/analytics-apis/docs/2.0/)

>[!TAB Adobe Commerce]

REST- und GraphQL-APIs für Katalog, Warenkorb, Bestellungen, Kunden und Promotions.

[Explore API](https://developer.adobe.com/commerce/webapi/)

>[!TAB Adobe Experience Platform]

CRUD-Vorgänge für Datensätze, Schemata, Profile, Identitäten, Abfragen und Segmentierung.

[Explore API](https://developer.adobe.com/experience-platform-apis/)

>[!TAB Adobe Journey Optimizer]

Journey-Orchestrierung, Kampagnenverwaltung, Inhaltsvorlagen und Offer Decisioning.

[Explore API](https://developer.adobe.com/journey-optimizer-apis/)

>[!TAB AEM as a Cloud Service]

Inhalts-, Asset- und Workflow-Management-APIs für Adobe Experience Manager.

[Explore API](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions)

>[!TAB Audience Manager]

Zielgruppen-Management und Aktivierungs-Workflows.

[Explore API](https://developer.adobe.com/audience-manager/)

>[!TAB Client-SDKs]

Mobile SDKs, Edge SDKs und In-App-Messaging.

[Explore API](https://developer.adobe.com/client-sdks/home/)

>[!TAB Customer Journey Analytics]

Workflows für Datenzugriff, Reporting und CJA Insights in Analytics.

[Explore API](https://developer.adobe.com/cja-apis/docs/)

>[!TAB Datenerfassung]

Datenaufnahme, Echtzeit-Ereigniserfassung und Streaming-Datenbereitstellung in Edge Network.

[Explore API](https://developer.adobe.com/data-collection-apis/docs/)

>[!TAB Developer Console]

Einrichtung, Authentifizierung und Verwaltung von API-Projekten.

[Explore API](https://developer.adobe.com/developer-console/docs/guides/)

>[!TAB Ereignisse]

Ereignisgesteuerte Integrationen, Webhooks und Automatisierungs-Trigger.

[Explore API](https://developer.adobe.com/events/docs/)

>[!TAB Datenschutz]

Datenschutz-Workflows, Data Governance und Anfragen von betroffenen Personen.

[Explore API](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/home)

>[!TAB Benutzerverwaltung]

Benutzerverwaltung, Identitätsverwaltung und Automatisierung von Unternehmenskonten.

[Explore API](https://developer.adobe.com/umapi/)

>[!ENDTABS]

## Erstellen mit APIs

![Eine IDE, die eine Verbindung zu Adobe CX Enterprise-APIs herstellt](../assets/hero-connect-apis.gif)

Codierungs-Agenten wie Claude Code, Cursor und OpenAI Codex eignen sich gut für die Erstellung mit Adobe CX Enterprise-APIs. Fügen Sie Ihrem Projekt eine OpenAPI-Spezifikation hinzu, und der Agent kann Endpunkte ermitteln, Anfragen erstellen und Gründe für das API-Verhalten ohne manuelle Verdrahtung angeben. Zunächst benötigen Sie zwei Dinge: authentifizierte Anmeldeinformationen von Adobe Developer Console und API-Dokumentation, die zu Ihrem Projekt hinzugefügt werden.

### Einrichten von API-Anmeldeinformationen in Adobe Developer Console

Der gesamte Zugriff auf die Adobe CX Enterprise API wird über [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) verwaltet. Erstellen Sie ein Projekt, fügen Sie die APIs hinzu, die Ihre Anwendung benötigt, und generieren Sie Anmeldeinformationen.

1. Melden Sie sich an und [erstellen Sie ein Projekt](https://developer.adobe.com/developer-console/docs/guides/projects/) in Adobe Developer Console.
2. [API hinzufügen](https://developer.adobe.com/developer-console/docs/guides/services/) für die benötigte Adobe CX Enterprise-Anwendung.
3. Wählen Sie einen [Authentifizierungstyp](https://developer.adobe.com/developer-console/docs/guides/authentication/). Verwenden Sie **OAuth Server-zu-Server** für automatisierte Workflows oder **OAuth Web App** für Anwendungen mit Benutzerzugriff.
4. Erstellen Sie Ihre Anmeldedaten. Notieren Sie sich die Client-ID, den geheimen Client-Schlüssel und den Token-Endpunkt zur Verwendung in Ihrer Anwendung.

Die meisten Adobe CX Enterprise-APIs erfordern eine Anwendungslizenzierung. Wenn in Ihrem Developer Console-Projekt keine API verfügbar ist, wenden Sie sich an den Adobe-Support.

### Hinzufügen von Adobe-API-Kontext zu Ihrem Projekt

KI-Codierer können Adobe-APIs zuverlässig erkennen und verwenden, wenn Sie das richtige Referenzmaterial zu Ihrem Projekt hinzufügen. Dies funktioniert für jede Adobe CX Enterprise-API, die eine OpenAPI-Spezifikation veröffentlicht.

**1. Suchen Sie die API-Spezifikation**

Durchsuchen Sie die oben aufgeführten [Adobe CX Enterprise](#adobe-cx-enterprise-apis)APIs oder navigieren Sie direkt zum [Adobe Developer-API-Katalog](https://developer.adobe.com/apis).

**2. Laden Sie die OpenAPI-Spezifikation herunter**

Erstellen Sie ein `/specs` in Ihrem Projekt. Laden Sie OpenAPI YAML von der Seite mit den API-Referenzen auf [developer.adobe.com](https://developer.adobe.com/apis) herunter und speichern Sie es dort. Fügen Sie eine `README.md` hinzu, die die Quell-URL und das Download-Datum aufzeichnet.

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>Ein eingecheckter Schnappschuss verleiht Ihrem Codierungsagenten ein stabiles, reproduzierbares Verhalten und macht API-Änderungen in Ihrem Git-Verlauf sichtbar.

**3. API-Index generieren**

Fügen Sie diese Eingabeaufforderung in Ihren Codierungsagenten ein und ersetzen Sie `<API-SPEC-FILE>` durch Ihren Dateinamen:

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. Generieren Sie Agentenanweisungen**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5. Überprüfen**

Bitten Sie den Codierer, eine einfache Aufgabe auszuführen, indem er nur die generierten Dateien verwendet:

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

Wenn der Agent den Vorgang korrekt abschließt, ohne das Verhalten zu erfinden, ist die Einrichtung abgeschlossen.

**Empfohlene Projektstruktur**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**Aktuelle Spezifikationen beibehalten**

Wenn Adobe eine neue API-Version veröffentlicht: Laden Sie einen neuen Schnappschuss in `/specs` herunter, aktualisieren Sie das Datum in `README.md` und generieren Sie den Index und die `AGENTS.md` neu.
