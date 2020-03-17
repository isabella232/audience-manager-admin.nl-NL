---
description: Gebruik de pagina Servers in het hulpprogramma Audience Manager Admin om een nieuwe FTP-server te maken of om een bestaande server te bewerken.
seo-description: Gebruik de pagina Servers in het hulpprogramma Audience Manager Admin om een nieuwe FTP-server te maken of om een bestaande server te bewerken.
seo-title: Een FTP-server maken of bewerken
title: Een FTP-server maken of bewerken
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# Een FTP-server maken of bewerken {#create-or-edit-an-ftp-server}

Gebruik de [!UICONTROL Servers] pagina in het hulpmiddel Admin van de Manager van de Publiek om een nieuwe server van FTP tot stand te brengen of een bestaande server uit te geven.

>[!NOTE]
>
>U moet de [!UICONTROL DEXADMIN] rol hebben om nieuwe servers te creëren of bestaande servers uit te geven.

1. Als u een nieuwe server wilt maken, klikt u op **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Als u een bestaande server wilt bewerken, klikt u op de gewenste server in de **[!UICONTROL Label]** kolom.
1. Geef het gewenste label voor deze server op.
1. Selecteer in de **[!UICONTROL Protocol]** vervolgkeuzelijst het gewenste protocol: **FTP**.

   >[!NOTE]
   >
   >Als beste praktijken, adviseren wij gebruikend [!DNL Amazon S3] als methode om dossiers van te krijgen en dossiers te leveren aan partners. [!DNL Amazon S3] verstrekt een eenvoudige interface van de Webdiensten die kan worden gebruikt om het even welke hoeveelheid gegevens op te slaan en terug te winnen, op elk ogenblik, van overal op het Web. Zie [Informatie over Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) in de gebruikershandleiding *van* Audience Manager voor meer informatie.

1. Vul de velden in:

   * **[!UICONTROL Type]:**Selecteer het gewenste versleutelingstype:**[!UICONTROL SFTP]**of **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:**Geef het gewenste domein (host) voor deze server op.
   * **[!UICONTROL Port]:**Geef de gewenste poort voor deze server op. De standaardpoort wordt weergegeven voor elk type codering. Indien nodig kunt u de standaardpoort wijzigen.
   * **[!UICONTROL Remote Path]:**Geef het gewenste externe pad voor deze server op. Als u dit veld leeg laat, plaatst Audience Manager de bestanden in de standaardmap.
   * **[!UICONTROL .tmp File Rename on Completion]:**Schakel deze optie in om de naam van het`.tmp`bestand te wijzigen als het is voltooid.
   * **[!UICONTROL Filename Suffix]:**Geef de tekst op die u wilt toevoegen aan de bestandsoverdracht.
   * **[!UICONTROL Moved to When Finished]:**Geef het pad op naar de locatie waar het overdrachtsbestand na voltooiing moet worden verplaatst.
   * **[!UICONTROL Authentication]:**Geef de gewenste serververificatiemethode op:**[!UICONTROL Username/Password]**of **[!UICONTROL SSH Key]**.
   >[!NOTE]
   >
   >Onthoud dat u een whitelist maakt van ons uitgang [!DNL FTP] [!DNL IP]: **52.44.29.2004**.

1. Voor **[!UICONTROL SSH Key]** verificatie:
   1. Genereer het paar openbare/persoonlijke sleutels van een [!DNL Linux] of [!DNL Mac] computer.
   1. Geef de **openbare sleutel** aan de cliënt om op hun [!DNL SFTP] server bij te werken. Zij moeten alle tekst van de openbare sleutel op hun server omvatten, met inbegrip van `-----BEGIN RSA PRIVATE KEY-----` en `-----END RSA PRIVATE KEY-----` . In ruil daarvoor moeten zij de gebruikersnaam opgeven waaronder zij de sleutel installeren.
   1. Werk het veld Gebruikersnaam bij met het veld dat door de client wordt opgegeven en het veld Sleutel met de **persoonlijke sleutel**.
1. Klik **[!UICONTROL Create]** als u een nieuwe server maakt of klik **[!UICONTROL Update]** als u een bestaande server bewerkt.
