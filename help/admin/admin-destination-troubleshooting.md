---
description: Informatie om u te helpen plaatsingsbestemmingen in Audience Manager en gemeenschappelijke problemen te vermijden.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: Problemen bij het instellen van bestemmingen oplossen
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 2%

---

# Problemen bij het instellen van bestemmingen oplossen {#destination-setup-troubleshooting}

Informatie om u te helpen plaatsingsbestemmingen in Audience Manager en gemeenschappelijke problemen te vermijden.

## Ik heb een bestemming ingesteld, maar ik zie geen bestanden. Waar zijn ze? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

De gemeenschappelijke problemen van de bestemmingsconfiguratie omvatten de volgende kwesties:

### Misconfigured Doel

* **Onjuist [!UICONTROL UserID] Sleutel:** De [!UICONTROL UserID] key is the [!UICONTROL MasterDPID] van deze bestemming en vormt de basis voor de id-waarden die worden overschreden. Zelfs als een [!UICONTROL UserID] De sleutel is selecteerbaar via de drop-down lijst, het betekent niet noodzakelijk dat er IDs/traits/segmenten aan deze waarde in kaart worden gebracht. Als de [!UICONTROL Outbound] Het proces (dat loopt nadat doelen zijn gemaakt) vindt geen gebruikers die aan dit proces zijn toegewezen [!UICONTROL UserID] key, er worden geen gegevens overtroffen.
* **Nee in geselecteerde bestandsgegevensbronnen:** Wanneer u een ander doeltype kiest dan [!UICONTROL S2S], verschijnt een sectie onder aan het scherm met het label [!UICONTROL Configure Data Sources]. Wanneer deze sectie voor het eerst wordt weergegeven, worden geen waarden geselecteerd. Als u bent vergeten op de knop [!UICONTROL All First Party] Schakel het selectievakje of selecteer afzonderlijk gegevensbronnen in het dialoogvenster [!UICONTROL Available Data Sources] venster, worden er geen gegevens overtroffen.

### Misconfigured Formaat

Wanneer u een indeling voor de buitenste gegevens selecteert, kunt u het beste indien mogelijk een bestaande indeling opnieuw gebruiken. Het gebruiken van reeds-bewezen formaat zorgt ervoor dat uw uitgaande gegevens met succes zullen worden geproduceerd. Als u precies wilt zien hoe een bestaande indeling wordt opgemaakt, klikt u op de knop [!UICONTROL Formats] in de menubalk en zoek naar de indeling op naam of op id-nummer. Onjuiste indelingen of macro&#39;s die in indelingen worden gebruikt, zorgen voor een verkeerde indeling of verhinderen dat informatie volledig wordt uitgevoerd.

Ga voor meer informatie over het instellen van indelingen en het gebruik van macro&#39;s naar [Bestandsindelingsmacro&#39;s](formats/file-formats.md#) en [HTTP-indelingsmacro&#39;s](formats/web-formats.md).

