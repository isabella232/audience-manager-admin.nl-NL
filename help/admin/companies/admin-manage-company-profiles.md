---
description: Gebruik de pagina van Bedrijven in het hulpmiddel van Admin van de Audience Manager om een nieuw bedrijf tot stand te brengen.
seo-description: Use the Companies page in the Audience Manager Admin tool to create a new company.
seo-title: Create a Company Profile
title: Een bedrijfsprofiel maken
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
exl-id: 80bb8a89-0207-4645-ac42-e73cd10561de
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 1%

---

# Een bedrijfsprofiel maken {#create-a-company-profile}

Gebruik de [!UICONTROL Companies] pagina in het hulpmiddel Admin van de Audience Manager om een nieuw bedrijf tot stand te brengen.

<!-- t_create_company.xml -->

>[!NOTE]
>
>U moet beschikken over de **[!UICONTROL DEXADMIN]** de rol om nieuwe ondernemingen op te richten.

1. Klik op **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. Vul de velden in:

   * **[!UICONTROL Name]**: (Vereist) Geef de naam van de onderneming op.
   * **[!UICONTROL Description]**: (Vereist) Geef beschrijvende informatie over de onderneming, zoals de industrie of haar volledige naam.
   * **[!UICONTROL Subdomain]**: (Vereist) Geef het subdomein van het bedrijf op. De tekst die u invoert, wordt weergegeven als het subdomein van de gebeurtenisaanroep. Dit kan niet worden gewijzigd. Het moet een tekenreeks zijn [!DNL URL]-valid characters.

      Als uw bedrijf bijvoorbeeld een naam heeft gekregen [!DNL AcmeCorp]het subdomein [!DNL acmecorp].

      Audience Manager gebruikt het subdomein voor de [!UICONTROL Data Collection Server] (DCS). In het vorige voorbeeld, als uw bedrijf volledig is [!DNL URL] in [!UICONTROL DCS] zou [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: Geef het gewenste werkgebied voor het bedrijf op:
      * **[!UICONTROL Active]**: Specificeer dat het bedrijf een actieve cliënt van de Audience Manager zal zijn. An [!UICONTROL Active] rekening: een betalende klant, niet alleen voor advies, maar voor de Audience Manager SKU.
      * **[!UICONTROL Demo]**: Geef op dat het bedrijf alleen voor demo-doeleinden zal worden gebruikt. Gegevens worden automatisch gerapporteerd.
      * **[!UICONTROL Prospect]**: Specificeer dat de onderneming een potentiële cliënt van de Audience Manager is, zoals een onderneming die een vrije [!DNL POC] of een accountinstelling voor een verkoopdemo.
      * **[!UICONTROL Test]**: Geef op dat het bedrijf alleen voor interne tests wordt gebruikt.
   * **[!UICONTROL Account Types]**: Geef de volledige set accounttypen voor dit bedrijf op. Geen accounttype sluit elkaar uit met een ander type.
      * **[!UICONTROL Full AAM]**: Geef op dat het bedrijf een volledige Adobe Audience Manager-account heeft en dat gebruikers toegang tot de aanmelding hebben.
      * **[!UICONTROL MMP]**: Geef op dat het bedrijf de [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]). De [!UICONTROL MMP] staat toe om publiek over de Experience Cloud te delen die [!UICONTROL Experience Cloud ID] ([!DNL MCID]) die aan elke bezoeker wordt toegewezen en vervolgens door Audience Manager wordt gebruikt. Als u dit accounttype selecteert, wordt [!UICONTROL Experience Cloud ID Service] wordt ook automatisch geselecteerd.

         Zie voor meer informatie [Experience Cloud publiek](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**: Specificeer dat het bedrijf een derde gegevensleverancier binnen Audience Manager is.
   * **[!UICONTROL Targeting Partner]**: Specificeer dat de onderneming als doelplatform voor klanten van de Audience Manager handelt.
   * **[!UICONTROL Visitor ID Service]**: Geef op dat het bedrijf de [!UICONTROL Experience Cloud Visitor ID Service].

      De [!UICONTROL Experience Cloud Visitor ID Service] biedt een universele bezoeker-id voor alle Experience Cloud-oplossingen. Zie voor meer informatie de [Gebruikershandleiding voor Experience Cloud-bezoekersidentiteitskaart](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en).

   * **[!UICONTROL Agency]**: Geef op dat het bedrijf een [!UICONTROL Agency] account.



1. Klik op **[!UICONTROL Create]**. Doorgaan met de instructies in [Een bedrijfsprofiel bewerken](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![Stap resultaat](assets/add_company.png)

## Een bedrijfsprofiel bewerken {#edit-company-profile}

Bewerk het profiel van een bedrijf, inclusief de naam, beschrijving, subdomein, levenscyclus en meer.

<!-- t_edit_company_profile.xml -->

1. Klikken **[!UICONTROL Companies]** en klik vervolgens op het gewenste bedrijf om het [!UICONTROL Profile] pagina.

   Gebruik de [!UICONTROL Search] of de pagineringscontroles bij de bodem van de lijst om het gewenste bedrijf te vinden. U kunt elke kolom in stijgende of dalende orde sorteren door de gewenste kopbal van de kolom te klikken.

   ![Stap resultaat](assets/profile_company.png)

1. Bewerk indien nodig de velden:

   * **[!UICONTROL Name]**: Bewerk de naam van het bedrijf. Dit is een verplicht veld.
   * **[!UICONTROL Description]**: Bewerk de beschrijving van het bedrijf. Dit is een verplicht veld.
   * **[!UICONTROL Subdomain]**: (Vereist) Geef het subdomein van het bedrijf op. De tekst die u invoert, wordt weergegeven als het subdomein van de gebeurtenisaanroep. Dit kan niet worden gewijzigd. Het moet een tekenreeks zijn [!DNL URL]-valid characters.

      Als uw bedrijf bijvoorbeeld een naam heeft gekregen [!DNL AcmeCorp]het subdomein [!DNL acmecorp].

      Audience Manager gebruikt het subdomein voor de [!UICONTROL Data Collection Server] (DCS). In het vorige voorbeeld, als uw bedrijf volledig is [!DNL URL] in [!UICONTROL DCS] zou [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Met deze id kunt u verbinding maken met uw bedrijf en de Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Geef het gewenste werkgebied voor het bedrijf op:
      * **[!UICONTROL Active]**: Specificeer dat het bedrijf een actieve cliënt van de Audience Manager zal zijn. Een actieve rekening betekent een betalende klant, niet alleen voor raadpleging, maar voor Audience Manager SKU.
      * **[!UICONTROL Demo]**: Geef op dat het bedrijf alleen voor demo-doeleinden zal worden gebruikt. Gegevens worden automatisch gerapporteerd.
      * **[!UICONTROL Prospect]**: Specificeer dat de onderneming een potentiële cliënt van de Audience Manager is, zoals een onderneming die een vrije [!DNL POC] of een accountinstelling voor een verkoopdemo.
      * **[!UICONTROL Test]**: Geef op dat het bedrijf alleen voor interne tests wordt gebruikt.
   * **[!UICONTROL Account Types]**: Geef de volledige set accounttypen voor dit bedrijf op. Geen accounttype sluit elkaar uit met een ander type.
      * **[!UICONTROL Full AAM]**: Geef op dat het bedrijf een volledige Adobe Audience Manager-account heeft en dat gebruikers toegang tot de aanmelding hebben.
      * **[!UICONTROL MMP]**: Geef op dat het bedrijf het Master marketingprofiel mag gebruiken ([!UICONTROL MMP]).

         Als u dit accounttype selecteert, **[!UICONTROL Visitor ID Service]** wordt ook automatisch geselecteerd.
Zie voor meer informatie [Experience Cloud publiek](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html?lang=en).
   * **[!UICONTROL Data Source]**: Specificeer dat het bedrijf een derde gegevensleverancier binnen Audience Manager is.
   * **[!UICONTROL Targeting Partner]**: Specificeer dat de onderneming als doelplatform voor klanten van de Audience Manager handelt.
   * **[!UICONTROL Visitor ID Service]**: Specificeer dat het bedrijf is toegelaten om de Dienst van identiteitskaart van de Bezoeker van Experience Cloud te gebruiken.

      De dienst van identiteitskaart van de Bezoeker van Experience Cloud verstrekt universele bezoekersidentiteitskaart over Experience Cloud oplossingen. Zie voor meer informatie de [Gebruikershandleiding voor Experience Cloud ID-service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en).

   * **[!UICONTROL Agency]**: Geef op dat de onderneming een account van het Agentschap heeft.
   * **[!UICONTROL Features]**: Selecteer de gewenste opties:
      * **[!UICONTROL Password Expiration]**: Plaatst alle gebruikerswachtwoorden binnen dit bedrijf om na 90 dagen te verlopen om de veiligheid van de Audience Manager te verhogen.
      * **[!UICONTROL Reporting]**: Laat Audience Manager rapportering voor dit bedrijf toe.
      * **[!UICONTROL Role Based Access Controls]**: Schakel op rol gebaseerde toegangsbesturingselementen voor dit bedrijf in. Op rol-gebaseerde toegangscontroles laten u gebruikersgroepen met verschillende toegangstoestemmingen tot stand brengen. De individuele gebruikers binnen deze groepen kunnen tot slechts specifieke eigenschappen in Audience Manager dan toegang hebben.


1. Klik op **[!UICONTROL Submit Updates]**.

## Een bedrijfsprofiel verwijderen {#delete-company-profile}

Gebruik de [!UICONTROL Companies] pagina in de Audience Manager [!UICONTROL Admin] om een bestaand bedrijf te verwijderen.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>U moet beschikken over de [!UICONTROL DEXADMIN] rol om bestaande ondernemingen te schrappen.

1. Als u een bestaand bedrijf wilt verwijderen, klikt u op **[!UICONTROL Companies]**.

   ![Stap resultaat](assets/companies.png)

1. Klikken  ![](assets/icon_delete.png) in de **[!UICONTROL Actions]** kolom van het gewenste bedrijf.
1. Klikken **[!UICONTROL OK]** om de schrapping te bevestigen.
