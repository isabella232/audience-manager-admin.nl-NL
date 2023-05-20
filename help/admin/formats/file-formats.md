---
description: Hier worden de macro's weergegeven die u kunt gebruiken om op FTP gebaseerde gegevensbestanden te maken. Sommige macro's kunnen voor alle gebieden en rijen van het gegevensdossier worden gebruikt. Andere macro's zijn alleen specifiek voor koptekst- en gegevensrijen.
seo-description: Lists the macros you can use to create FTP-based data files. Some macros can be used for all data file fields and rows. Other macros are specific to header and data rows only.
seo-title: File Format Macros
title: Macro's voor bestandsindelingen
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
exl-id: e686bc33-da3e-49a9-8c71-2bc6ca399bfb
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 1%

---

# Macro&#39;s voor bestandsindelingen {#file-format-macros}

Hier worden de macro&#39;s weergegeven die u kunt gebruiken om te maken [!DNL FTP]op -gebaseerde gegevensbestanden. Sommige macro&#39;s kunnen voor alle gebieden en rijen van het gegevensdossier worden gebruikt. Andere macro&#39;s zijn alleen specifiek voor koptekst- en gegevensrijen.

## Algemene macro&#39;s {#common-macros}

Deze macro&#39;s kunnen in elk formaatveld worden gebruikt. Zie voor voorbeelden [Voorbeelden van bestandsformaten in macro](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>Een niet-afdrukbaar ASCII-teken. Hiermee wordt het begin van een rij of een sectie met inhoud aangegeven. Deze kan ook worden gebruikt om gegevenskolommen in een bestand te scheiden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>Id van doelgegevensaanbieder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>ID belangrijkste gegevensaanbieder van gebruikersnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>Volgorde/doel-id. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>An alias for an order/destination ID. </p> <p>De waarde voor deze alias wordt ingesteld in het dialoogvenster <span class="wintitle"> Id van externe account </span> veld voor een doel (in het gedeelte <span class="wintitle"> Basisinstellingen </span> ). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>Geeft het synchronisatietype aan. Accepteert de volgende optionele variabelen: </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>: Volledige synchronisatie. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>: Incrementele synchronisatie. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Geeft de methode voor gegevensoverdracht aan. Accepteert de volgende optionele variabelen: </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>Een tijdstempel van 10 cijfers, UTC en Unix. </p> <p>Het kan ook worden opgemaakt als <code>YYYYMMDDhhmmss</code> volgt de opmaakregels voor datum- en tijdstempels van Java. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Koptekstveldmacro&#39;s {#header-field-macros}

Macro&#39;s die alleen in koptekstvelden worden gebruikt. Zie voor voorbeelden [Voorbeelden van bestandsformaten in macro](../formats/file-format-examples.md).

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Deze macro wordt gebruikt als scheidingsteken en voegt een tab in tussen velden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Macro&#39;s gegevensrij {#data-row-macros}

Macro&#39;s die alleen in gegevensrijen worden gebruikt. Zie voor voorbeelden [Voorbeelden van bestandsformaten in macro](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Macro </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt een gesloten accolade ingevoegd <code>}</code> teken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u een komma in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> Unieke gebruikersnaam gegevenspartner </span>. Hiermee wordt de id geretourneerd die u aan een gebruiker/sitebezoeker hebt toegewezen als die id al is gesynchroniseerd met een <span class="keyword"> Audience Manager </span> apparaat-id. </p> <p>Als DPID 0 is, retourneert deze macro de <span class="keyword"> Audience Manager </span> ID in plaats van je ID voor de gebruiker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>Keert een lijst terug die veelvoudige IDs voor een gegevenspartner bevat. Dit is nuttig als u een grote organisatie met veelvoudige onderverdelingen of andere organisatorische groepen hebt u gegevens met mag delen. Deze macro keert een lijst van identiteitskaarts voor die ondergeschikte groepen terug. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>De uitvoer van deze macro wijst de gegevensleverancier-id (DPID) toe aan gerelateerde unieke gebruikers-id's (DPUUID). Deze macro moet een opmaaktekenreeks hebben om de uitvoer ervan te bepalen. De voorbeelduitvoer ziet er ongeveer als volgt uit: </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p>De <code>maxMappings</code> met deze instelling bepaalt u hoeveel toewijzingen de macro moet retourneren. Wanneer <code>maxMappings=0</code>, retourneert deze macro alle toewijzingen voor elke opgegeven DPID. Gegevens worden gesorteerd op tijdstempel (meest recente eerst) en retourneert eerst resultaten met de grootste tijdstempel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>Vereist bij gebruik van de voorwaarde <code>if</code> en de <code>SEGMENT_LIST</code> en <code>REMOVED_SEGMENT_LIST</code> macro's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>Deze combinatie van macro's maakt een voorwaardelijke instructie waarin de segmenten worden vermeld waartoe gebruikers behoren <i>en</i> zijn verwijderd. Er wordt een lege tekenreeks geretourneerd als niet aan beide voorwaarden is voldaan of als er geen gegevens zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud ID.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt een open accolade ingevoegd <code>{</code> teken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>Vervangen. Niet gebruiken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>Vervangen. Niet gebruiken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p>Retourneert <code>1</code> als een statische, hardcodeerde waarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>Partner ID (PID). De PID verschijnt onder de <span class="wintitle"> Profiel </span> in de interface voor beheerders. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Retourneert een lijst met eventueel verwijderde segmenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Retourneert een lijst met segmenten in een lijst. Accepteert de volgende optionele variabelen: </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>: Verouderde id. Vervangen. Gebruiken <code>sid</code> (alleen kleine letters). </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>: Verouderde id. Vervangen. Gebruiken <code>sid</code> (alleen kleine letters). </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>: Segment-id. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>: Retourneert <code>5</code>, een statische, gecodeerde waarde die gegevens als segmentgegevens identificeert. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>: Toewijzing van het segment. Vervangen. Gebruiken <code>sid</code> (alleen kleine letters). </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>: Een Unix-tijdstempel waarmee de laatste keer wordt aangegeven dat een segment werd gerealiseerd. </li> 
    </ul> <p>Plaats deze variabelen tussen accolades na de macro. Deze code scheidt bijvoorbeeld de resultaten met een verticale streep (|): <code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p>Retourneert <code>1</code> als een statische, hardcodeerde waarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>Hiermee voegt u een tabscheidingsteken in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>Retourneert een lijst met kenmerken. Accepteert de volgende optionele argumenten: </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>: Typen dienstreizen geïdentificeerd door een numerieke id. Deze variabele retourneert: 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> die een spoor DPM (off-line, die door een binnenkomende baan wordt ingezien) identificeert. </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> die een op regels gebaseerde eigenschap identificeert (realtime; via <span class="wintitle"> DCS </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>: Gebruikersnaam dienstreis. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>: De laatste keer dat de eigenschap werd gerealiseerd. Unix timestamp. </li> 
    </ul> <p>Plaats deze variabelen tussen accolades na de macro. In deze code worden de resultaten bijvoorbeeld gescheiden met het teken "|" van de pipe: <code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> gebruikersnaam. </p> </td> 
  </tr> 
 </tbody> 
</table>
