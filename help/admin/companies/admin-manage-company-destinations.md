---
description: Audience Managers maken, bewerken en verwijderen.
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: Bedrijfsbestemmingen beheren
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# Bedrijfsbestemmingen beheren {#manage-company-destinations}

Audience Managers maken, bewerken en verwijderen.

<!-- t_company_destinations.xml -->

Zie voor meer informatie [Doelen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) in de *Gebruikershandleiding voor Audience Manager*.

## Bedrijfsbestemmingen maken of bewerken {#create-edit-company-destinations}

Doorblader de secties voor geleidelijke instructies op hoe te om nieuw te creëren [!DNL Audience Manager] doelen of bestaande doelen bewerken.

<!-- create-edit-company-destinations.xml -->

Ga naar [Experience Cloud partner integratiepagina](https://wiki.corp.adobe.com/x/mPIMPw) vóór het instellen van doelen. De pagina bevat de specifieke informatie die u voor elke pagina moet invullen [!DNL Audience Manager] partnerintegratie.

Als uw client wilt gebruiken [!DNL Adobe Media Optimizer] als een bestemming in [!DNL Audience Manager] , moet u dit instellen in [!DNL Adobe Media Optimizer].

## Ga naar het tabblad Doelen {#navigate-destinations}

1. Klikken **[!UICONTROL Companies]** en klik vervolgens op het gewenste bedrijf om het [!UICONTROL Profile] pagina. U kunt de [!UICONTROL Search] of de pagineringscontroles bij de bodem van de lijst om het gewenste bedrijf te vinden. U kunt elke kolom in stijgende of dalende orde sorteren door de gewenste kopbal van de kolom te klikken.
1. Klik op de knop **[!UICONTROL Destinations]** tab.
1. Als u een nieuwe bestemming wilt maken, klikt u op **[!UICONTROL Add Destination]**. Als u een bestaand doel wilt bewerken, klikt u op de naam van het doel in het dialoogvenster **[!UICONTROL Name]** kolom.

## Basisinstellingen {#basic-settings}

Vul de velden in de **[!UICONTROL Basic Settings]** venster.

* **[!UICONTROL Name]:** (Vereist) Geef de naam van dit doel op.
* **[!UICONTROL Description]:** Geef beschrijvende informatie op over deze bestemming.
* **[!UICONTROL Type]:** (Vereist) Selecteer het gewenste doeltype:
   * **[!UICONTROL Bulk ID]**: Synchroniseer id&#39;s tussen verschillende platforms.
   * **[!UICONTROL Bulk Trait]**: Verstuur onbewerkte gegevens naar verschillende platforms.
   * **[!UICONTROL Bulk Segment]**: Segmentinformatie bulksgewijs naar verschillende platforms verzenden.
   * **[!UICONTROL S2S]**: Gebruik server-aan-server bestemmingen om gegevens in real time en partijgegevens naar verschillende platforms te verzenden.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] (Alleen) Selecteer een optie:
   * **[!UICONTROL Segment ID]:** Als u deze instelling selecteert, wordt de doelwaardetoewijzing gevuld met de optie [!DNL Audience Manager] Segment-id.
   * **[!UICONTROL Integration Code Value]:** Als u deze instelling selecteert, wordt de doelwaardetoewijzing gevuld met de optie [!DNL Audience Manager] Segmentintegratiecode.
* **[!UICONTROL User ID Key]:** (Vereist) Selecteer de gewenste sleutel van identiteitskaart voor deze bestemming van de drop-down lijst.

Deze id wordt gebruikt als de master gegevensbron-id. Hiermee bepaalt u welke gebruikers-id&#39;s in het bestand worden overtroffen.

>[!NOTE]
>
>Voor de [!UICONTROL Bulk ID] doeltype, kunt u niet het [!DNL Audience Manager] [!UICONTROL User ID] of de [!DNL Adobe Experience Cloud] ID.

