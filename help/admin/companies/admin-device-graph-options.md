---
description: De opties voor apparaatgrafiek zijn beschikbaar voor bedrijven die deelnemen aan de Adobe Experience Cloud Device Co-op. Als een klant ook een contractuele relatie heeft met een externe provider van apparaatgrafieken die is geïntegreerd met Audience Manager, worden in deze sectie opties voor die apparaatgrafiek weergegeven. U vindt deze opties in Bedrijven > bedrijfsnaam > Profiel > Opties apparaatgrafiek.
seo-description: De opties voor apparaatgrafiek zijn beschikbaar voor bedrijven die deelnemen aan de Adobe Experience Cloud Device Co-op. Als een klant ook een contractuele relatie heeft met een externe provider van apparaatgrafieken die is geïntegreerd met Audience Manager, worden in deze sectie opties voor die apparaatgrafiek weergegeven. U vindt deze opties in Bedrijven > bedrijfsnaam > Profiel > Opties apparaatgrafiek.
seo-title: Device graph-opties voor bedrijven
title: Device graph-opties voor bedrijven
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 3%

---


# Device graph-opties voor bedrijven {#device-graph-options-for-companies}

Deze [!UICONTROL Device Graph Options] zijn beschikbaar voor bedrijven die aan de [!DNL Adobe Experience Cloud Device Co-op]overeenkomst deelnemen. Als een klant ook een contractuele relatie heeft met een externe provider van apparaatgrafieken die is geïntegreerd met Audience Manager, worden in deze sectie opties voor die apparaatgrafiek weergegeven. U vindt deze opties in [!UICONTROL Companies] > bedrijfsnaam > [!UICONTROL Profile] > [!UICONTROL Device Graph Options].

![](assets/adminUIdataSource.png)

Deze illustratie gebruikt generieke namen voor de grafiekopties van apparaten van derden. In productie, komen deze namen uit de leverancier van de apparatengrafiek en kunnen van wat variëren hier wordt getoond. De [!DNL LiveRamp] opties zijn bijvoorbeeld gewoonlijk (maar niet altijd):

* Beginnen met &quot;[!DNL LiveRamp]&quot;
* Bevat een variërende middelste naam
* Einde met &quot;[!UICONTROL - Household]&quot; of &quot;[!UICONTROL -Person]&quot;

## Apparaatgrafiekopties gedefinieerd {#device-graph-options-defined}

Met de opties voor apparaatgrafieken die u hier selecteert, worden de [!UICONTROL Device Options] keuzes die beschikbaar zijn voor een [!DNL Audience Manager] klant, onthuld of verborgen wanneer deze een [!UICONTROL Profile Merge Rule].

### Afbeelding van apparaat voor coop {#co-op-graph}

Klanten die deelnemen aan de [Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/en_US/mcdc/) gebruiken deze opties om een [!UICONTROL Profile Merge Rule] met [deterministische en probabilistische gegevens](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html)te maken. De [!DNL Corporate Provisioning Team] activeert en desactiveert deze optie via een achterste-eind [!DNL API] vraag. U kunt deze vakken niet in de [!DNL Admin UI]lijst in- of uitschakelen. De opties **[!UICONTROL Co-op Device Graph]** en **[!UICONTROL Company Device Graph]** opties sluiten elkaar ook uit. Klanten kunnen ons vragen het ene of het andere te activeren, maar niet beide. Als deze optie is ingeschakeld, wordt het **[!UICONTROL Co-op Device Graph]** besturingselement in de [!UICONTROL Device Options] instellingen voor een [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### Bedrijfsapparaatgrafiek {#company-graph}

Deze optie is voor [!DNL Analytics] klanten die [!UICONTROL People] metrisch in hun [!DNL Analytics] rapportreeks gebruiken. De [!DNL Corporate Provisioning Team] activeert en desactiveert deze optie via een achterste-eind [!DNL API] vraag. U kunt deze vakken niet in de [!DNL Admin UI]lijst in- of uitschakelen. De opties **[!UICONTROL Company Device Graph]** en **[!UICONTROL Co-op Device Graph]** opties sluiten elkaar ook uit. Klanten kunnen ons vragen het ene of het andere te activeren, maar niet beide. Indien ingeschakeld:

* Deze apparatengrafiek gebruikt deterministische gegevens die tot het bedrijf behoren u (geen probabilistische gegevens) vormt.
* [!DNL Audience Manager] leidt automatisch tot een [!UICONTROL Data Source] genoemd `*`partnernaam`*-Company Device Graph-Person`. In de [!UICONTROL Data Source] detailspagina, kunnen de [!DNL Audience Manager] klanten de partnernaam, beschrijving veranderen, en de Controles [van de Uitvoer van](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) Gegevens op deze gegevensbron toepassen.
* [!DNL Audience Manager] klanten *zien geen* nieuwe instelling in de [!UICONTROL Device Options] sectie voor een [!UICONTROL Profile Merge Rule].

### Grafiek LiveRamp-apparaat (persoonlijk of in het huishouden) {#liveramp-device-graph}

Deze controledozen worden toegelaten in de [!DNL Admin UI] wanneer een partner creeert [!UICONTROL Data Source] en selecteert **[!UICONTROL Use as an Authenticated Profile]** en/of **[!UICONTROL Use as a Device Graph]**. De namen voor deze instellingen worden bepaald door de externe provider van apparaatgrafieken (bijvoorbeeld, [!DNL LiveRamp], [!DNL TapAd]enz.). Als deze optie is ingeschakeld, betekent dit dat het bedrijf dat u configureert, gegevens zal gebruiken die door deze apparaatgrafieken worden verschaft.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [Definities van opties voor regels voor profielsamenvoeging](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html).
>* [Instellingen gegevensbron en menuopties](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)

