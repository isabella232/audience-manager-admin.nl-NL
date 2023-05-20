---
description: Standaard synchroniseren alle bedrijven gegevens met Adobe Media Optimizer (AMO). In Admin UI, heeft elke bedrijfcontainer een gegevensbron die dit proces beheert. Deze gegevensbron is Adobe AMO (ID 411). Klik op een containerrij (onder het tabblad Containers) voor een geselecteerd bedrijf om deze standaardsynchronisatie uit te schakelen of om andere gegevensbronnen aan het AMO-synchronisatieproces toe te voegen en te verwijderen.
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: Id's synchroniseren met Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 5%

---

# Id&#39;s synchroniseren met Media Optimizer {#id-syncing-with-media-optimizer}

Standaard synchroniseren alle bedrijven gegevens met [!DNL Adobe Media Optimizer] ([!DNL AMO]). In de [!UICONTROL Admin UI], heeft elke bedrijfscontainer een gegevensbron die dit proces beheert. Deze gegevensbron is [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Klik op een containerrij (onder de [!UICONTROL Containers] tab) voor een geselecteerd bedrijf om deze standaardsynchronisatie uit te schakelen of om andere gegevensbronnen toe te voegen aan en te verwijderen uit de [!DNL AMO] synchronisatieproces.

![](assets/id-sync.png)

## Synchronisatiestatus ID {#id-sync-status}

In de volgende tabel wordt de synchronisatiestatus van een gegevensbron beschreven.

| Status | Beschrijving |
|------ | -------- |
| Uit | Alle gegevensbronnen verwijderen uit [!UICONTROL Selected Data Sources] voor deze container om ID-synoniemen uit te schakelen met [!DNL AMO] |
| Aan (ongeacht versie van de ID-service) | Een gegevensbron synchroniseert met [!DNL AMO] ongeacht de versie van de ID-service wanneer: <ul><li>De gegevensbron wordt weergegeven in het dialoogvenster [!UICONTROL Selected Data Sources] lijst.</li><li>De [!DNL AMO] selectievakje *is niet* geselecteerd.</li></ul> |
| Aan (ongeacht versie van de ID-service) | Een gegevensbron synchroniseert met [!DNL AMO] met ID-service versie 2.0 (of hoger) wanneer: <ul><li>De gegevensbron wordt weergegeven in het dialoogvenster [!UICONTROL Selected Data Sources] lijst.</li><li>De [!DNL AMO] selectievakje *is* geselecteerd.</li></ul> |

>[!MORELIKETHIS]
>
>* [Containers beheren](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