Als uw gegevensbron-id ( [!UICONTROL DPID]) niet wordt weergegeven in de vervolgkeuzelijst, moet u de optie **[!UICONTROL Outbound]** Selectievakje op gegevensbronniveau op [Instellingen gegevensbron, pagina](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (Vereist) Selecteer de gewenste gegevensbron voor deze bestemming van de drop-down lijst. Met deze instelling wordt de etikettering van buitenaf gemaakte gegevens ingeschakeld, waardoor inname in afzonderlijke systemen aan de zijde van de client mogelijk is.
* **[!UICONTROL Foreign Account ID]:** Geef de externe account-id voor deze bestemming op. Dit is de identificatiewaarde in het systeem van de ontvanger voor deze outbounded gegevens.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Wanneer de totale hoeveelheid geretourneerde gegevens onbekend is, gebruikt u deze instelling om alleen een voorbeeldhoeveelheid gegevens te retourneren in plaats van de volledige hoeveelheid. Pas hier het getal aan dat een fractie van de gegevens vertegenwoordigt (een waarde &#39;100&#39; retourneert bijvoorbeeld 1/100e van de normale hoeveelheid gegevens, een waarde &#39;10&#39; retourneert een tiende van de normale hoeveelheid gegevens). De standaardwaarde is &#39;1&#39;, die alle gegevens retourneert.

## Realtime-gegevens (voor S2S-bestemmingen) {#realtime-s2s}

Als u een [!UICONTROL S2S] doel, vul de onderstaande velden in:

**[!UICONTROL Servers]**: Selecteer het gewenste `HTTP` server voor dit doel.
**[!UICONTROL Format]**: Selecteer de gewenste indeling voor dit doel in de vervolgkeuzelijst: [!UICONTROL HTTP only].

>[!NOTE]
>
>Voor [!DNL S2S] alleen kunt u een van de [!UICONTROL Realtime] of [!UICONTROL Batch] doelen met de schuifregelaars Op het scherm Uit/Aan. U kunt beide opties niet uitschakelen.

## Batchgegevens {#batch-data}

Voor [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] of [!UICONTROL Bulk Segment] doelen, vul de onderstaande velden in:

* **[!UICONTROL Protocol]**: (Vereist) Selecteer het gewenste protocol voor deze bestemming van de drop-down lijst:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Vereist) Selecteer de gewenste server voor deze bestemming van de drop-down lijst.
* **[!UICONTROL Format]**: (Vereist) Selecteer het gewenste formaat voor deze bestemming van de drop-down lijst: [!DNL HTTP] of bestandstype, afhankelijk van het protocol dat u hierboven hebt gekozen.
* **[!UICONTROL Sync Type]**: (Vereist) Selecteer het gewenste synchronisatietype voor deze bestemming. Dit wijst op het niveau van gebruikersactiviteiten cliënten in de uitgaande orden zouden willen omvatten. Selecteren **[!UICONTROL Customer]** indien cliënten alleen geïnteresseerd zijn in het analyseren van de kwalificaties van de segmenten op basis van hun eigendommen. Selecteren **[!UICONTROL Platform]** als zij de segmentkwalificaties van externe activiteiten in alle sectoren willen opnemen [!DNL Audience Manager] klanten.
* **[!UICONTROL Customer]**: Het bestand bevat actieve gebruikers die alleen op de eigenschappen van de client ten minste één kenmerk hebben (gekoppeld aan de eigenschappen van de client) [!UICONTROL PID]) voor de geselecteerde tijdsperiode. Uw klanten moeten deze optie gebruiken om hun *real-time* segmentkwalificaties naar bestemmingen.
* **[!UICONTROL Platform]**: Het bestand bevat actieve gebruikers met minstens één realtime interactie, of het nu gaat om id-synchronisatie of realisatie van het kenmerk, overal ter wereld [!DNL Audience Manager] de eigenschappen van de cliënten (verbonden aan alle cliëntPIDs) voor de geselecteerde tijdspanne. Uw klanten moeten deze optie gebruiken om hun *totaal* segmentkwalificaties naar bestemmingen.
* **[!UICONTROL Lifetime]**: Bestand bevat actieve gebruikers die overal zichtbaar zijn [!DNL Audience Manager] de eigenschappen van de cliënten sinds de verwezenlijking van de bestemming.
* **[!UICONTROL Sync Type Lookback Period]**: Als u [!UICONTROL Customer] of [!UICONTROL Platform]selecteert u een tijdsperiode. Bestanden bevatten actieve gebruikers voor de geselecteerde tijdsperiode.
Selecteer vervolgens het ordertype. Dit wijst op de frequentie en het werkingsgebied van elke uitgaande integratie met partners. Selecteer tussen incrementele en volledige bestellingen.
* **[!UICONTROL Incremental Scheduled Run]**: Bij elke run, [!DNL Audience Manager] zal slechts de netto nieuwe gebruikers verlaten die sinds de vorige uitgaande orde worden gekwalificeerd. Selecteer de gewenste tijdsperiode [!DNL Audience Manager] om incrementele synchronisatieprocessen uit te voeren. U kunt bijvoorbeeld elke 24 uur selecteren, elke 7 dagen, elke 30 dagen of nooit.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>De eerste incrementele volgorde is gelijk aan een volledige volgorde, omdat er nooit eerder gebruikers naar de bestemming zijn gestuurd.

