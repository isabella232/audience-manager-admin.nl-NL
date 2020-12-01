---
description: Gebruik de pagina van Bedrijven in het hulpmiddel van Admin van de Audience Manager om een nieuw bedrijf tot stand te brengen.
seo-description: Gebruik de pagina van Bedrijven in het hulpmiddel van Admin van de Audience Manager om een nieuw bedrijf tot stand te brengen.
seo-title: Een bedrijfsprofiel maken
title: Een bedrijfsprofiel maken
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
translation-type: tm+mt
source-git-commit: 69b733ae869b3dded76f0264e395f0157b445148
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 1%

---


# Een bedrijfsprofiel maken {#create-a-company-profile}

Gebruik de pagina [!UICONTROL Companies] in het hulpmiddel van Admin van de Audience Manager om een nieuw bedrijf tot stand te brengen.

<!-- t_create_company.xml -->

>[!NOTE]
>
>U moet de **[!UICONTROL DEXADMIN]** rol hebben om nieuwe bedrijven tot stand te brengen.

1. Klik op **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. Vul de velden in:

   * **[!UICONTROL Name]**: (Vereist) Geef de naam van de onderneming op.
   * **[!UICONTROL Description]**: (Vereist) Geef beschrijvende informatie over de onderneming, zoals de industrie of haar volledige naam.
   * **[!UICONTROL Subdomain]**: (Vereist) Geef het subdomein van het bedrijf op. De tekst die u invoert, wordt weergegeven als het subdomein van de gebeurtenisaanroep. Dit kan niet worden gewijzigd. Het moet een tekenreeks van [!DNL URL]-geldige tekens zijn.

      Bijvoorbeeld, als uw bedrijf [!DNL AcmeCorp] werd genoemd, zou subdomain [!DNL acmecorp] zijn.

      Audience Manager gebruikt subdomain voor [!UICONTROL Data Collection Server] (DCS). In het vorige voorbeeld, als de volledige [!DNL URL] in [!UICONTROL DCS] [!DNL acmecorp.demdex.net] zou zijn.

   * **[!UICONTROL Lifecyle]**: Geef het gewenste werkgebied voor het bedrijf op:
      * **[!UICONTROL Active]**: Specificeer dat het bedrijf een actieve cliënt van de Audience Manager zal zijn. Een [!UICONTROL Active]-account betekent een betalende klant, niet alleen voor advies, maar ook voor de Audience Manager SKU.
      * **[!UICONTROL Demo]**: Geef op dat het bedrijf alleen voor demo-doeleinden zal worden gebruikt. Gegevens worden automatisch gerapporteerd.
      * **[!UICONTROL Prospect]**: Specificeer dat de onderneming een potentiële cliënt van de Audience Manager is, zoals een onderneming die een vrije  [!DNL POC] of een rekeningsopstelling voor een verkoopdemo wordt gegeven.
      * **[!UICONTROL Test]**: Geef op dat het bedrijf alleen voor interne tests wordt gebruikt.
   * **[!UICONTROL Account Types]**: Geef de volledige set accounttypen voor dit bedrijf op. Geen accounttype sluit elkaar uit met een ander type.
      * **[!UICONTROL Full AAM]**: Geef op dat het bedrijf een volledige Adobe Audience Manager-account heeft en dat gebruikers toegang tot de aanmelding hebben.
      * **[!UICONTROL MMP]**: Specificeer dat het bedrijf is toegelaten om de  [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP]) mogelijkheden te gebruiken. Met [!UICONTROL MMP] kunnen soorten publiek via de Experience Cloud worden gedeeld met een [!UICONTROL Experience Cloud ID] ([!DNL MCID]) die aan elke bezoeker is toegewezen en vervolgens door de Audience Manager wordt gebruikt. Als u dit accounttype selecteert, wordt [!UICONTROL Experience Cloud ID Service] ook automatisch geselecteerd.

         Zie [Soorten publiek - Master marketingprofiel](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) voor meer informatie.
   * **[!UICONTROL Data Source]**: Specificeer dat het bedrijf een derde gegevensleverancier binnen Audience Manager is.
   * **[!UICONTROL Targeting Partner]**: Specificeer dat de onderneming als doelplatform voor klanten van de Audience Manager handelt.
   * **[!UICONTROL Visitor ID Service]**: Geef op dat het bedrijf de  [!UICONTROL Experience Cloud Visitor ID Service]functie mag gebruiken.

      [!UICONTROL Experience Cloud Visitor ID Service] verstrekt een universele bezoekersidentiteitskaart over Experience Cloud oplossingen. Raadpleeg de gebruikershandleiding [Experience Cloud-bezoeker-id Service](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html) voor meer informatie.

   * **[!UICONTROL Agency]**: Geef op dat het bedrijf een  [!UICONTROL Agency] account krijgt.



