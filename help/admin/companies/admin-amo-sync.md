---
description: Standaard synchroniseren alle bedrijven gegevens met Adobe Media Optimizer (AMO). In Admin UI, heeft elke bedrijfcontainer een gegevensbron die dit proces beheert. Deze gegevensbron is Adobe AMO (ID 411). Klik op een containerrij (onder het tabblad Containers) voor een geselecteerd bedrijf om deze standaardsynchronisatie uit te schakelen of om andere gegevensbronnen aan het AMO-synchronisatieproces toe te voegen en te verwijderen.
seo-description: Standaard synchroniseren alle bedrijven gegevens met Adobe Media Optimizer (AMO). In Admin UI, heeft elke bedrijfcontainer een gegevensbron die dit proces beheert. Deze gegevensbron is Adobe AMO (ID 411). Klik op een containerrij (onder het tabblad Containers) voor een geselecteerd bedrijf om deze standaardsynchronisatie uit te schakelen of om andere gegevensbronnen aan het AMO-synchronisatieproces toe te voegen en te verwijderen.
seo-title: Id's synchroniseren met Media Optimizer
title: Id's synchroniseren met Media Optimizer
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 6%

---


# Id&#39;s synchroniseren met Media Optimizer {#id-syncing-with-media-optimizer}

Standaard synchroniseren alle bedrijven gegevens met [!DNL Adobe Media Optimizer] ([!DNL AMO]). In [!UICONTROL Admin UI], heeft elke bedrijfcontainer een gegevensbron die dit proces beheert. Deze gegevensbron is [!UICONTROL Adobe AMO] ([!UICONTROL ID] 411). Klik op een containerrij (onder het tabblad [!UICONTROL Containers]) voor een geselecteerd bedrijf om deze standaardsynchronisatie uit te schakelen of om andere gegevensbronnen toe te voegen en te verwijderen aan het synchronisatieproces [!DNL AMO].

![](assets/id-sync.png)

## Synchronisatiestatus id {#id-sync-status}

In de volgende tabel wordt de synchronisatiestatus van een gegevensbron beschreven.

| Status | Beschrijving |
|------ | -------- |
| Uit | Verwijder alle gegevensbronnen van [!UICONTROL Selected Data Sources] voor deze container om de synoniemen van identiteitskaart met [!DNL AMO] onbruikbaar te maken |
| Aan (ongeacht versie van de ID-service) | Een gegevensbron synchroniseert met [!DNL AMO], ongeacht de versie van de ID-service wanneer: <ul><li>De gegevensbron wordt weergegeven in de lijst [!UICONTROL Selected Data Sources].</li><li>Het selectievakje [!DNL AMO] *is niet* geselecteerd.</li></ul> |
| Aan (ongeacht versie van de ID-service) | Een gegevensbron synchroniseert met [!DNL AMO] met ID-service versie 2.0 (of hoger) wanneer: <ul><li>De gegevensbron wordt weergegeven in de lijst [!UICONTROL Selected Data Sources].</li><li>Het selectievakje [!DNL AMO] *is* geselecteerd.</li></ul> |

>[!MORELIKETHIS]
>
>* [Containers beheren](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)

