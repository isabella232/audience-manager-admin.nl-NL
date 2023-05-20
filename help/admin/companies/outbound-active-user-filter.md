---
description: Volg deze instructies om een volledig synchronisatiedossier te produceren dat onlangs actieve gebruikers slechts omvat. U kunt desgewenst filteren op actieve gebruikers om relevante gegevens door te sturen naar een on-site doelsysteem of om de grootte van de bestanden die naar een DSP worden verzonden te beperken. U kunt dit filter niet gebruiken met incrementele synchronisatie.
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: Uitgaande gegevens alleen op actieve gebruikers filteren
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# Uitgaande gegevens alleen op actieve gebruikers filteren {#filter-outbound-data-by-active-users-only}

Volg deze instructies om een volledig synchronisatiedossier te produceren dat onlangs actieve gebruikers slechts omvat. U kunt desgewenst filteren op actieve gebruikers om relevante gegevens door te sturen naar een on-site doelsysteem of om de grootte van de bestanden die naar een DSP worden verzonden te beperken. U kunt dit filter niet gebruiken met incrementele synchronisatie.

>[!NOTE]
>
>Een bezoeker hoeft niet op een geselecteerde klantsite of in zijn advertentieverkeer te worden gezien om als &quot;actief&quot; te worden beschouwd. Ze kunnen door iedereen worden gezien [!DNL Audience Manager] klant of partner om als &quot;actief&quot;te kwalificeren.

Alleen door actieve gebruikers filteren:

1. Klik op **[!UICONTROL Companies]**.
1. Selecteer het bedrijf waarmee u wilt werken en klik op **[!UICONTROL Destinations]**.
1. In de [!UICONTROL Batch Data] de volgende opties instellen:

   * **[!UICONTROL Sync Type]**: Selecteren **[!UICONTROL Customer]** of **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: Dit tijdinterval bepaalt de waaier van uw gegevensdossier. Inclusief keuzen **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Selecteren **[!UICONTROL Never]**. Dit filter is alleen van toepassing op bestanden met volledige synchronisatie.
   * **[!UICONTROL Full Sync Scheduled Run]**: Hiermee bepaalt u hoe vaak u dit bestand wilt ontvangen. Inclusief keuzen **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**, of **[!UICONTROL Never]** (uit te schakelen).

1. Klik op **[!UICONTROL Save]**.