1. Klik op **[!UICONTROL Create]**. Ga met de instructies in [geef een Profiel van het Bedrijf](../companies/admin-manage-company-profiles.md#edit-company-profile) uit.

   ![Stap resultaat](assets/add_company.png)

## Een bedrijfsprofiel bewerken {#edit-company-profile}

Bewerk het profiel van een bedrijf, inclusief de naam, beschrijving, subdomein, levenscyclus en meer.

<!-- t_edit_company_profile.xml -->

1. Klik **[!UICONTROL Companies]**, dan bepaal de plaats en klik het gewenste bedrijf om zijn [!UICONTROL Profile] pagina te tonen.

   Gebruik de doos [!UICONTROL Search] of de pagineringscontroles bij de bodem van de lijst om het gewenste bedrijf te vinden. U kunt elke kolom in stijgende of dalende orde sorteren door de gewenste kopbal van de kolom te klikken.

   ![Stap resultaat](assets/profile_company.png)

1. Bewerk indien nodig de velden:

   * **[!UICONTROL Name]**: Bewerk de naam van het bedrijf. Dit is een verplicht veld.
   * **[!UICONTROL Description]**: Bewerk de beschrijving van het bedrijf. Dit is een verplicht veld.
   * **[!UICONTROL Subdomain]**: (Vereist) Geef het subdomein van het bedrijf op. De tekst die u invoert, wordt weergegeven als het subdomein van de gebeurtenisaanroep. Dit kan niet worden gewijzigd. Het moet een tekenreeks van [!DNL URL]-geldige tekens zijn.

      Bijvoorbeeld, als uw bedrijf [!DNL AcmeCorp] werd genoemd, zou subdomain [!DNL acmecorp] zijn.

      Audience Manager gebruikt subdomain voor [!UICONTROL Data Collection Server] (DCS). In het vorige voorbeeld, als de volledige [!DNL URL] in [!UICONTROL DCS] [!DNL acmecorp.demdex.net] zou zijn.

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Met deze id kunt u verbinding maken met uw bedrijf en de Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Geef het gewenste werkgebied voor het bedrijf op:
      * **[!UICONTROL Active]**: Specificeer dat het bedrijf een actieve cliënt van de Audience Manager zal zijn. Een actieve rekening betekent een betalende klant, niet alleen voor raadpleging, maar voor Audience Manager SKU.
      * **[!UICONTROL Demo]**: Geef op dat het bedrijf alleen voor demo-doeleinden zal worden gebruikt. Gegevens worden automatisch gerapporteerd.
      * **[!UICONTROL Prospect]**: Specificeer dat de onderneming een potentiële cliënt van de Audience Manager is, zoals een onderneming die een vrije  [!DNL POC] of een rekeningsopstelling voor een verkoopdemo wordt gegeven.
      * **[!UICONTROL Test]**: Geef op dat het bedrijf alleen voor interne tests wordt gebruikt.
   * **[!UICONTROL Account Types]**: Geef de volledige set accounttypen voor dit bedrijf op. Geen accounttype sluit elkaar uit met een ander type.
      * **[!UICONTROL Full AAM]**: Geef op dat het bedrijf een volledige Adobe Audience Manager-account heeft en dat gebruikers toegang tot de aanmelding hebben.
      * **[!UICONTROL MMP]**: Geef op dat het bedrijf de mogelijkheden van het Master marketingprofiel ([!UICONTROL MMP]) mag gebruiken.

         Als u dit accounttype selecteert, wordt **[!UICONTROL Visitor ID Service]** ook automatisch geselecteerd.
Zie [Soorten publiek - Master marketingprofiel](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) voor meer informatie.
   * **[!UICONTROL Data Source]**: Specificeer dat het bedrijf een derde gegevensleverancier binnen Audience Manager is.
   * **[!UICONTROL Targeting Partner]**: Specificeer dat de onderneming als doelplatform voor klanten van de Audience Manager handelt.
   * **[!UICONTROL Visitor ID Service]**: Specificeer dat het bedrijf is toegelaten om de Dienst van identiteitskaart van de Bezoeker van Experience Cloud te gebruiken.

      De dienst van identiteitskaart van de Bezoeker van Experience Cloud verstrekt universele bezoekersidentiteitskaart over Experience Cloud oplossingen. Raadpleeg de gebruikershandleiding [Experience Cloud-bezoeker-id Service](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html) voor meer informatie.

   * **[!UICONTROL Agency]**: Geef op dat de onderneming een account van het Agentschap heeft.
   * **[!UICONTROL Features]**: Selecteer de gewenste opties:
      * **[!UICONTROL Password Expiration]**: Plaatst alle gebruikerswachtwoorden binnen dit bedrijf om na 90 dagen te verlopen om de veiligheid van de Audience Manager te verhogen.
      * **[!UICONTROL Reporting]**: Laat Audience Manager rapportering voor dit bedrijf toe.
      * **[!UICONTROL Role Based Access Controls]**: Schakel op rol gebaseerde toegangsbesturingselementen voor dit bedrijf in. Op rol-gebaseerde toegangscontroles laten u gebruikersgroepen met verschillende toegangstoestemmingen tot stand brengen. De individuele gebruikers binnen deze groepen kunnen tot slechts specifieke eigenschappen in Audience Manager dan toegang hebben.


1. Klik op **[!UICONTROL Submit Updates]**.

## Een bedrijfsprofiel {#delete-company-profile} verwijderen

Gebruik de [!UICONTROL Companies] pagina in de Audience Manager [!UICONTROL Admin] hulpmiddel om een bestaand bedrijf te schrappen.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>U moet de rol [!UICONTROL DEXADMIN] hebben om bestaande bedrijven te schrappen.

1. Als u een bestaand bedrijf wilt verwijderen, klikt u op **[!UICONTROL Companies]**.

   ![Stap resultaat](assets/companies.png)

1. Klik ![](assets/icon_delete.png) in **[!UICONTROL Actions]** kolom van het gewenste bedrijf.
1. Klik **[!UICONTROL OK]** om de schrapping te bevestigen.
