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

* **Onjuiste  [!UICONTROL UserID] sleutel:** De  [!UICONTROL UserID] sleutel is de  [!UICONTROL MasterDPID] van deze bestemming en is de basis voor de waarden van identiteitskaart die zullen worden begrensd. Zelfs als een [!UICONTROL UserID] sleutel via de drop-down lijst selecteerbaar is, betekent het niet noodzakelijk dat er IDs/traits/segmenten aan deze waarde in kaart worden gebracht. Als het [!UICONTROL Outbound] proces (dat loopt nadat de bestemmingen worden gecreeerd) geen gebruikers vindt die aan deze [!UICONTROL UserID] sleutel worden in kaart gebracht, zullen geen gegevens worden begrensd.
* **Nee in geselecteerde bestandsgegevensbronnen:** wanneer u een ander doeltype kiest dan  [!UICONTROL S2S], wordt een sectie onder aan het scherm met het label  [!UICONTROL Configure Data Sources]. Wanneer deze sectie voor het eerst wordt weergegeven, worden geen waarden geselecteerd. Als u vergeet om [!UICONTROL All First Party] controledoos te klikken of individueel gegevensbronnen van het [!UICONTROL Available Data Sources] venster te selecteren, zullen geen gegevens worden begrensd.

### Misconfigured Formaat

Wanneer u een indeling voor de buitenste gegevens selecteert, kunt u het beste indien mogelijk een bestaande indeling opnieuw gebruiken. Het gebruiken van reeds-bewezen formaat zorgt ervoor dat uw uitgaande gegevens met succes zullen worden geproduceerd. Als u precies wilt zien hoe een bestaande indeling wordt opgemaakt, klikt u op de optie [!UICONTROL Formats] in de menubalk en zoekt u de indeling op naam of op id-nummer. Onjuiste indelingen of macro&#39;s die in indelingen worden gebruikt, zorgen voor een verkeerde indeling of verhinderen dat informatie volledig wordt uitgevoerd.

