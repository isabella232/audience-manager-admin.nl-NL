---
description: Creeer, geef, en schrap de bestemmingen van de Manager van de Publiek uit.
seo-description: Creeer, geef, en schrap de bestemmingen van de Manager van de Publiek uit.
seo-title: Bedrijfsdoelen beheren
title: Bedrijfsdoelen beheren
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Bedrijfsdoelen beheren {#manage-company-destinations}

Creeer, geef, en schrap de bestemmingen van de Manager van de Publiek uit.

<!-- t_company_destinations.xml -->

Voor gedetailleerde informatie, zie [Doelen](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) in de Gids *van de Gebruiker van de Manager van de* Auditie.

## Bedrijfsdoelen maken of bewerken {#create-edit-company-destinations}

De rol door de secties voor geleidelijke instructies op hoe te om nieuwe [!DNL Audience Manager] bestemmingen tot stand te brengen of bestaande bestemmingen uit te geven.

<!-- create-edit-company-destinations.xml -->

Bezoek de pagina [voor de integratie van](https://wiki.corp.adobe.com/x/mPIMPw) Experience Cloud-partners voordat u doelen instelt. De pagina bevat de specifieke informatie die u voor elke [!DNL Audience Manager] partnerintegratie moet invullen.

Als uw klant [!DNL Adobe Media Optimizer] als doel in wilt gebruiken [!DNL Audience Manager] , moet u dit instellen in [!DNL Adobe Media Optimizer].

## Navigate to the Destinations Tab {#navigate-destinations}

1. Klik **[!UICONTROL Companies]**, bepaal de plaats en klik het gewenste bedrijf om zijn [!UICONTROL Profile] pagina te tonen. U kunt het [!UICONTROL Search] vakje of de pagineringscontroles bij de bodem van de lijst gebruiken om het gewenste bedrijf te vinden. U kunt elke kolom in stijgende of dalende orde sorteren door de gewenste kopbal van de kolom te klikken.
1. Klik op het **[!UICONTROL Destinations]** tabblad.
1. Klik op een nieuwe bestemming **[!UICONTROL Add Destination]**. Als u een bestaand doel wilt bewerken, klikt u op de naam van het doel in de **[!UICONTROL Name]** kolom.

## Basisinstellingen {#basic-settings}

Vul de velden in het **[!UICONTROL Basic Settings]** venster in.

* **[!UICONTROL Name]:**(Vereist) Geef de naam van dit doel op.
* **[!UICONTROL Description]:**Geef beschrijvende informatie op over deze bestemming.
* **[!UICONTROL Type]:**(Vereist) Selecteer het gewenste doeltype:
   * **[!UICONTROL Bulk ID]**: Synchroniseer id&#39;s tussen verschillende platforms.
   * **[!UICONTROL Bulk Trait]**: Verstuur onbewerkte gegevens naar verschillende platforms.
   * **[!UICONTROL Bulk Segment]**: Segmentinformatie bulksgewijs naar verschillende platforms verzenden.
   * **[!UICONTROL S2S]**: Gebruik server-aan-server bestemmingen om gegevens in real time en partijgegevens naar verschillende platforms te verzenden.
* **[!UICONTROL Auto-Fill Destination Mapping]:**([!UICONTROL S2S]Alleen) Selecteer een optie:
   * **[!UICONTROL Segment ID]:**Als u deze instelling selecteert, wordt de doelwaardetoewijzing gevuld met de[!DNL Audience Manager]Segment-id.
   * **[!UICONTROL Integration Code Value]:**Als u deze instelling selecteert, wordt de doelwaardetoewijzing gevuld met de[!DNL Audience Manager]segmentintegratiecode.
* **[!UICONTROL User ID Key]:**(Vereist) Selecteer de gewenste sleutel van identiteitskaart voor deze bestemming van de drop-down lijst.

Deze id wordt gebruikt als de hoofd-gegevensbron-id. Hiermee bepaalt u welke gebruikers-id&#39;s in het bestand worden overtroffen.

>[!NOTE]
>
>Voor het [!UICONTROL Bulk ID] bestemmingstype, kunt u niet gebruiken [!DNL Audience Manager] of identiteitskaart [!UICONTROL User ID] [!DNL Adobe Experience Cloud] .

Als uw gegevensbron-id ( [!UICONTROL DPID]) niet in de vervolgkeuzelijst wordt weergegeven, moet u het **[!UICONTROL Outbound]** selectievakje op gegevensbronniveau op de pagina [Instellingen](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)gegevensbron inschakelen.

* **[!UICONTROL Target Data Source]:**(Vereist) Selecteer de gewenste gegevensbron voor deze bestemming van de drop-down lijst. Met deze instelling wordt de etikettering van buitenaf gemaakte gegevens ingeschakeld, waardoor inname in afzonderlijke systemen aan de zijde van de client mogelijk is.
* **[!UICONTROL Foreign Account ID]:**Geef de externe account-id voor deze bestemming op. Dit is de identificatiewaarde in het systeem van de ontvanger voor deze outbounded gegevens.
* **[!UICONTROL Outbound Sample Rate Denominator]:**Wanneer de totale hoeveelheid geretourneerde gegevens onbekend is, gebruikt u deze instelling om alleen een voorbeeldhoeveelheid gegevens te retourneren in plaats van de volledige hoeveelheid. Pas hier het getal aan dat een fractie van de gegevens vertegenwoordigt (een waarde &#39;100&#39; retourneert bijvoorbeeld 1/100e van de normale hoeveelheid gegevens, een waarde &#39;10&#39; retourneert een tiende van de normale hoeveelheid gegevens). De standaardwaarde is &#39;1&#39;, die alle gegevens retourneert.

## Realtime-gegevens (voor S2S-bestemmingen) {#realtime-s2s}

Als u een [!UICONTROL S2S] doel maakt, vult u de onderstaande velden in:

**[!UICONTROL Servers]**: Selecteer de gewenste `HTTP` server voor dit doel.
**[!UICONTROL Format]**: Selecteer de gewenste indeling voor dit doel in de vervolgkeuzelijst: [!UICONTROL HTTP only].

>[!NOTE]
>
>U kunt [!DNL S2S] [!UICONTROL Realtime] [!UICONTROL Batch] alleen doelen of doelen in- of uitschakelen met de schuifregelaars voor Uit/Aan op het scherm. U kunt beide opties niet uitschakelen.

## Batchgegevens {#batch-data}

Vul voor [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] of [!UICONTROL Bulk Segment] bestemmingen de onderstaande velden in:

* **[!UICONTROL Protocol]**: (Vereist) Selecteer het gewenste protocol voor deze bestemming van de drop-down lijst:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Vereist) Selecteer de gewenste server voor deze bestemming van de drop-down lijst.
* **[!UICONTROL Format]**: (Vereist) Selecteer het gewenste formaat voor deze bestemming van de drop-down lijst: of bestandstype, afhankelijk van het protocol dat u hierboven hebt gekozen. [!DNL HTTP]
* **[!UICONTROL Sync Type]**: (Vereist) Selecteer het gewenste synchronisatietype voor deze bestemming. Dit wijst op het niveau van gebruikersactiviteiten cliënten in de uitgaande orden zouden willen omvatten. Selecteer **[!UICONTROL Customer]** als klanten alleen geïnteresseerd zijn in het analyseren van segmentkwalificaties op basis van hun eigenschappen. Selecteer **[!UICONTROL Platform]** als zij segmentkwalificaties van off-site activiteiten over alle [!DNL Audience Manager] klanten willen omvatten.
* **[!UICONTROL Customer]**: Het bestand bevat actieve gebruikers die voor de geselecteerde tijdsperiode ten minste één kenmerk hebben dat alleen kan worden gerealiseerd op de eigenschappen van de client (gekoppeld aan de client [!UICONTROL PID]). Uw cliënten zouden deze optie moeten gebruiken om hun *real-time* segmentkwalificaties aan bestemmingen uit te zenden.
* **[!UICONTROL Platform]**: Het dossier bevat actieve gebruikers die minstens 1 interactie in real time hebben, of het synchroon van identiteitskaart of de verwezenlijking van het bezit, overal over alle eigenschappen van [!DNL Audience Manager] cliënten (verbonden aan alle cliëntPIDs) voor de geselecteerde tijdspanne. Uw cliënten zouden deze optie moeten gebruiken om hun *totale* segmentkwalificaties aan bestemmingen uit te zenden.
* **[!UICONTROL Lifetime]**: Het bestand bevat actieve gebruikers die overal op de eigenschappen van alle [!DNL Audience Manager] clients worden gezien sinds het maken van het doel.
* **[!UICONTROL Sync Type Lookback Period]**: Als u een tijdsperiode selecteert [!UICONTROL Customer] of [!UICONTROL Platform]selecteert. Bestanden bevatten actieve gebruikers voor de geselecteerde tijdsperiode.
Selecteer vervolgens het ordertype. Dit wijst op de frequentie en het werkingsgebied van elke uitgaande integratie met partners. Selecteer tussen incrementele en volledige bestellingen.
* **[!UICONTROL Incremental Scheduled Run]**: Met elke looppas, [!DNL Audience Manager] zal slechts de netto nieuwe gebruikers verlaten die sinds de vorige uitgaande orde worden gekwalificeerd. Selecteer de gewenste tijdsperiode die u incrementele synchronisatieprocessen wilt [!DNL Audience Manager] uitvoeren. U kunt bijvoorbeeld elke 24 uur selecteren, elke 7 dagen, elke 30 dagen of nooit.

>[!NOTE] {Important=&quot;high&quot;}
>
>De eerste incrementele volgorde is gelijk aan een volledige volgorde, omdat er nooit eerder gebruikers naar de bestemming zijn gestuurd.

* **[!UICONTROL Full Sync Scheduled Run]**: Met elke looppas, [!DNL Audience Manager] zal alle actieve gebruikers uitgaand aangezien de bestemming eerst opstelling was. Selecteer het gewenste programma dat u wilt gebruiken [!DNL Audience Manager] om volledige synchronisatieprocessen uit te voeren. U kunt bijvoorbeeld elke 24 uur selecteren, elke 7 dagen, elke 30 dagen of nooit.

>[!NOTE] {Important=&quot;high&quot;}
>
>We raden u aan incrementele syncs vaker te gebruiken dan volledige syncs. Met incrementele syncs worden alleen bestanden verzonden die nieuwe functies of id-syncs bevatten. Met Volledige syntaxis worden alle bestanden verzonden, ongeacht of deze nieuwe realisaties of id-syncs bevatten. Gebruik slechts de [!UICONTROL Full Sync Scheduled Run] configuratie wanneer de cliënten een volledig exemplaar van al hun gebruikers nodig hebben, om het uitgaande gegevensvolume te verminderen.

## Gegevensbronnen configureren {#configure-data-sources}

Vul voor [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] of [!UICONTROL Bulk Segment] doelen de onderstaande velden in. Met deze instellingen kunt u alle gegevens (kenmerken, segmenten of id&#39;s op basis van het geselecteerde type) verzenden die aan de gegevensbronnen zijn gekoppeld.

* **[!UICONTROL All Unrestricted First Party Data]**: Selecteer deze optie om alle gegevensbronnen van de eerste partij te gebruiken. Als u deze optie selecteert, worden de [!UICONTROL Available Data Sources] opties uitgeschakeld.
* **[!UICONTROL Available Data Sources]**: Gebruik de pijlen om gegevensbronnen tussen de **[!UICONTROL Available Data Sources]** vakken en de **[!UICONTROL In File Data Sources]** vakken te verplaatsen.

## Opslaan en voltooien {#save-and-finalize}

De **[!UICONTROL Save]** knop wordt geactiveerd nadat alle vereiste velden zijn ingevuld. Klik **[!UICONTROL Save]** om te voltooien creeer bestemmingsproces.

## Bedrijfsdoelen verwijderen {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

Een doel verwijderen:

1. Klik **[!UICONTROL Companies]**, bepaal de plaats van en klik het gewenste bedrijf, dan klik de **[!UICONTROL Destinations]** tabel.
1. Klik ![](assets/icon_delete.png) in de **[!UICONTROL Actions]** kolom van de gewenste bestemming.
1. Klik **[!UICONTROL OK]** om de verwijdering te bevestigen.

>[!NOTE]
>
>U kunt een doel niet verwijderen als er segmenten aan zijn toegewezen.