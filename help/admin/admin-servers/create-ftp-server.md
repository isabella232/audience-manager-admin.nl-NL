---
description: Gebruik de pagina Servers in het hulpmiddel Admin van de Audience Manager om een nieuwe server van FTP tot stand te brengen of een bestaande server uit te geven.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: Een FTP-server maken of bewerken
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 3%

---

# Een FTP-server maken of bewerken {#create-or-edit-an-ftp-server}

Gebruik de [!UICONTROL Servers] pagina in het hulpmiddel Admin van de Audience Manager om een nieuwe server van FTP tot stand te brengen of een bestaande server uit te geven.

>[!NOTE]
>
>U moet beschikken over de [!UICONTROL DEXADMIN] rol om nieuwe servers te maken of bestaande servers te bewerken.

1. Als u een nieuwe server wilt maken, klikt u op **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Als u een bestaande server wilt bewerken, klikt u op de gewenste server in het dialoogvenster **[!UICONTROL Label]** kolom.
1. Geef het gewenste label voor deze server op.
1. Van de **[!UICONTROL Protocol]** Selecteer het gewenste protocol in de vervolgkeuzelijst: **FTP**.

   >[!NOTE]
   >
   >Als beste praktijken, adviseren wij het gebruiken [!DNL Amazon S3] als een methode voor het ophalen van bestanden van en het leveren van bestanden aan partners. [!DNL Amazon S3] verstrekt een eenvoudige interface van de Webdiensten die kan worden gebruikt om het even welke hoeveelheid gegevens op te slaan en terug te winnen, op elk ogenblik, van overal op het Web. Zie voor meer informatie [Informatie over Amazon S3](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) in de *Gebruikershandleiding voor Audience Manager*.

1. Vul de velden in:

   * **[!UICONTROL Type]:** Selecteer het gewenste versleutelingstype: **[!UICONTROL SFTP]** of **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** Geef het gewenste domein (host) voor deze server op.
   * **[!UICONTROL Port]:** Geef de gewenste poort voor deze server op. De standaardpoort wordt weergegeven voor elk type codering. Indien nodig kunt u de standaardpoort wijzigen.
   * **[!UICONTROL Remote Path]:** Geef het gewenste externe pad voor deze server op. Als u dit veld leeg laat, plaatst Audience Manager de bestanden in de standaardmap.
   * **[!UICONTROL .tmp File Rename on Completion]:** Schakel deze optie in om de naam van de `.tmp` bestand na voltooiing.
   * **[!UICONTROL Filename Suffix]:** Geef de tekst op die u wilt toevoegen aan de bestandsoverdracht.
   * **[!UICONTROL Moved to When Finished]:** Geef het pad op naar de locatie waar het overdrachtsbestand na voltooiing moet worden verplaatst.
   * **[!UICONTROL Authentication]:** Geef de gewenste serververificatiemethode op: **[!UICONTROL Username/Password]** of **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >Vergeet niet ons egres toe te voegen [!DNL FTP] [!DNL IP] aan uw lijst van toegestane IPs: **52.44.29.2004**.

1. Voor **[!UICONTROL SSH Key]** verificatie:
   >[!NOTE]
   >
   >Wanneer het vormen van de Zeer belangrijke authentificatie van SSH, zorg ervoor om de openbare en privé sleutels altijd in formaat slechts OpenSSH te produceren.
   1. Het openbare/persoonlijke sleutelpaar genereren op basis van een willekeurige [!DNL Linux] of [!DNL Mac] machine.
   1. Geef de **openbare sleutel** aan de klant om op hun [!DNL SFTP] server. Zij moeten al tekst van de openbare sleutel op hun server omvatten, met inbegrip van `-----BEGIN RSA PRIVATE KEY-----` en  `-----END RSA PRIVATE KEY-----` . In ruil daarvoor moeten zij de gebruikersnaam opgeven waaronder zij de sleutel installeren.
   1. Werk het veld Gebruikersnaam bij met het veld dat door de client is opgegeven en het veld Key met het veld **persoonlijke sleutel**.
1. Klikken **[!UICONTROL Create]** als u een nieuwe server maakt, of klikt u op **[!UICONTROL Update]** als u een bestaande server bewerkt.
