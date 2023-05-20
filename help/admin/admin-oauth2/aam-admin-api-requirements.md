---
description: Dingen u uw cliënten zou moeten aanmoedigen om zich bewust te zijn van wanneer zij met Audience Manager APIs werken.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API-vereisten en -aanbevelingen
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# API-vereisten en -aanbevelingen {#api-requirements-and-recommendations}

Dingen u uw klanten zou moeten aanmoedigen om zich bewust te zijn van wanneer zij met de Audience Manager werken [!DNL API]s.

## Vereisten {#requirements}

Let op het volgende wanneer u werkt met [!DNL Audience Manager] [!DNL API] code:

* **Parameters aanvragen:** Alle verzoekparameters worden vereist tenzij anders gespecificeerd.
* **[!DNL JSON]inhoudstype:** Opgeven `content-type: application/json` *en* `accept: application/json` in uw code.

* **Verzoeken en antwoorden:** Aanvragen verzenden als een correct opgemaakt bestand [!DNL JSON] object. [!DNL Audience Manager] reageert met [!DNL JSON] opgemaakte gegevens. Serverreacties kunnen gevraagde gegevens, een statuscode of beide bevatten.

* **Toegang:** Uw [!DNL Audience Manager] consultant zal u een klant-id en een sleutel geven waarmee u [!DNL API] verzoeken.

* **Documentatie en codevoorbeelden:** Tekst in *cursief* vertegenwoordigt een variabele die u verstrekt of binnen overgaat wanneer het maken of het ontvangen [!DNL API] gegevens. Vervangen *cursief* tekst met uw eigen code, parameters of andere vereiste informatie.

## Recommendations: Een generieke API-gebruiker maken {#recommendations}

We raden u aan een aparte, technische gebruikersaccount te maken voor het werken met de Audience Manager [!DNL API]s. Dit is een generische account die niet is gekoppeld aan of gekoppeld aan een specifieke gebruiker in de organisatie van uw klant. Dit type van [!DNL API] Met gebruikersaccount kunt u twee dingen bereiken:

* Identificeer welke dienst roept [!DNL API] (Bijvoorbeeld, vraag van een cliënttoepassing die onze [!DNL API]s of van het aanbrengen van bulkwijzigingen).
* Ononderbroken toegang tot de [!DNL API]s. Een rekening die aan een specifieke werknemer is gebonden, kan worden geschrapt wanneer zij het bedrijf verlaten. Hierdoor kunnen uw klanten niet met de beschikbare [!DNL API] code. Dit probleem wordt voorkomen door een algemeen account te maken dat niet aan een bepaalde werknemer is gekoppeld.

Als voorbeeld of gebruiksgeval voor dit type van rekening, laten wij zeggen uw klanten een hoop segmenten in één keer met willen veranderen [Bulkbeheertools](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). Om dit te doen, hebben zij nodig [!DNL API] toegang. In plaats van machtigingen toe te voegen aan een specifieke gebruiker, maakt u een niet-specifieke gebruiker. [!DNL API] gebruikersaccount met de juiste gegevens, sleutel en geheim om [!DNL API] oproepen. Dit is ook handig als de client eigen toepassingen ontwikkelt die gebruikmaken van de [!DNL Audience Manager] [!DNL API]s.
