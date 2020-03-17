---
description: Informatie die u helpt bij het instellen van doelen in Audience Manager en het vermijden van algemene problemen.
seo-description: Informatie die u helpt bij het instellen van doelen in Audience Manager en het vermijden van algemene problemen.
seo-title: Probleemoplossing voor configuratie bestemming
title: Probleemoplossing voor configuratie bestemming
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# Probleemoplossing voor configuratie bestemming {#destination-setup-troubleshooting}

Informatie die u helpt bij het instellen van doelen in Audience Manager en het vermijden van algemene problemen.

## Ik heb een bestemming ingesteld, maar ik zie geen bestanden. Waar zijn ze? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

De gemeenschappelijke problemen van de bestemmingsconfiguratie omvatten de volgende kwesties:

### Misconfigured Doel

* **Onjuiste[!UICONTROL UserID]sleutel:** De [!UICONTROL UserID] sleutel is de [!UICONTROL MasterDPID] van deze bestemming en vormt de basis voor de waarden van identiteitskaart die zullen worden begrensd. Zelfs als een [!UICONTROL UserID] sleutel via de drop-down lijst selecteerbaar is, betekent het niet noodzakelijk dat er IDs/traits/segmenten aan deze waarde in kaart worden gebracht. Als het [!UICONTROL Outbound] proces (dat loopt nadat de doelen zijn gemaakt) geen gebruikers vindt die aan deze [!UICONTROL UserID] sleutel zijn toegewezen, zullen er geen gegevens worden overtroffen.
* **Nee in geselecteerde bestandsgegevensbronnen:** Wanneer u een ander doeltype kiest dan [!UICONTROL S2S], wordt onder aan het scherm een sectie met het label weergegeven [!UICONTROL Configure Data Sources]. Wanneer deze sectie voor het eerst wordt weergegeven, worden geen waarden geselecteerd. Als u bent vergeten op het [!UICONTROL All First Party] selectievakje te klikken of gegevensbronnen afzonderlijk in het [!UICONTROL Available Data Sources] venster te selecteren, worden er geen gegevens overtroffen.

### Misconfigured Formaat

Wanneer u een indeling voor de buitenste gegevens selecteert, kunt u het beste indien mogelijk een bestaande indeling opnieuw gebruiken. Het gebruiken van reeds-bewezen formaat zorgt ervoor dat uw uitgaande gegevens met succes zullen worden geproduceerd. Als u precies wilt zien hoe een bestaande indeling wordt opgemaakt, klikt u op de [!UICONTROL Formats] optie in de menubalk en zoekt u de indeling op naam of op id-nummer. Onjuiste indelingen of macro&#39;s die in indelingen worden gebruikt, zorgen voor een verkeerde indeling of verhinderen dat informatie volledig wordt uitgevoerd.

