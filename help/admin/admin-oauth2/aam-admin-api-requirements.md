---
description: Dingen u uw cliënten zou moeten aanmoedigen om zich bewust te zijn van wanneer zij met Audience Manager APIs werken.
seo-description: Dingen u uw cliënten zou moeten aanmoedigen om zich bewust te zijn van wanneer zij met Audience Manager APIs werken.
seo-title: API-vereisten en -aanbevelingen
title: API-vereisten en -aanbevelingen
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# API-vereisten en -aanbevelingen {#api-requirements-and-recommendations}

Dingen u uw cliënten zou moeten aanmoedigen om zich bewust te zijn van wanneer zij met de Audience Manager [!DNL API]s werken.

## Vereisten {#requirements}

Let op het volgende wanneer u werkt met [!DNL Audience Manager] [!DNL API] code:

* **Request-parameters:** alle request-parameters zijn vereist, tenzij anders opgegeven.
* **[!DNL JSON]inhoudssoort:** Geef  `content-type: application/json` ** `accept: application/json` en in de code op.

* **Verzoeken en reacties:** Verstuur aanvragen als een correct opgemaakt  [!DNL JSON] object. [!DNL Audience Manager] reageert met  [!DNL JSON] opgemaakte gegevens. Serverreacties kunnen gevraagde gegevens, een statuscode of beide bevatten.

* **Toegang:** Uw  [!DNL Audience Manager] consultant geeft u een client-id en sleutel waarmee u  [!DNL API] aanvragen kunt indienen.

* **Documentatie en codevoorbeelden:** Tekst in  ** cursief vertegenwoordigt een variabele die u opgeeft of doorgeeft bij het maken of ontvangen van  [!DNL API] gegevens. Vervang *cursieve* tekst met uw eigen code, parameters, of andere vereiste informatie.

## Recommendations: Een generieke API-gebruiker maken {#recommendations}

We raden u aan een aparte, technische gebruikersaccount te maken voor het werken met de Audience Manager [!DNL API]s. Dit is een generische account die niet is gekoppeld aan of gekoppeld aan een specifieke gebruiker in de organisatie van uw klant. Met dit type gebruikersaccount van [!DNL API] kunt u twee dingen bereiken:

* Identificeer welke dienst [!DNL API] roept (b.v., vraag van een cliënttoepassing die onze [!DNL API]s of van het aanbrengen van bulkveranderingen gebruikt).
* Ononderbroken toegang tot de [!DNL API]s bieden. Een rekening die aan een specifieke werknemer is gebonden, kan worden geschrapt wanneer zij het bedrijf verlaten. Hierdoor kunnen uw klanten niet met de beschikbare [!DNL API]-code werken. Dit probleem wordt voorkomen door een algemeen account dat niet aan een bepaalde werknemer is gekoppeld.

Als voorbeeld of gebruiksgeval voor dit type van rekening, laten wij zeggen uw klanten een heleboel segmenten in één keer met [Bulk de Hulpmiddelen van het Beheer willen veranderen](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). Om dit te doen, hebben zij [!DNL API] toegang nodig. In plaats van toestemmingen aan een specifieke gebruiker toe te voegen, creeer een niet-specifieke, [!DNL API] gebruikersrekening die de aangewezen geloofsbrieven, de sleutel, en het geheim heeft om [!DNL API] vraag te maken. Dit is ook handig als de client eigen toepassingen ontwikkelt die de [!DNL Audience Manager] [!DNL API]s gebruiken.