* **[!UICONTROL Full Sync Scheduled Run]**: Bij elke run, [!DNL Audience Manager] zal alle actieve gebruikers verlaten aangezien de bestemming eerst opstelling was. Selecteer het gewenste schema [!DNL Audience Manager] gebruiken om volledige synchronisatieprocessen uit te voeren. U kunt bijvoorbeeld elke 24 uur selecteren, elke 7 dagen, elke 30 dagen of nooit.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>We raden u aan incrementele syncs vaker te gebruiken dan volledige syncs. Met incrementele syncs worden alleen bestanden verzonden die nieuwe functies of id-syncs bevatten. Met Volledige syntaxis worden alle bestanden verzonden, ongeacht of deze nieuwe realisaties of id-syncs bevatten. Alleen de [!UICONTROL Full Sync Scheduled Run] configuratie wanneer de cliënten een volledig exemplaar van al hun gebruikers nodig hebben, om het uitgaande gegevensvolume te verminderen.

## Gegevensbronnen configureren {#configure-data-sources}

Voor [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] of [!UICONTROL Bulk Segment] doelen, vul de onderstaande velden in. Met deze instellingen kunt u alle gegevens (kenmerken, segmenten of id&#39;s op basis van het geselecteerde type) verzenden die aan de gegevensbronnen zijn gekoppeld.

* **[!UICONTROL All Unrestricted First Party Data]**: Selecteer deze optie om alle gegevensbronnen van de eerste partij te gebruiken. Als u deze optie selecteert, [!UICONTROL Available Data Sources] opties zijn uitgeschakeld.
* **[!UICONTROL Available Data Sources]**: Met de pijlen verplaatst u gegevensbronnen tussen de **[!UICONTROL Available Data Sources]** en **[!UICONTROL In File Data Sources]** vakken.

## Opslaan en voltooien {#save-and-finalize}

De **[!UICONTROL Save]** wordt geactiveerd nadat u alle vereiste velden hebt ingevuld. Klikken **[!UICONTROL Save]** om te voltooien creeer bestemmingsproces.

## Bedrijfsdoelen verwijderen {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Een doel verwijderen:

1. Klikken **[!UICONTROL Companies]**, zoek en klik op het gewenste bedrijf en klik vervolgens op de knop **[!UICONTROL Destinations]** tab.
1. Klikken  ![](assets/icon_delete.png) in de **[!UICONTROL Actions]** kolom van het gewenste doel.
1. Klikken **[!UICONTROL OK]** om de schrapping te bevestigen.

>[!NOTE]
>
>U kunt een doel niet verwijderen als er segmenten aan zijn toegewezen.
