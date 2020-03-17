---
description: Gebruik de pagina van de Gebruikers van de Integratie om een lijst van gebruikers in uw configuratie van de Manager van de Publiek te bekijken. U kunt bestaande gebruikers bewerken of verwijderen of nieuwe gebruikers maken, op voorwaarde dat u de juiste gebruikersrollen hebt toegewezen.
seo-description: Gebruik de pagina van de Gebruikers van de Integratie om een lijst van gebruikers in uw configuratie van de Manager van de Publiek te bekijken. U kunt bestaande gebruikers bewerken of verwijderen of nieuwe gebruikers maken, op voorwaarde dat u de juiste gebruikersrollen hebt toegewezen.
seo-title: Integratiegebruikers
title: Integratiegebruikers
uuid: 13dcb3fb-4561-409c-84da-943d0d390cf3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# Integratiegebruikers {#integration-users}

Gebruik de [!UICONTROL Integration Users] pagina om een lijst van gebruikers in uw configuratie van de Manager van de Publiek te bekijken. U kunt bestaande gebruikers bewerken of verwijderen of nieuwe gebruikers maken, op voorwaarde dat u de juiste gebruikersrollen hebt toegewezen.

<!-- c_integration_users.xml -->

U kunt elke kolom in stijgende of dalende orde sorteren door de gewenste kopbal van de kolom te klikken.
Gebruik het [!UICONTROL Search] vakje of de pagineringscontroles bij de bodem van de lijst om de gewenste gebruiker te vinden.

## Een gebruiker maken of bewerken {#create-edit-user}

Gebruik de [!UICONTROL Integration Users] pagina in het hulpprogramma Audience Manager [!UICONTROL Admin] om een nieuwe gebruiker te maken of om een bestaande gebruikersaccount te bewerken.

<!-- t_create_user.xml -->

>[!NOTE]
>
>U moet de [!UICONTROL CREATE_USER] rol hebben om nieuwe gebruikers tot stand te brengen. U moet de [!UICONTROL EDIT_USER] rol hebben om bestaande gebruikers uit te geven.

1. Als u een nieuwe gebruiker wilt maken, klikt u op **[!UICONTROL Integration Users]** > **[!UICONTROL Create a New User]**. Als u een bestaande gebruiker wilt bewerken, klikt u op de gewenste gebruiker in de **[!UICONTROL Username]** kolom.
2. Vul de velden in:
   * **[!UICONTROL First Name]**: (Vereist) Geef de voornaam van de gebruiker op.
   * **[!UICONTROL Last Name]**: (Vereist) Geef de achternaam van de gebruiker op.
   * **[!UICONTROL Username]**: (Vereist) Geef de gebruikersnaam van de gebruiker op.
   * **[!UICONTROL Email Address]**: (Vereist) Geef het e-mailadres van de gebruiker op.
   * **[!UICONTROL Phone Number]**: Geef het telefoonnummer van de gebruiker op.
   * **[!UICONTROL IMS ID]**: Geef de naam van de gebruiker op [!UICONTROL Internet Messaging Service ID].
   * **[!UICONTROL User Roles]**: Selecteer de gewenste gebruikersrollen:
      * **[!UICONTROL DEXADMIN]**: Verleent beheerdertoegang om taken in het [!UICONTROL Admin] hulpmiddel van de Manager van de Publiek uit te voeren. Als u deze optie niet selecteert, kunt u afzonderlijke rollen kiezen. Deze rollen laten gebruikers taken uitvoeren gebruikend [!DNL API] vraag, maar niet in het hulpmiddel Admin.
      * **[!UICONTROL CREATE_USERS]**: Laat gebruikers nieuwe gebruikers tot stand brengen gebruikend een [!DNL API] vraag.
      * **[!UICONTROL DELETE_USERS]**: Laat gebruikers bestaande gebruikers schrappen gebruikend een [!DNL API] vraag.
      * **[!UICONTROL EDIT_USERS]**: Laat gebruikers bestaande gebruikers uitgeven gebruikend een [!DNL API] vraag.
      * **[!UICONTROL VIEW_USERS]**: Laat gebruikers andere gebruikers in uw configuratie van de Manager van de Publiek bekijken gebruikend een [!DNL API] vraag.
      * **[!UICONTROL CREATE_PARTNERS]**: Laat gebruikers de partners van de Manager van het Publiek tot stand brengen gebruikend een [!DNL API] vraag.
      * **[!UICONTROL DELETE_PARTNERS]**: Laat gebruikers de partners schrappen van de Manager van het Publiek gebruikend een [!DNL API] vraag.
      * **[!UICONTROL EDIT_PARTNERS]**: Laat gebruikers de partners van de Manager van de Publiek uitgeven gebruikend een [!DNL API] vraag.
      * **[!UICONTROL VIEW_PARNTERS]**: Laat gebruikers de partners van de Manager van de Auditie bekijken gebruikend een [!DNL API] vraag.
   * **Status:** Schakel deze optie in **[!UICONTROL Active]** om van deze gebruiker een geactiveerde gebruiker van Audience Manager te maken.
3. Klik op **[!UICONTROL Submit]**.

## Een gebruiker verwijderen {#delete-user}

Gebruik de [!UICONTROL Integration Users] pagina in het [!UICONTROL Admin] gereedschap Auditiebeheer om een bestaande gebruiker te verwijderen.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>U moet de **[!UICONTROL DELETE_USER]** rol hebben om nieuwe gebruikers tot stand te brengen.

1. Klik op **[!UICONTROL Integration Users]**.
2. Klik ![](assets/icon_delete.png) in de **[!UICONTROL Actions]** kolom van de gewenste gebruiker.
3. Klik **[!UICONTROL OK]** om de verwijdering te bevestigen.