Zie [Bestandsindelingmacro&#39;s](formats/file-formats.md#) en [HTTP-indelingsmacro&#39;s](formats/web-formats.md) voor meer informatie over het instellen van indelingen en het gebruik van macro&#39;s.

### Misgeconfigureerde server

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Voer geen voorvoegsels voor hostnamen in. Als u een account [!DNL ftp://hello.com] krijgt, voert u [!DNL hello.com] in dit veld in.
   * **[!UICONTROL Port/Type Combination]**
      * Voor een [!DNL FTP] overdracht, is het aangewezen overdrachtstype [!DNL SFTP].
      * Wanneer u het type [!DNL SFTP] selecteert, is de poort bijna altijd 22.
      * Wanneer u het type [!DNL FTPs/TLS] selecteert, is de poort bijna altijd 21.
      * Het type [!DNL FTPs/TLS] is niet het zelfde als regelmatige [!DNL FTP] overdracht. Wij steunen regelmatige (ongedekte) [!DNL FTP] overdrachten niet.
   * **[!UICONTROL Remote Path]**
      * Wanneer u een extern subpad kiest, moet dit zonder slash worden ingevoerd.
      * Als het overgedragen bestand in de submap [!DNL (root)/inbound] moet worden geplaatst, voegt u [!DNL inbound] toe voor het externe pad, niet [!DNL /inbound].
      * Als u uw bestanden meerdere directory&#39;s langs het pad verzendt, voert u tussen elke directory een slash in. Als u de locatie van [!DNL /inbound/subdirectory1/subdirectory2] hebt, moet u [!DNL inbound/subdirectory1/subdirectory2] in dit veld invoeren.
      * Als het bestand automatisch naar de externe server wordt gerouteerd en in de map wordt geplaatst, kunt u deze ruimte leeg laten. Voer geen punt in ( . ), schuine streep ( / ) of iets anders.

* **[!DNL S3]**
   * [!DNL S3] is het voorkeursoverdrachtprotocol (boven  [!DNL FTP] of  [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * De naam van het emmertje moet worden vermeld zonder schuine strepen, voorvoegsels, achtervoegsels, enz. Als u het adres [!DNL s3://your-bucket] wordt gegeven zou u eenvoudig [!DNL your-bucket] aan dit gebied moeten toevoegen.
      * **[!UICONTROL Directory]**
         * Laat dit veld leeg, tenzij u specifiek een submap krijgt waarin de gegevens moeten worden geplaatst. Als u het adres [!DNL s3://your-bucket/your-subdirectory] wordt gegeven, ga [!DNL your-bucket] op [!UICONTROL Bucket] gebied in en [!DNL your-subdirectory] zou in [!UICONTROL Directory] gebied moeten worden toegevoegd. Voeg geen voorafgaande schuine strepen toe.
         * Als u meerdere directory&#39;s langs het pad moet verplaatsen, moet u alleen slashes gebruiken als scheidingstekens. Op een locatie van [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] zou [!DNL your-bucket] in het veld [!UICONTROL Bucket] worden ingevoerd en [!DNL your-subdirectory1/your-subdirectory2] in het veld [!UICONTROL Directory].
      * **[!UICONTROL Access / Secret Keys]**
         * Als [!DNL TechOps] een emmertje maakt en toegang/geheime sleutels aan een consultant verstrekt, zijn die geloofsbrieven gewoonlijk `READ-ONLY` geloofsbrieven die aan de cliënt moeten worden geleverd. Deze geloofsbrieven zouden niet in de [!UICONTROL Access / Secret Key] gebieden moeten zijn ingegaan, omdat dit de overdracht zal veroorzaken om te ontbreken (omdat die geloofsbrieven read-only, niet schrijfbaar zijn). Als [!DNL TechOps] een emmer maakt en referenties verschaft, moet de consultant ook een sleutelpaar voor Adobe aanvragen - NIET AAN DE CLIENT TE WORDEN TOEGEKEND - waarmee bestanden naar dit emmertje kunnen worden geschreven. Die sleutel moet aan deze gebieden worden toegevoegd.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Voer voorvoegselgegevens in voor [!DNL HTTP]-items. Als u een account [!DNL https://superduper.com] krijgt, voert u [!DNL https://superduper.com] in dit veld in.
      * **[!UICONTROL URL Prefix]**
         * Wanneer u een voorvoegsel [!DNL URL] toevoegt, laat u de voorafgaande schuine streep weg. Bij een adres van [!DNL https://hello.com/r/x/y/z] moet [!DNL https://hello.com] worden ingevoerd in het veld [!UICONTROL Domain] en [!DNL r/x/y/z] hier worden ingevoerd in het veld [!UICONTROL URL Prefix].
         * Als een [!UICONTROL URL Prefix] niet nodig is, verlaat deze waarde leeg.
      * **[!UICONTROL Authentication - SSH Key]**
         * Voer in dit vak de volledige waarde `SSH PRIVATE` in voor de sleutel, inclusief kop- en voetteksten en regeleinden, zodat u over nauwkeurige versleuteling/sleutelopslag beschikt.

### Onvoldoende tijd voor uitgaande Generatie

Het outbounding proces loopt tweemaal daags, en veelvoudige processen (het uitspringen, het publiceren, het duwen aan externe plaatsen, enz.) moet worden uitgevoerd voordat een bestand naar de uiteindelijke bestemming wordt geduwd. Een goede regel van duim is dat een bestemming volledig zou moeten worden gevormd minstens 24 uren alvorens u gegevens kunt verwachten die aan een externe plaats worden geduwd.

### Gesplitste bestanden te groot

Wanneer uitgaande bestanden naar doelen worden gesplitst, kunt u grotere uitgaande bestanden in bestandskoppelingen splitsen. Controleer of de afzonderlijke bestandskoppelingen niet groter zijn dan 10 GB. Zie ook [Naam uitgaand gegevensbestand: Syntaxis en voorbeelden](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## Hoe te opstelling Uw Doelen om Experience Cloud IDs, identiteitskaart van de Klant of Audience Manager IDs in Uitgaande Dossiers van Gegevens uit te voeren {#set-up-destinations-export}

Deze pagina toont u hoe te opstellingsbestemmingen om gegevens uit te voeren die van het type ID u in [!UICONTROL Outbound Data Files] wilt.

<!-- set-up-destinations-mcid-aamid.xml -->

Met doelen kunnen onze klanten hun gegevens op elk willekeurig aantal digitale kanalen activeren. Ze kunnen bijvoorbeeld publieksgegevens exporteren naar andere [!DNL Adobe Experience Cloud]-oplossingen ([!DNL Target], [!DNL Campaign] enzovoort). Of ze kunnen gegevens verzenden naar [!UICONTROL DSP]s, [!UICONTROL SSP]s of elk platform dat is geïntegreerd met Audience Manager. We houden een lijst bij van partners waarmee we werken aan onze [pagina Integrations Wiki](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Voor een gedetailleerde analyse bij het creëren van bestemmingen in Admin UI, kijk aan [creeer of geef de Doelen van het Bedrijf](companies/admin-manage-company-destinations.md#create-edit-company-destinations) artikel uit.

Uw klanten willen verschillende types van identiteitskaart, afhankelijk van bestemming uitvoeren. In het onderstaande configuratieschema ziet u de opties die u moet selecteren om profielgegevens te exporteren die betrekking hebben op verschillende id-typen. Wij adviseren u ook naar [Index van IDs in Audience Manager ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en) te verwijzen. Er zijn drie belangrijke instellingen die in overweging moeten worden genomen: [!UICONTROL User ID Key], [!UICONTROL Data Source Type] en [!UICONTROL Format]. We geven ze allemaal hieronder in detail weer.

* [!UICONTROL User ID Key]. Ga in [!UICONTROL Admin UI] naar **[!UICONTROL Companies]**. Zoek naar het bedrijf van uw klant en klik het. Zoek naar **[!UICONTROL Destinations]** tabel en druk **[!UICONTROL Add Destination]**. Selecteer [!UICONTROL User ID Key] in de **[!UICONTROL Add Destination]**-workflow. Met [!UICONTROL User ID Key] worden de inkomende id&#39;s van de doelgegevensbron gefilterd en kunnen alleen de id&#39;s worden doorgegeven.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Selecteer deze optie wanneer u een doel maakt in de gebruikersinterface van de Audience Manager. Selecteer eerst [!UICONTROL Inbound] en selecteer vervolgens het gewenste id-type. De opties zijn:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Met deze optie bepaalt u de bestandsindeling die u wilt exporteren. Selecteer de indeling in de **[!UICONTROL Add Destination]**-workflow onder **[!UICONTROL Batch Data]**.

Als u een indeling wilt inspecteren, gaat u naar **[!UICONTROL Admin UI > Formats]** en zoekt u het element [!UICONTROL Data Row]. This element contains a macro of the file format, &lt;MCID> in het onderstaande voorbeeld.

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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
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

Laten we zeggen dat u Audience Manager en [!DNL Campaign] gebruikt. Als u de klantgegevens in [!DNL Campaign] wilt activeren, wilt u [!UICONTROL Experience Cloud IDs] exporteren. Gebruik in dit geval configuratienummer 3.
