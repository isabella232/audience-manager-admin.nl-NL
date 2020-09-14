---
description: Gebruik de pagina Servers in het hulpmiddel Admin van de Audience Manager om een nieuwe server van HTTP tot stand te brengen of een bestaande server uit te geven.
seo-description: Gebruik de pagina Servers in het hulpmiddel Admin van de Audience Manager om een nieuwe server van HTTP tot stand te brengen of een bestaande server uit te geven.
seo-title: Een HTTP-server maken of bewerken
title: Een HTTP-server maken of bewerken
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
translation-type: tm+mt
source-git-commit: d518ba4011f203a7d450ce76d8c1924f7d73a815
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 5%

---


# Een HTTP-server maken of bewerken {#create-or-edit-an-http-server}

Gebruik de [!UICONTROL Servers] pagina in het hulpmiddel van Admin van de Audience Manager om een nieuwe server van HTTP tot stand te brengen of een bestaande server uit te geven.

>[!NOTE]
>
>U moet de [!UICONTROL DEXADMIN] rol hebben om nieuwe servers te creëren of bestaande servers uit te geven.

1. Ga naar **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. Als u een bestaande server wilt bewerken, klikt u op de gewenste server in de **[!UICONTROL Label]** kolom.
1. Geef het gewenste label voor deze server op.
1. Selecteer in de **[!UICONTROL Protocol]** vervolgkeuzelijst het gewenste protocol: [!DNL HTTP].
1. Vul de velden in:

   * **[!UICONTROL Domain]:** Geef het gewenste domein (host) voor deze server op.
   * **[!UICONTROL Port]:** Geef de gewenste poort voor deze server op. De standaardpoort wordt weergegeven voor elk type codering. U kunt de standaardpoort desgewenst wijzigen
   * **[!UICONTROL Maximum Users Per Request]:** Geef het maximumaantal gebruikers op dat per aanvraag is toegestaan voor deze server.
   * **[!UICONTROL URL Prefix]:** Geef het [!DNL URL] voorvoegsel op dat u voor deze server wilt gebruiken.
   * **[!UICONTROL Authentication URL]:** Geef de [!UICONTROL Authentication URL] voor deze `HTTP` server op.
   * **[!UICONTROL Authentication]:** Geef de gewenste verificatiemethode op: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** of **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** De naam van de [!DNL HTTP] header, verstrekt door de klant, die de [!DNL HTTP] handtekeningsleutel bevat. De standaardwaarde is, [!UICONTROL X-Signature]zoals in het onderstaande voorbeeld wordt getoond:

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

   * **[!UICONTROL HTTP Signature Key]:** De sleutel die wordt gebruikt om het [!DNL HTTP] verzoek te ondertekenen, door de klant wordt verstrekt die.
   * **[!UICONTROL Show Signature Key]:** Schakel deze optie in of uit om de handtekening in de browser weer te geven.
   * **[!UICONTROL HTTP Signature Encryption Method]:** Geef de methode op waarmee de handtekening wordt versleuteld. Gebruik deze optie [!UICONTROL SHA1] tenzij de klant anders kiest.

   >[!NOTE]
   >
   >Als u [authentificatie OAuth 2.0 voor gegevensoverdrachten](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) in real time voor een partner wilt toelaten, vul de gebieden zoals in de hieronder lijst in. De velden *cursief* moeten exact zo worden ingevuld als in de tabel.

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

1. Klik **[!UICONTROL Create]** als u een nieuwe server maakt of klik **[!UICONTROL Update]** als u een bestaande server bewerkt.
