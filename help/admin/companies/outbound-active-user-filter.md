---
description: Volg deze instructies om een volledig synchronisatiedossier te produceren dat onlangs actieve gebruikers slechts omvat. U kunt desgewenst filteren op actieve gebruikers om relevante gegevens door te sturen naar een on-site doelsysteem of om de grootte van de bestanden die naar een DSP worden verzonden te beperken. U kunt dit filter niet gebruiken met incrementele synchronisatie.
seo-description: Volg deze instructies om een volledig synchronisatiedossier te produceren dat onlangs actieve gebruikers slechts omvat. U kunt desgewenst filteren op actieve gebruikers om relevante gegevens door te sturen naar een on-site doelsysteem of om de grootte van de bestanden die naar een DSP worden verzonden te beperken. U kunt dit filter niet gebruiken met incrementele synchronisatie.
seo-title: Uitgaande gegevens filteren op Alleen actieve gebruikers
title: Uitgaande gegevens filteren op Alleen actieve gebruikers
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Uitgaande gegevens filteren op Alleen actieve gebruikers {#filter-outbound-data-by-active-users-only}

Volg deze instructies om een volledig synchronisatiedossier te produceren dat onlangs actieve gebruikers slechts omvat. U kunt desgewenst filteren op actieve gebruikers om relevante gegevens door te sturen naar een on-site doelsysteem of om de grootte van de bestanden die naar een DSP worden verzonden te beperken. U kunt dit filter niet gebruiken met incrementele synchronisatie.

>[!NOTE]
>
>Een bezoeker hoeft niet op een geselecteerde klantsite of in zijn advertentieverkeer te worden gezien om als &quot;actief&quot; te worden beschouwd. Zij kunnen door om het even welke [!DNL Audience Manager] klant of partner worden gezien om als &quot;actief te kwalificeren.&quot;

Alleen door actieve gebruikers filteren:

1. Klik op **[!UICONTROL Companies]**.
1. Selecteer het bedrijf waarmee u wilt werken en klik op **[!UICONTROL Destinations]**.
1. Stel in de [!UICONTROL Batch Data] sectie de volgende opties in:

   * **[!UICONTROL Sync Type]**: Selecteer **[!UICONTROL Customer]** of **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Dit tijdinterval bepaalt de waaier van uw gegevensdossier. U kunt kiezen uit **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Selecteer **[!UICONTROL Never]**. Dit filter is alleen van toepassing op bestanden met volledige synchronisatie.
   * **[!UICONTROL Full Sync Scheduled Run]**: Hiermee bepaalt u hoe vaak u dit bestand wilt ontvangen. U kunt kiezen uit **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]** of **[!UICONTROL Never]** (uitschakelen).

1. Klik op **[!UICONTROL Save]**.
