---
description: Gebruik de pagina van Clients OAuth2 om een lijst van cliënten OAuth2 in uw configuratie van de Audience Manager te bekijken. U kunt bestaande clients bewerken of verwijderen of nieuwe clients maken, op voorwaarde dat u de juiste gebruikersrollen hebt toegewezen.
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: OAuth2-clients
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# OAuth2-clients {#oauth-clients}

Gebruik de pagina [!UICONTROL OAuth2 Clients] om een lijst van [!UICONTROL OAuth2] cliënten in uw [!DNL Audience Manager] configuratie te bekijken. U kunt bestaande clients bewerken of verwijderen of nieuwe clients maken, op voorwaarde dat u de juiste gebruikersrollen hebt toegewezen.

## Overzicht {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Zorg ervoor dat uw klant de [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) documentatie in de Gids van de Gebruiker van de Audience Manager leest.

[!DNL OAuth2] is een open norm voor vergunning om beveiligde gedelegeerde toegang tot  [!DNL Audience Manager] middelen namens een middeleigenaar te verlenen.

![](assets/oauth.png)

U kunt elke kolom in stijgende of dalende orde sorteren door de gewenste kopbal van de kolom te klikken.

Gebruik de doos [!UICONTROL Search] of de pagineringscontroles bij de bodem van de lijst om de gewenste cliënt te vinden.

## Een OAuth2-client maken of bewerken {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Met de [!UICONTROL OAuth2 Clients]-pagina in de Audience Manager [!UICONTROL Admin] kunt u een nieuwe [!UICONTROL Oauth2]-client maken of een bestaande client bewerken.

1. Als u een nieuwe [!UICONTROL OAuth2]-client wilt maken, klikt u op **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**. Als u een bestaande [!UICONTROL OAuth2]-client wilt bewerken, klikt u op de gewenste client in de kolom **[!UICONTROL Client ID]**.
1. Geef de gewenste naam op voor deze [!UICONTROL OAuth2]-client. Dit is alleen een naam voor de record.
1. Geef het e-mailadres van de [!UICONTROL OAuth2]-client op. Er geldt een limiet van één e-mailadres.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Partner]** de gewenste partner.
1. Geef in het vak **[!UICONTROL Client ID]** de gewenste id op. Dit is de waarde die wordt gebruikt bij het verzenden van [!DNL API] verzoeken. Het voorvoegsel wordt automatisch gevuld wanneer u begint te typen nadat u een [!UICONTROL Partner] in de vervolgkeuzelijst in de voorafgaande stap hebt gekozen. De juiste indeling is &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>.
1. Schakel desgewenst het selectievakje **[!UICONTROL Restrict to Partner Users]** in of uit. Als dit controlevakje wordt geselecteerd, moet de gebruiker een [!DNL Audience Manager] gebruiker zijn die voor de geselecteerde partner wordt vermeld. We raden u aan deze optie te selecteren.
1. Schakel in de sectie **[!UICONTROL Scope]** de selectievakjes **[!UICONTROL Read]** en **[!UICONTROL Write]** naar wens in of uit.
1. Selecteer in de sectie **[!UICONTROL Grant Type]** het gewenste middel voor autorisatie. Wij adviseren dat u de standaardmontages van [!UICONTROL Password] en [!UICONTROL Refresh-token] opties gebruikt.

   * **[!UICONTROL Implicit]**: Als u deze optie selecteert, wordt het  [!UICONTROL Redirect URI] vak ingeschakeld. De gebruiker krijgt een automatisch toegangstoken nadat voor authentiek wordt verklaard en wordt onmiddellijk verzonden naar omleiding [!DNL URI].
   * **[!UICONTROL Authorization Code]**: Als u deze optie selecteert, wordt het  [!UICONTROL Redirect URI] vak ingeschakeld. De gebruiker wordt teruggegeven aan de cliënt na voor authentiek verklaard en dan verzonden naar redirect [!DNL URI].
   * **[!UICONTROL Password]**: De gebruiker wordt geverifieerd met een door de gebruiker ingevoerd wachtwoord en niet met een automatische validatiepoging via een verificatieserver.
   * **[!UICONTROL Refresh_token]**: Gebruikt om een verlopen toegangstoken voor een lange periode te verfrissen.

1. Geef in het tekstvak **[!UICONTROL Redirect URI]** de gewenste [!DNL URI] op. Deze optie wordt toegelaten slechts als u **[!UICONTROL Implicit]** en **[!UICONTROL Authorization_code]** subsidietypes selecteert. In het tekstvak **[!UICONTROL Redirect URI]** kunt u een door komma&#39;s gescheiden waarde van acceptabele [!DNL URI]-waarden opgeven. Dit is [!DNL URI] een gebruiker van een cliënt wordt opnieuw gericht aan na het goedkeuren van de cliënt voor toegang [!DNL API].
1. Geef de gewenste vervaltijd (in seconden) op voor toegang en vernieuw de vervaldatum van het token.

   * **[!UICONTROL Access Token Expiration Time]**: Het aantal seconden dat een toegangstoken na wordt uitgegeven geldig is. Kan null zijn als u de standaardinstelling van het platform wilt gebruiken (12 uur). Ook kan -1 zijn om erop te wijzen dat het toegangstoken niet verloopt.
   * **[!UICONTROL Refresh Token Expiration Time]**: Het aantal seconden dat een vernieuwingstoken geldig is nadat het wordt uitgegeven. Kan null zijn als u de standaardinstelling van het platform wilt gebruiken (30 dagen).

1. Klik op **[!UICONTROL Save]**.

Als u een [!UICONTROL OAuth2]-client wilt verwijderen, klikt u op **[!UICONTROL OAuth2 Clients]** en vervolgens op ![](assets/icon_delete.png) in de kolom **[!UICONTROL Actions]** voor de gewenste client.

>[!MORELIKETHIS]
>
>* [API-vereisten en -aanbevelingen](../admin-oauth2/aam-admin-api-requirements.md)

