---
description: Om toevallig dossier en gegevens te verhinderen in doelgegevensbronnen die door andere partners of klanten worden bezeten, heeft de Audience Manager een kaartvereiste tussen partner identiteitskaart (PID) en de gegevensbronnen toegevoegd die door andere partners worden bezeten.
title: Toegang aan boord beheren voor gegevens van andere leveranciers
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Toegang aan boord beheren voor gegevens van een tweede partij {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> Het publiek voor deze pagina is Adobe-interne werknemers. Als u een klant van de Audience Manager bent die om een tweede-partijgegevenstoewijzing zoals die op deze pagina wordt beschreven verzoekt, contacteer de Zorg van de Klant of uw Technische Manager van de Rekening.
> Merk op dat niet wordt vereist om een afbeelding voor bestaande gegevens te verzoeken delend verhoudingen. De toewijzing wordt ook niet vereist wanneer het aan boord gaan van gegevens in doelgegevensbronnen die tot uw PID behoren.

Om toevallig dossier en gegevens te verhinderen in doelgegevensbronnen die door andere partners worden bezeten, heeft de Audience Manager een kaartvereiste tussen partner identiteitskaart (PID) en de gegevensbronnen (DPID) toegevoegd die door andere partners worden bezeten. Lees meer over PID en DPID in [index van Audience Manager-id&#39;s](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

Voor de doeleinden van het delen van gegevens van de tweede partij, als een partner van de Audience Manager of een klant dossiers in een doelgegevensbron willen opnemen die zij niet hebben, dan moeten zij om een afbeelding tussen hun partnerID (PID) en die specifieke gegevensbron (DPID) verzoeken. Als de toewijzing ontbreekt, worden de bestanden niet verwerkt door de binnenkomende gegevenstaak en worden de gegevens niet in de Audience Manager opgenomen.

Om die afbeelding tot stand te brengen, dient u een Jira-ticket in bij het technische team van de Audience Manager. Een Jira-voorbeeldticket bekijken [hier](https://jira.corp.adobe.com/browse/AAM-60353). U hoeft geen toewijzingen op te vragen die moeten worden gemaakt voor bestaande relaties voor het delen van gegevens.
