---
description: Audience Managers maken, bewerken en verwijderen.
seo-description: Audience Managers maken, bewerken en verwijderen.
seo-title: Bedrijfsbestemmingen beheren
title: Bedrijfsbestemmingen beheren
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: f247457004a624297ddc8847dd256dbb7d8da418
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 1%

---


# Bedrijfsbestemmingen beheren {#manage-company-destinations}

Audience Managers maken, bewerken en verwijderen.

<!-- t_company_destinations.xml -->

Voor gedetailleerde informatie, zie [Doelen](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) in *de Gids van de Gebruiker van de Audience Manager*.

## Bedrijfsbestemmingen maken of bewerken {#create-edit-company-destinations}

Blader door de secties voor stapsgewijze instructies over hoe u nieuwe [!DNL Audience Manager]-doelen kunt maken of bestaande doelen kunt bewerken.

<!-- create-edit-company-destinations.xml -->

Bezoek de [Experience Cloud partner integratiepagina](https://wiki.corp.adobe.com/x/mPIMPw) alvorens bestemmingen te vestigen. De pagina bevat de specifieke informatie die u voor elke [!DNL Audience Manager] partnerintegratie moet invullen.

Als uw client [!DNL Adobe Media Optimizer] als doel in [!DNL Audience Manager] wil gebruiken, moet u dit instellen in [!DNL Adobe Media Optimizer].

## Navigeer naar het tabblad Doelen {#navigate-destinations}

1. Klik **[!UICONTROL Companies]**, dan bepaal de plaats en klik het gewenste bedrijf om zijn [!UICONTROL Profile] pagina te tonen. U kunt de [!UICONTROL Search] doos of de pagineringscontroles bij de bodem van de lijst gebruiken om het gewenste bedrijf te vinden. U kunt elke kolom in stijgende of dalende orde sorteren door de gewenste kopbal van de kolom te klikken.
1. Klik op het tabblad **[!UICONTROL Destinations]**.
1. Als u een nieuw doel wilt maken, klikt u op **[!UICONTROL Add Destination]**. Als u een bestaand doel wilt bewerken, klikt u op de naam van het doel in de kolom **[!UICONTROL Name]**.

## Basisinstellingen {#basic-settings}

Vul de velden in het venster **[!UICONTROL Basic Settings]** in.

* **[!UICONTROL Name]:** (Vereist) Geef de naam van dit doel op.
* **[!UICONTROL Description]:** Geef beschrijvende informatie op over deze bestemming.
* **[!UICONTROL Type]:** (Vereist) Selecteer het gewenste doeltype:
   * **[!UICONTROL Bulk ID]**: Synchroniseer id&#39;s tussen verschillende platforms.
   * **[!UICONTROL Bulk Trait]**: Verstuur onbewerkte gegevens naar verschillende platforms.
   * **[!UICONTROL Bulk Segment]**: Segmentinformatie bulksgewijs naar verschillende platforms verzenden.
   * **[!UICONTROL S2S]**: Gebruik server-aan-server bestemmingen om gegevens in real time en partijgegevens naar verschillende platforms te verzenden.
* **[!UICONTROL Auto-Fill Destination Mapping]:** (  [!UICONTROL S2S] alleen) Selecteer een optie:
   * **[!UICONTROL Segment ID]:** Als u deze het plaatsen selecteert, wordt de afbeelding van de bestemmingswaarde gevuld met identiteitskaart van het  [!DNL Audience Manager] Segment.
   * **[!UICONTROL Integration Code Value]:** Als u dit het plaatsen selecteert, wordt de afbeelding van de bestemmingswaarde gevuld met de de integratiecode van het  [!DNL Audience Manager] Segment.
* **[!UICONTROL User ID Key]:** (Vereist) Selecteer de gewenste sleutel van identiteitskaart voor deze bestemming van de drop-down lijst.

Deze id wordt gebruikt als de master gegevensbron-id. Hiermee bepaalt u welke gebruikers-id&#39;s in het bestand worden overtroffen.

>[!NOTE]
>
>Voor het [!UICONTROL Bulk ID] bestemmingstype, kunt u [!DNL Audience Manager] [!UICONTROL User ID] of [!DNL Adobe Experience Cloud] identiteitskaart niet gebruiken.

Als de gegevensbron-id ( [!UICONTROL DPID]) niet in de vervolgkeuzelijst wordt weergegeven, moet u het selectievakje **[!UICONTROL Outbound]** op gegevensbronniveau op de [pagina Instellingen gegevensbron](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html) inschakelen.

* **[!UICONTROL Target Data Source]:** (Vereist) Selecteer de gewenste gegevensbron voor deze bestemming van de drop-down lijst. Met deze instelling wordt de etikettering van buitenaf gemaakte gegevens ingeschakeld, waardoor inname in afzonderlijke systemen aan de zijde van de client mogelijk is.
* **[!UICONTROL Foreign Account ID]:** Geef de externe account-id voor deze bestemming op. Dit is de identificatiewaarde in het systeem van de ontvanger voor deze outbounded gegevens.
* **[!UICONTROL Outbound Sample Rate Denominator]:** Wanneer de totale hoeveelheid geretourneerde gegevens onbekend is, gebruikt u deze instelling om alleen een voorbeeldhoeveelheid gegevens te retourneren in plaats van de volledige hoeveelheid. Pas hier het getal aan dat een fractie van de gegevens vertegenwoordigt (een waarde &#39;100&#39; retourneert bijvoorbeeld 1/100e van de normale hoeveelheid gegevens, een waarde &#39;10&#39; retourneert een tiende van de normale hoeveelheid gegevens). De standaardwaarde is &#39;1&#39;, die alle gegevens retourneert.

## Realtime-gegevens (voor S2S-doelen) {#realtime-s2s}

Als u een [!UICONTROL S2S] bestemming creeert, vul de hieronder gebieden in:

**[!UICONTROL Servers]**: Selecteer de gewenste  `HTTP` server voor deze bestemming.
**[!UICONTROL Format]**: Selecteer de gewenste indeling voor dit doel in de vervolgkeuzelijst:  [!UICONTROL HTTP only].

>[!NOTE]
>
>Alleen voor [!DNL S2S] kunt u [!UICONTROL Realtime]- of [!UICONTROL Batch]-doelen in- of uitschakelen met de schuifregelaars voor Uit/Aan op het scherm. U kunt beide opties niet uitschakelen.

## Batchgegevens {#batch-data}

Vul voor [!UICONTROL Bulk ID]-, [!UICONTROL Bulk Trait]- of [!UICONTROL Bulk Segment]-doelen de onderstaande velden in:

* **[!UICONTROL Protocol]**: (Vereist) Selecteer het gewenste protocol voor deze bestemming van de drop-down lijst:
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (Vereist) Selecteer de gewenste server voor deze bestemming van de drop-down lijst.
* **[!UICONTROL Format]**: (Vereist) Selecteer het gewenste formaat voor deze bestemming van de drop-down lijst:  [!DNL HTTP] of bestandstype, afhankelijk van het protocol dat u hierboven hebt gekozen.
* **[!UICONTROL Sync Type]**: (Vereist) Selecteer het gewenste synchronisatietype voor deze bestemming. Dit wijst op het niveau van gebruikersactiviteiten cliënten in de uitgaande orden zouden willen omvatten. Selecteer **[!UICONTROL Customer]** als clients alleen geïnteresseerd zijn in het analyseren van segmentkwalificaties op basis van hun eigenschappen. Selecteer **[!UICONTROL Platform]** als zij segmentkwalificaties van offsite activiteiten in alle [!DNL Audience Manager] klanten willen opnemen.
* **[!UICONTROL Customer]**: Het bestand bevat actieve gebruikers die voor de geselecteerde tijdsperiode ten minste één kenmerk hebben dat alleen kan worden gerealiseerd op de eigenschappen van de client (gekoppeld aan de client  [!UICONTROL PID]). Uw cliënten zouden deze optie moeten gebruiken om hun *real-time* segmentkwalificaties aan bestemmingen uit te zenden.
* **[!UICONTROL Platform]**: Het dossier bevat actieve gebruikers die minstens 1 interactie in real time hebben, of het synchroon van identiteitskaart of de verwezenlijking van het bezit, overal over alle eigenschappen van  [!DNL Audience Manager] cliënten (verbonden aan alle cliëntPIDs) voor de geselecteerde tijdspanne. Uw cliënten zouden deze optie moeten gebruiken om hun *total* segmentkwalificaties aan bestemmingen uit te zenden.
* **[!UICONTROL Lifetime]**: Het bestand bevat actieve gebruikers die overal op de eigenschappen van alle  [!DNL Audience Manager] clients worden gezien sinds het maken van het doel.
* **[!UICONTROL Sync Type Lookback Period]**: Als u een tijdsperiode selecteert  [!UICONTROL Customer] of  [!UICONTROL Platform]selecteert. Bestanden bevatten actieve gebruikers voor de geselecteerde tijdsperiode.
Selecteer vervolgens het ordertype. Dit wijst op de frequentie en het werkingsgebied van elke uitgaande integratie met partners. Selecteer tussen incrementele en volledige bestellingen.
* **[!UICONTROL Incremental Scheduled Run]**: Met elke looppas,  [!DNL Audience Manager] zal slechts de netto nieuwe gebruikers verlaten die sinds de vorige uitgaande orde worden gekwalificeerd. Selecteer de gewenste tijdsperiode die [!DNL Audience Manager] incrementele synchronisatieprocessen moet uitvoeren. U kunt bijvoorbeeld elke 24 uur selecteren, elke 7 dagen, elke 30 dagen of nooit.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>De eerste incrementele volgorde is gelijk aan een volledige volgorde, omdat er nooit eerder gebruikers naar de bestemming zijn gestuurd.

* **[!UICONTROL Full Sync Scheduled Run]**: Met elke looppas,  [!DNL Audience Manager] zal alle actieve gebruikers uitgaand aangezien de bestemming eerst opstelling was. Selecteer het gewenste programma dat u [!DNL Audience Manager] wilt gebruiken om volledige synchronisatieprocessen uit te voeren. U kunt bijvoorbeeld elke 24 uur selecteren, elke 7 dagen, elke 30 dagen of nooit.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>We raden u aan incrementele syncs vaker te gebruiken dan volledige syncs. Met incrementele syncs worden alleen bestanden verzonden die nieuwe functies of id-syncs bevatten. Met Volledige syntaxis worden alle bestanden verzonden, ongeacht of deze nieuwe realisaties of id-syncs bevatten. Gebruik alleen de [!UICONTROL Full Sync Scheduled Run]-configuratie wanneer clients een volledige kopie van alle gebruikers nodig hebben om het uitgaande gegevensvolume te verminderen.

## Gegevensbronnen {#configure-data-sources} configureren

Vul voor [!UICONTROL Bulk ID]-, [!UICONTROL Bulk Trait]- of [!UICONTROL Bulk Segment]-doelen de onderstaande velden in. Met deze instellingen kunt u alle gegevens (kenmerken, segmenten of id&#39;s op basis van het geselecteerde type) verzenden die aan de gegevensbronnen zijn gekoppeld.

* **[!UICONTROL All Unrestricted First Party Data]**: Selecteer deze optie om alle gegevensbronnen van de eerste partij te gebruiken. Als u deze optie selecteert, worden de [!UICONTROL Available Data Sources] opties onbruikbaar gemaakt.
* **[!UICONTROL Available Data Sources]**: Gebruik de pijlen om gegevensbronnen tussen de  **[!UICONTROL Available Data Sources]** vakken en de  **[!UICONTROL In File Data Sources]** vakken te verplaatsen.

## {#save-and-finalize} opslaan en voltooien

De knop **[!UICONTROL Save]** wordt geactiveerd nadat alle vereiste velden zijn ingevuld. Klik **[!UICONTROL Save]** om te voltooien creeer bestemmingsproces.

## Bedrijfsdoelen {#delete-company-destinations} verwijderen

<!-- delete-company-destinations.xml -->

Een doel verwijderen:

1. Klik **[!UICONTROL Companies]**, bepaal de plaats en klik het gewenste bedrijf, dan klik **[!UICONTROL Destinations]** tabel.
1. Klik ![](assets/icon_delete.png) in **[!UICONTROL Actions]** kolom van de gewenste bestemming.
1. Klik **[!UICONTROL OK]** om de schrapping te bevestigen.

>[!NOTE]
>
>U kunt een doel niet verwijderen als er segmenten aan zijn toegewezen.