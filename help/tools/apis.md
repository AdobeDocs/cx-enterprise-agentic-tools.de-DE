---
title: APIs für Builder
description: Erstellen benutzerdefinierter Anwendungen und Integrationen mithilfe von Adobe CX Enterprise-APIs.
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: 093448ea6a9840d1d2027b76e177b145400a9202
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 24%

---


# APIs für Builder

<!-- last-modified: 2026-06-02 -->

![Adobe CX Enterprise-APIs](../assets/hero-apis.png)

Adobe CX Enterprise-APIs bieten Entwicklern und Entwicklern von KI-unterstützten Codierungsagenten-Tools direkten Zugriff auf Adobe-Daten und -Workflows. Verwenden Sie sie, um benutzerdefinierte Programme zu erstellen, Integrationen zu automatisieren und Adobe-Funktionen in Ihre eigenen Systeme einzubetten. APIs sind die richtige Wahl, wenn Sie die vollständige programmgesteuerte Kontrolle über eine Systemintegration benötigen oder eine Anwendung auf Adobe-Daten aufbauen. Informationen zum agentengesteuerten, konversativen Zugriff auf Adobe-Workflows finden Sie unter [MCP-Server](mcp-servers.md).

## Adobe CX Enterprise-APIs

Adobe CX Enterprise-APIs stellen die Kerndaten und -vorgänge bereit, auf denen Produkte wie Adobe Experience Platform, Journey Optimizer und Customer Journey Analytics basieren. Jede API folgt einem API-First-Design, das Entwickelnden und KI-unterstützten Codierungsagenten-Tools direkten, programmierbaren Zugriff auf dieselben Funktionen gewährt, die Adobe intern verwendet. Verwenden Sie sie, um benutzerdefinierte Programme zu erstellen, Workflows zu automatisieren und Adobe-Daten in Ihre eigenen Systeme zu integrieren.

<!--
CARDS

* https://developer.adobe.com/audience-manager/
  {title = Audience Manager}
  {description = Audience management and activation workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aam-card.png}

