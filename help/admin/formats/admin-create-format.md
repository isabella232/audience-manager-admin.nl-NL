---
description: Met de pagina Opmaak in het Audience Manager Admin kunt u een nieuwe indeling maken of een bestaande indeling bewerken.
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: Een indeling maken of bewerken
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 2%

---

# Een indeling maken of bewerken {#create-or-edit-a-format}

Gebruik de [!UICONTROL Formats] in het hulpmiddel Admin van de Audience Manager om een nieuw formaat tot stand te brengen of een bestaand formaat uit te geven.

<!-- t_create_format.xml -->

>[!TIP]
>
>Wanneer u een indeling voor de buitenste gegevens selecteert, kunt u het beste indien mogelijk een bestaande indeling opnieuw gebruiken. Het gebruiken van reeds-bewezen formaat zorgt ervoor dat uw uitgaande gegevens met succes zullen worden geproduceerd. Als u precies wilt zien hoe een bestaande indeling wordt opgemaakt, klikt u op de knop [!UICONTROL Formats] in de menubalk en zoek naar de indeling op naam of op id-nummer. Onjuiste indelingen of macro&#39;s die in indelingen worden gebruikt, zorgen voor een verkeerde indeling of verhinderen dat informatie volledig wordt uitgevoerd.

1. Als u een nieuwe indeling wilt maken, klikt u op **[!UICONTROL Formats]** > **[!UICONTROL Add Format]**. Als u een bestaande indeling wilt bewerken, klikt u op de gewenste indeling in het dialoogvenster **[!UICONTROL Name]** kolom.

   ![](assets/create_format.png)

1. Vul de velden in:
   * **Naam:** (Vereist) Geef een beschrijvende naam op voor de indeling.
   * **Type:** (Vereist) Selecteer de gewenste indeling:
      * **[!UICONTROL File]**: Hiermee verzendt u gegevens via [!DNL FTP] bestanden.
      * **[!UICONTROL HTTP]**: Omsluit gegevens in een [!DNL JSON] inpakken.

1. (Voorwaardelijk) Als u **[!UICONTROL File]**, vult de velden in:

   >[!NOTE]
   >
   >Voor een lijst met beschikbare macro&#39;s raadpleegt u [Bestandsindelingsmacro&#39;s](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) en [HTTP-indelingsmacro&#39;s](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** Geef de bestandsnaam op voor het bestand voor gegevensoverdracht.
   * **Koptekst:** Geef de tekst op die in de eerste rij van het bestand voor gegevensoverdracht wordt weergegeven.
   * **[!UICONTROL Data Row]:** Geef de tekst op die in elke buitenste rij van het bestand wordt weergegeven.
   * **[!UICONTROL Maximum File Size (In MB)]:** Geef de maximale bestandsgrootte op voor bestanden voor gegevensoverdracht. Gecomprimeerde bestanden moeten kleiner zijn dan 100 MB. De ongecomprimeerde bestandsgrootte is niet beperkt.
   * **[!UICONTROL Compression]:** Selecteer het gewenste compressietype: gz of zip voor uw gegevensbestanden. Voor levering aan [!UICONTROL AWS S3], moet u .gz of ongecomprimeerde dossiers gebruiken.
   * **[!UICONTROL .info Receipt]:** Specificeert dat een overdracht-controle ([!DNL .info]) is gegenereerd. De [!DNL .info] het dossier verstrekt meta-gegevensinformatie over dossieroverdrachten zodat de partners kunnen verifiëren dat de Audience Manager correct behandelde dossieroverdrachten. Zie voor meer informatie [Bestanden voor bestandsoverdracht overdragen van logbestanden](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en).
   * **[!UICONTROL MD5 Checksum Receipt]:** Hiermee wordt opgegeven dat een [!DNL MD5] kassabon wordt gegenereerd. De [!DNL MD5] checksum ontvangstbewijs zodat de partners kunnen verifiëren dat de Audience Manager de volledige overdracht correct behandelde.

1. (Voorwaardelijk) Als u **[!UICONTROL HTTP]**, vult de velden in:

   * **[!UICONTROL Method]:** Kies de optie [!DNL API] methode die u voor het overdrachtsproces wilt gebruiken:
      * **[!UICONTROL POST]:** Als u [!DNL POST]selecteert u het inhoudstype ([!DNL XML] of [!DNL JSON]), wordt de aanvraaginstantie vermeld.
      * **[!UICONTROL GET]:** Als u [!DNL GET], geeft u de queryparameters op.

1. Klikken **[!UICONTROL Create]** als u een nieuwe indeling maakt, of klikt u op **[!UICONTROL Save Updates]** als u een bestaande indeling bewerkt.

## Een indeling verwijderen {#delete-format}

1. Klik op **[!UICONTROL Formats]**.
2. Klikken  ![](assets/icon_delete.png) in de **[!UICONTROL Actions]** van de gewenste indeling.
3. Klikken **[!UICONTROL OK]** om de schrapping te bevestigen.