### Misgeconfigureerde server

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Voer geen voorvoegsels voor hostnamen in. Als je een account hebt [!DNL ftp://hello.com], eenvoudig binnenkomen [!DNL hello.com] op dit gebied.
   * **[!UICONTROL Port/Type Combination]**
      * Voor een [!DNL FTP] overdracht, het aangewezen overdrachtstype is [!DNL SFTP].
      * Wanneer u de [!DNL SFTP] type, de haven is bijna altijd 22.
      * Wanneer u de [!DNL FTPs/TLS] type, de haven is bijna altijd 21.
      * De [!DNL FTPs/TLS] type is niet hetzelfde als normaal [!DNL FTP] overdracht. We ondersteunen geen reguliere (ongedekte) [!DNL FTP] overdrachten.
   * **[!UICONTROL Remote Path]**
      * Wanneer u een extern subpad kiest, moet dit zonder slash worden ingevoerd.
      * Als het overgedragen bestand in het [!DNL (root)/inbound] submap, eenvoudig toevoegen [!DNL inbound] voor het externe pad, niet [!DNL /inbound].
      * Als u uw bestanden meerdere directory&#39;s langs het pad verzendt, voert u tussen elke directory een slash in. Als u de locatie van [!DNL /inbound/subdirectory1/subdirectory2], moet u [!DNL inbound/subdirectory1/subdirectory2] op dit gebied.
      * Als het bestand automatisch naar de externe server wordt gerouteerd en in de map wordt geplaatst, kunt u deze ruimte leeg laten. Voer geen punt in ( . ), schuine streep ( / ) of iets anders.

* **[!DNL S3]**
   * [!DNL S3] is het voorkeursoverdrachtprotocol (over [!DNL FTP] of [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * De naam van het emmertje moet worden vermeld zonder schuine strepen, voorvoegsels, achtervoegsels, enz. Als u het adres krijgt [!DNL s3://your-bucket] toevoegen [!DNL your-bucket] in dit veld.
      * **[!UICONTROL Directory]**
         * Laat dit veld leeg, tenzij u specifiek een submap krijgt waarin de gegevens moeten worden geplaatst. Als u het adres krijgt [!DNL s3://your-bucket/your-subdirectory], enter [!DNL your-bucket] in de [!UICONTROL Bucket] veld en [!DNL your-subdirectory] worden toegevoegd aan de [!UICONTROL Directory] veld. Voeg geen voorafgaande schuine strepen toe.
         * Als u meerdere directory&#39;s langs het pad moet verplaatsen, moet u alleen slashes gebruiken als scheidingstekens. Dus een locatie van [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] zou [!DNL your-bucket] in de [!UICONTROL Bucket] veld en [!DNL your-subdirectory1/your-subdirectory2] zijn ingevoerd [!UICONTROL Directory] veld.
      * **[!UICONTROL Access / Secret Keys]**
         * Wanneer [!DNL TechOps] maakt een emmer en verleent toegang/geheime sleutels aan een consultant. Deze referenties zijn meestal `READ-ONLY` geloofsbrieven die aan de cliënt moeten worden geleverd. Deze referenties mogen niet worden ingevoerd in het dialoogvenster [!UICONTROL Access / Secret Key] velden, omdat de overdracht dan mislukt (omdat deze gegevens alleen-lezen zijn en niet beschrijfbaar). Wanneer [!DNL TechOps] maakt een emmer en verstrekt geloofsbrieven, zou de adviseur ook om een zeer belangrijk paar van de Adobe moeten verzoeken - NIET AAN DE CLIENT WORDEN VERLEEND - dat voor het schrijven van dossiers aan dit emmertje zal toestaan. Die sleutel moet aan deze gebieden worden toegevoegd.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Voer voorvoegselgegevens in voor [!DNL HTTP] vermeldingen. Als je een account hebt [!DNL https://superduper.com], enter [!DNL https://superduper.com] op dit gebied.
      * **[!UICONTROL URL Prefix]**
         * Bij het toevoegen van een [!DNL URL] , laat de voorafgaande schuine streep weg. Een adres van [!DNL https://hello.com/r/x/y/z] moeten [!DNL https://hello.com] ingevoerd in het [!UICONTROL Domain] veld en [!DNL r/x/y/z] hier ingevoerd in het [!UICONTROL URL Prefix] veld.
         * Indien een [!UICONTROL URL Prefix] niet nodig is, laat deze waarde leeg.
      * **[!UICONTROL Authentication - SSH Key]**
         * Voer de volledige waarde in `SSH PRIVATE` De sleutelwaarde in dit vakje, met inbegrip van kopballen, footers, en lijnonderbrekingen om nauwkeurige encryptie/zeer belangrijke opslag te verzekeren.

### Onvoldoende tijd voor uitgaande Generatie

Het outbounding proces loopt tweemaal daags, en veelvoudige processen (het uitspringen, het publiceren, het duwen aan externe plaatsen, enz.) moet worden uitgevoerd voordat een bestand naar de uiteindelijke bestemming wordt geduwd. Een goede regel van duim is dat een bestemming volledig zou moeten worden gevormd minstens 24 uren alvorens u gegevens kunt verwachten die aan een externe plaats worden geduwd.

### Gesplitste bestanden te groot

Wanneer uitgaande bestanden naar doelen worden gesplitst, kunt u grotere uitgaande bestanden in bestandskoppelingen splitsen. Controleer of de afzonderlijke bestandskoppelingen niet groter zijn dan 10 GB. Zie ook: [Naam uitgaand gegevensbestand: Syntaxis en voorbeelden](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Hoe te opstelling Uw Doelen om Experience Cloud IDs, identiteitskaart van de Klant of Audience Manager IDs in Uitgaande Dossiers van Gegevens uit te voeren {#set-up-destinations-export}

Op deze pagina ziet u hoe u doelen instelt voor het exporteren van gegevens die zijn weggehaald van het id-type dat u wilt in [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Met doelen kunnen onze klanten hun gegevens op elk willekeurig aantal digitale kanalen activeren. Ze kunnen bijvoorbeeld publieksgegevens exporteren naar andere [!DNL Adobe Experience Cloud] oplossingen ([!DNL Target], [!DNL Campaign], enz.). Of ze kunnen gegevens verzenden naar [!UICONTROL DSP]s, [!UICONTROL SSP]s, of om het even welk platform dat met Audience Manager wordt geïntegreerd. We houden een lijst bij van partners waarmee we samenwerken aan onze [Integratie Wiki-pagina](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Voor een gedetailleerde analyse bij het creëren van bestemmingen in Admin UI, kijk aan [Bedrijfsdoelen maken of bewerken](companies/admin-manage-company-destinations.md#create-edit-company-destinations) artikel.

Uw klanten willen verschillende types van identiteitskaart, afhankelijk van bestemming uitvoeren. In het onderstaande configuratieschema ziet u de opties die u moet selecteren om profielgegevens te exporteren die betrekking hebben op verschillende id-typen. We raden u aan ook te verwijzen naar de [Index van id&#39;s in Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). Er zijn drie belangrijke instellingen die in overweging moeten worden genomen: [!UICONTROL User ID Key]de [!UICONTROL Data Source Type] en de [!UICONTROL Format]. We geven ze allemaal hieronder in detail weer.

* [!UICONTROL User ID Key]. In de [!UICONTROL Admin UI], ga naar **[!UICONTROL Companies]**. Zoek naar het bedrijf van uw klant en klik het. Zoek naar **[!UICONTROL Destinations]** tab en druk op **[!UICONTROL Add Destination]**. In de **[!UICONTROL Add Destination]** werkstroom, selecteert u de [!UICONTROL User ID Key]. De [!UICONTROL User ID Key] De binnenkomende id&#39;s van de doelgegevensbron filteren en alleen toestaan dat de id&#39;s worden doorgegeven.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Selecteer deze optie wanneer u een doel maakt in de gebruikersinterface van de Audience Manager. Selecteer eerst [!UICONTROL Inbound]Selecteer vervolgens het gewenste id-type. De opties zijn:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Met deze optie bepaalt u de bestandsindeling die u wilt exporteren. In de **[!UICONTROL Add Destination]** workflow, onder **[!UICONTROL Batch Data]** selecteert u de indeling.

Als u een indeling wilt inspecteren, gaat u naar **[!UICONTROL Admin UI > Formats]** en zoekt naar [!UICONTROL Data Row] element. This element contains a macro of the file format, &lt;mcid> in het onderstaande voorbeeld.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> Configuratienummer. </th> 
   <th colname="col1" class="entry"> <p>Gebruikerssleutel </p> </th> 
   <th colname="col2" class="entry"> <p>Type gegevensbron </p> </th> 
   <th colname="col3" class="entry"> <p>Indeling </p> </th> 
   <th colname="col4" class="entry"> <p>Geëxporteerd id-type </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud-id </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud-id </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud-id </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud-id </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-id </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-id </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-id </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-id </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager-id </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Klant-id </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Klant-id (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Klant-id </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-id </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Klant-id </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Audience Manager-id </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Audience Manager-id </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud-id </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Audience Manager-id </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID Audience Manager </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gevallen gebruiken

Laten we zeggen dat u Audience Manager gebruikt en [!DNL Campaign]. Om de klantgegevens in [!DNL Campaign], wilt u exporteren [!UICONTROL Experience Cloud IDs]. Gebruik in dit geval configuratienummer 3.