* https://developer.adobe.com/client-sdks/home/
  {title = Client SDKs}
  {description = Mobile SDKs, edge SDKs, and in-app messaging.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/cja-apis/docs/
  {title = Customer Journey Analytics}
  {description = Analytics data access, reporting, and CJA insights workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cja-card.png}

* https://developer.adobe.com/data-collection-apis/docs/
  {title = Data Collection}
  {description = Edge Network data ingestion, real-time event collection, and streaming data delivery.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/developer-console/docs/guides/
  {title = Developer Console}
  {description = API project setup, authentication, and credential management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/events/docs/
  {title = Events}
  {description = Event-driven integrations, webhooks, and automation triggers.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://experienceleague.adobe.com/en/docs/experience-platform/privacy/home
  {title = Privacy}
  {description = Privacy workflows, data governance, and data subject requests.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/experience-platform-apis/
  {title = Adobe Experience Platform}
  {description = CRUD operations for datasets, schemas, profiles, identities, queries, and segmentation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/journey-optimizer-apis/
  {title = Adobe Journey Optimizer}
  {description = Journey orchestration, campaign management, content templates, and offer decisioning.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-ajo-card.png}

* https://developer.adobe.com/analytics-apis/docs/2.0/
  {title = Adobe Analytics}
  {description = Reporting, data feeds, calculated metrics, and segment management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions
  {title = AEM as a Cloud Service}
  {description = Content, asset, and workflow management APIs for Adobe Experience Manager.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aem-card.png}

* https://developer.adobe.com/commerce/webapi/
  {title = Adobe Commerce}
  {description = REST and GraphQL APIs for catalog, cart, orders, customers, and promotions.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-commerce-card.png}

* https://developer.adobe.com/umapi/
  {title = User Management}
  {description = User management, identity administration, and enterprise account automation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience Manager">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/audience-manager/" title="Audience Manager" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-aam-card.png" alt="Audience Manager"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/audience-manager/" target="_blank" rel="referrer" title="Audience Manager">Audience Manager</a>
                    </p>
                    <p class="is-size-6">Zielgruppen-Management und Aktivierungs-Workflows.</p>
                </div>
                <a href="https://developer.adobe.com/audience-manager/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Client SDKs">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/" title="Client-SDKs" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-cxenterprise-card.png" alt="Client-SDKs"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/" target="_blank" rel="referrer" title="Client-SDKs">Client-SDKs</a>
                    </p>
                    <p class="is-size-6">Mobile SDKs, Edge SDKs und In-App-Messaging.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Customer Journey Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/cja-apis/docs/" title="Customer Journey Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-cja-card.png" alt="Customer Journey Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/cja-apis/docs/" target="_blank" rel="referrer" title="Customer Journey Analytics">Customer Journey Analytics</a>
                    </p>
                    <p class="is-size-6">Workflows für Datenzugriff, Reporting und CJA Insights in Analytics.</p>
                </div>
                <a href="https://developer.adobe.com/cja-apis/docs/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Data Collection">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/data-collection-apis/docs/" title="Datenerfassung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-aep-card.png" alt="Datenerfassung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/data-collection-apis/docs/" target="_blank" rel="referrer" title="Datenerfassung">Datenerfassung</a>
                    </p>
                    <p class="is-size-6">Datenaufnahme, Echtzeit-Ereigniserfassung und Streaming-Datenbereitstellung in Edge Network.</p>
                </div>
                <a href="https://developer.adobe.com/data-collection-apis/docs/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Developer Console">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/developer-console/docs/guides/" title="Developer Console" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-cxenterprise-card.png" alt="Developer Console"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/developer-console/docs/guides/" target="_blank" rel="referrer" title="Developer Console">Developer Console</a>
                    </p>
                    <p class="is-size-6">Einrichtung, Authentifizierung und Verwaltung von API-Projekten.</p>
                </div>
                <a href="https://developer.adobe.com/developer-console/docs/guides/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Events">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/events/docs/" title="Ereignisse" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-cxenterprise-card.png" alt="Ereignisse"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/events/docs/" target="_blank" rel="referrer" title="Ereignisse">Ereignisse</a>
                    </p>
                    <p class="is-size-6">Ereignisgesteuerte Integrationen, Webhooks und Automatisierungs-Trigger.</p>
                </div>
                <a href="https://developer.adobe.com/events/docs/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Privacy">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/de/docs/experience-platform/privacy/home" title="Datenschutz" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-aep-card.png" alt="Datenschutz"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/de/docs/experience-platform/privacy/home" target="_blank" rel="referrer" title="Datenschutz">Datenschutz</a>
                    </p>
                    <p class="is-size-6">Datenschutz-Workflows, Data Governance und Anfragen von betroffenen Personen.</p>
                </div>
                <a href="https://experienceleague.adobe.com/de/docs/experience-platform/privacy/home" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Platform">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/experience-platform-apis/" title="Adobe Experience Platform" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-aep-card.png" alt="Adobe Experience Platform"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/experience-platform-apis/" target="_blank" rel="referrer" title="Adobe Experience Platform">Adobe Experience Platform</a>
                    </p>
                    <p class="is-size-6">CRUD-Vorgänge für Datensätze, Schemata, Profile, Identitäten, Abfragen und Segmentierung.</p>
                </div>
                <a href="https://developer.adobe.com/experience-platform-apis/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/journey-optimizer-apis/" title="Adobe Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-ajo-card.png" alt="Adobe Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank" rel="referrer" title="Adobe Journey Optimizer">Adobe Journey Optimizer</a>
                    </p>
                    <p class="is-size-6">Journey-Orchestrierung, Kampagnenverwaltung, Inhaltsvorlagen und Offer Decisioning.</p>
                </div>
                <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/analytics-apis/docs/2.0/" title="Adobe Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-analytics-card.png" alt="Adobe Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/analytics-apis/docs/2.0/" target="_blank" rel="referrer" title="Adobe Analytics">Adobe Analytics</a>
                    </p>
                    <p class="is-size-6">Berichte, Daten-Feeds, berechnete Metriken und Segmentverwaltung.</p>
                </div>
                <a href="https://developer.adobe.com/analytics-apis/docs/2.0/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Commerce">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/commerce/webapi/" title="Adobe Commerce" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-commerce-card.png" alt="Adobe Commerce"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/commerce/webapi/" target="_blank" rel="referrer" title="Adobe Commerce">Adobe Commerce</a>
                    </p>
                    <p class="is-size-6">REST- und GraphQL-APIs für Katalog, Warenkorb, Bestellungen, Kunden und Promotions.</p>
                </div>
                <a href="https://developer.adobe.com/commerce/webapi/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="User Management">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/umapi/" title="Benutzerverwaltung" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-cxenterprise-card.png" alt="Benutzerverwaltung"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/umapi/" target="_blank" rel="referrer" title="Benutzerverwaltung">Benutzerverwaltung</a>
                    </p>
                    <p class="is-size-6">Benutzerverwaltung, Identitätsverwaltung und Automatisierung von Unternehmenskonten.</p>
                </div>
                <a href="https://developer.adobe.com/umapi/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Erkunden der API</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## APIs für Builder vs. MCP-Server

Verwenden Sie APIs, wenn Sie die Systemintegration vollständig steuern müssen oder ein benutzerdefiniertes Programm erstellen möchten. Verwenden Sie MCP-Server, wenn ein KI-Agent direkt mit Adobe-Workflows arbeiten soll.

| | APIs | MCP-Server |
| --- | --- | --- |
| Direkte Systemintegration | Ja | manchmal |
| Agent-freundliche Orchestrierung | Limited | Ja |
| Zugriff auf Rohdaten | Ja | Gewöhnlich abstrahiert |
| Entwicklung benutzerdefinierter Anwendungen | Primärer Anwendungsfall | Sekundär |
| KI-unterstützte Workflows | „Unterstützt“ | Primärer Anwendungsfall |

## Erste Schritte mit APIs für Builder

![Eine IDE, die eine Verbindung zu Adobe CX Enterprise-APIs herstellt](../assets/hero-connect-apis.gif)

Bevor Sie Adobe CX Enterprise-APIs erstellen können, sind zwei Dinge erforderlich: authentifizierte Anmeldeinformationen von Adobe Developer Console und API-Dokumentation, die Ihrem Projekt hinzugefügt werden, damit Ihr Codierungsagent zuverlässig mit Adobe-APIs arbeiten kann.

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