Zie [Bestandsindelingmacro&#39;s](formats/file-formats.md#) en [HTTP-indelingsmacro&#39;s](formats/web-formats.md)voor meer informatie over het instellen van indelingen en het gebruik van macro&#39;s.

### Misgeconfigureerde server

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * Voer geen voorvoegsels voor hostnamen in. Als je een account hebt, kun je gewoon [!DNL ftp://hello.com][!DNL hello.com] in dit veld invoeren.
   * **[!UICONTROL Port/Type Combination]**
      * Voor een [!DNL FTP] overdracht, is het aangewezen overdrachtstype [!DNL SFTP].
      * Wanneer het selecteren van het [!DNL SFTP] type, is de haven bijna altijd 22.
      * Wanneer het selecteren van het [!DNL FTPs/TLS] type, is de haven bijna altijd 21.
      * Het [!DNL FTPs/TLS] type is niet hetzelfde als een normale [!DNL FTP] overdracht. We ondersteunen regelmatige (ongedekte) [!DNL FTP] overdrachten niet.
   * **[!UICONTROL Remote Path]**
      * Wanneer u een extern subpad kiest, moet dit zonder slash worden ingevoerd.
      * Als het overgedragen bestand in de [!DNL (root)/inbound] submap moet worden geplaatst, voegt u het gewoon toe [!DNL inbound] voor het externe pad, niet [!DNL /inbound].
      * Als u uw bestanden meerdere directory&#39;s langs het pad verzendt, voert u tussen elke directory een slash in. Als u de locatie van [!DNL /inbound/subdirectory1/subdirectory2]krijgt, moet u [!DNL inbound/subdirectory1/subdirectory2] dit veld invoeren.
      * Als het bestand automatisch naar de externe server wordt gerouteerd en in de map wordt geplaatst, kunt u deze ruimte leeg laten. Voer geen punt in ( . ), schuine streep ( / ) of iets anders.

* **[!DNL S3]**
   * [!DNL S3] is het voorkeursoverdrachtprotocol (boven [!DNL FTP] of [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * De naam van het emmertje moet worden vermeld zonder schuine strepen, voorvoegsels, achtervoegsels, enz. Als u het adres krijgt [!DNL s3://your-bucket] moet u dit veld gewoon [!DNL your-bucket] uitbreiden.
      * **[!UICONTROL Directory]**
         * Laat dit veld leeg, tenzij u specifiek een submap krijgt waarin de gegevens moeten worden geplaatst. Als u het adres krijgt, ga [!DNL s3://your-bucket/your-subdirectory]op het [!DNL your-bucket] gebied in en [!UICONTROL Bucket] zou aan het [!DNL your-subdirectory] [!UICONTROL Directory] gebied moeten worden toegevoegd. Voeg geen voorafgaande schuine strepen toe.
         * Als u meerdere directory&#39;s langs het pad moet verplaatsen, moet u alleen slashes gebruiken als scheidingstekens. Een locatie van [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] zou dus [!DNL your-bucket] in het [!UICONTROL Bucket] veld zijn ingevoerd en in het [!DNL your-subdirectory1/your-subdirectory2] veld zijn [!UICONTROL Directory] ingevoerd.
      * **[!UICONTROL Access / Secret Keys]**
         * Wanneer [!DNL TechOps] creeert een emmer en toegang/geheime sleutels aan een consultant verstrekt, zijn die geloofsbrieven gewoonlijk `READ-ONLY` geloofsbrieven die aan de cliënt moeten worden overhandigd. Deze gegevens moeten niet in de [!UICONTROL Access / Secret Key] velden worden ingevoerd, omdat de overdracht dan mislukt (omdat deze gegevens alleen-lezen zijn en niet beschrijfbaar). Als er een emmertje [!DNL TechOps] wordt gemaakt en er referenties worden verschaft, moet de consultant ook een Adobe-sleutelpaar aanvragen - NIET AAN DE CLIENT TE WORDEN GEGEVEN - waarmee bestanden naar dit emmertje kunnen worden geschreven. Die sleutel moet aan deze gebieden worden toegevoegd.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * Voer geen voorvoegselgegevens in voor [!DNL HTTP] vermeldingen. Als je een account hebt ontvangen [!DNL https://superduper.com], voer je dit [!DNL https://superduper.com] in.
      * **[!UICONTROL URL Prefix]**
         * Laat de voorafgaande schuine streep weg wanneer u een [!DNL URL] voorvoegsel toevoegt. Een adres van [!DNL https://hello.com/r/x/y/z] zou op het [!DNL https://hello.com] gebied moeten zijn [!UICONTROL Domain] ingegaan en [!DNL r/x/y/z] ingegaan hier op het [!UICONTROL URL Prefix] gebied.
         * Laat deze waarde leeg als er geen waarde [!UICONTROL URL Prefix] nodig is.
      * **[!UICONTROL Authentication - SSH Key]**
         * Voer in dit vak de volledige `SSH PRIVATE` sleutelwaarde in, inclusief kop- en voetteksten en regeleinden, voor een nauwkeurige versleuteling/sleutelopslag.

### Onvoldoende tijd voor uitgaande Generatie

Het outbounding proces loopt tweemaal daags, en veelvoudige processen (het uitspringen, het publiceren, het duwen aan externe plaatsen, enz.) moet worden uitgevoerd voordat een bestand naar de uiteindelijke bestemming wordt geduwd. Een goede regel van duim is dat een bestemming volledig zou moeten worden gevormd minstens 24 uren alvorens u gegevens kunt verwachten die aan een externe plaats worden geduwd.

### Gesplitste bestanden te groot

Wanneer uitgaande bestanden naar doelen worden gesplitst, kunt u grotere uitgaande bestanden in bestandskoppelingen splitsen. Controleer of de afzonderlijke bestandskoppelingen niet groter zijn dan 10 GB. Zie ook [Naam uitgaand gegevensbestand: Syntaxis en voorbeelden](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## Hoe u uw doelen instelt voor het exporteren van de ervaring in cloud-id&#39;s, Customer ID&#39;s of Audience Manager-id&#39;s in uitgaande gegevensbestanden {#set-up-destinations-export}

Deze pagina toont u hoe te opstellingsbestemmingen om gegevens uit te voeren die van het type van identiteitskaart u binnen wilt [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

Met doelen kunnen onze klanten hun gegevens op elk willekeurig aantal digitale kanalen activeren. Ze kunnen bijvoorbeeld publieksgegevens exporteren naar andere [!DNL Adobe Experience Cloud] oplossingen ([!DNL Target], [!DNL Campaign]enz.). Of ze kunnen gegevens verzenden naar [!UICONTROL DSP]s, [!UICONTROL SSP]s of een platform dat is geïntegreerd met Audience Manager. We houden een lijst bij van partners waarmee we werken aan onze [integrations Wiki pagina](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>Voor een gedetailleerde analyse bij het creëren van bestemmingen in Admin UI, kijk aan het [Create of geeft het artikel van de Doelen](companies/admin-manage-company-destinations.md#create-edit-company-destinations) van het Bedrijf uit.

Uw klanten willen verschillende types van identiteitskaart, afhankelijk van bestemming uitvoeren. In het onderstaande configuratieschema ziet u de opties die u moet selecteren om profielgegevens te exporteren die betrekking hebben op verschillende id-typen. We raden u aan ook te verwijzen naar de [index van id&#39;s in Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). Er zijn drie belangrijke instellingen die in overweging moeten worden genomen: de [!UICONTROL User ID Key], de [!UICONTROL Data Source Type] en de [!UICONTROL Format]. We geven ze allemaal hieronder in detail weer.

* [!UICONTROL User ID Key]. Ga in de [!UICONTROL Admin UI]. Ga naar **[!UICONTROL Companies]**. Zoek naar het bedrijf van uw klant en klik het. Zoek het **[!UICONTROL Destinations]** tabblad en druk op **[!UICONTROL Add Destination]**. Selecteer de **[!UICONTROL Add Destination]** werkstroom in de werkstroom [!UICONTROL User ID Key]. De id&#39;s [!UICONTROL User ID Key] filteren de inkomende id&#39;s van de doelgegevensbron en staan alleen toe dat de id&#39;s worden doorgegeven.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Selecteer deze optie wanneer u een doel maakt in de gebruikersinterface van Audience Manager. Selecteer eerst het gewenste id-type [!UICONTROL Inbound]en selecteer vervolgens het gewenste id-type. De opties zijn:

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. Met deze optie bepaalt u de bestandsindeling die u wilt exporteren. Selecteer de indeling onder **[!UICONTROL Add Destination]** in de **[!UICONTROL Batch Data]** workflow.

Als u een indeling wilt inspecteren, gaat u naar **[!UICONTROL Admin UI > Formats]** en zoekt u het [!UICONTROL Data Row] element. This element contains a macro of the file format, &lt;MCID> in het onderstaande voorbeeld.

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
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>UUID van Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Auditiebeheer-id </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID van Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Auditiebeheer-id </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Auditiebeheer-id </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID van Audience Manager </p> </td> 
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
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Klant-id </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID van Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Auditiebeheer-id </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>UUID van Audience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Auditiebeheer-id </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (Om het even welke gegevensbron het bedrijf heeft toegang tot) </p> </td> 
   <td colname="col2"> <p>Auditiebeheer-id </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>UUID van Audience Manager </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gevallen gebruiken

Laten we zeggen dat u Audience Manager en [!DNL Campaign]. Als u de klantgegevens in wilt laten werken, [!DNL Campaign]wilt u exporteren [!UICONTROL Experience Cloud IDs]. Gebruik in dit geval configuratienummer 3.