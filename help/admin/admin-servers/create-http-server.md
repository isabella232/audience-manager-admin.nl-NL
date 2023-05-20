---
description: Gebruik de pagina Servers in het hulpmiddel Admin van de Audience Manager om een nieuwe server van HTTP tot stand te brengen of een bestaande server uit te geven.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: Een HTTP-server maken of bewerken
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 3%

---

# Een HTTP-server maken of bewerken {#create-or-edit-an-http-server}

Gebruik de [!UICONTROL Servers] pagina in het hulpmiddel Admin van de Audience Manager om een nieuwe server van HTTP tot stand te brengen of een bestaande server uit te geven.

>[!NOTE]
>
>U moet beschikken over de [!UICONTROL DEXADMIN] rol om nieuwe servers te maken of bestaande servers te bewerken.

1. Ga naar **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Als u een bestaande server wilt bewerken, klikt u op de gewenste server in het dialoogvenster **[!UICONTROL Label]** kolom.
1. Geef het gewenste label voor deze server op.
1. Van de **[!UICONTROL Protocol]** Selecteer het gewenste protocol in de vervolgkeuzelijst: [!DNL HTTP].
1. Vul de velden in:

   * **[!UICONTROL Domain]:** Geef het gewenste domein (host) voor deze server op.
   * **[!UICONTROL Port]:** Geef de gewenste poort voor deze server op. De standaardpoort wordt weergegeven voor elk type codering. U kunt de standaardpoort desgewenst wijzigen
   * **[!UICONTROL Maximum Users Per Request]:** Geef het maximumaantal gebruikers op dat per aanvraag is toegestaan voor deze server.
   * **[!UICONTROL URL Prefix]:** Geef de [!DNL URL] voor deze server te gebruiken.
   * **[!UICONTROL Authentication URL]:** Geef de [!UICONTROL Authentication URL] voor `HTTP` server.
   * **[!UICONTROL Authentication]:** Geef de gewenste verificatiemethode op: **[!UICONTROL None]**, **[!UICONTROL Username/Password]**, of **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** De naam van de [!DNL HTTP] header, verstrekt door de klant, die de [!DNL HTTP] handtekeningensleutel. De standaardwaarde is [!UICONTROL X-Signature], zoals in het onderstaande voorbeeld wordt getoond:

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** De sleutel die wordt gebruikt om het [!DNL HTTP] verzoek, verstrekt door de klant.
   * **[!UICONTROL Show Signature Key]:** Schakel deze optie in of uit om de handtekening in de browser weer te geven.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Geef de methode op waarmee de handtekening wordt versleuteld. Gebruiken [!UICONTROL SHA1] tenzij de klant anders kiest.

   >[!NOTE]
   >
   >Als u wilt inschakelen [OAuth 2.0 authentificatie voor gegevensoverdrachten in real time](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en) vult voor een partner de velden in zoals in de onderstaande tabel. De velden in *cursief* moeten exact worden ingevuld zoals in de tabel.

   | Naam | Waarde |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Toestemming*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. Klikken **[!UICONTROL Create]** als u een nieuwe server maakt, of klikt u op **[!UICONTROL Update]** als u een bestaande server bewerkt.
