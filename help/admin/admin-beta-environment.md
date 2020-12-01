---
description: De bètaomgeving is bedoeld voor het testen van implementaties van Audience Managers. Wijzigingen in bèta hebben geen invloed op de productiegegevens. De bètaomgeving van de Audience Manager is een kleinschalige, zelfstandige versie van de productieomgeving. Alle gegevens die u wilt testen, moeten in deze omgeving worden ingevoerd en verzameld.
seo-description: De bètaomgeving is bedoeld voor het testen van implementaties van Audience Managers. Wijzigingen in bèta hebben geen invloed op de productiegegevens. De bètaomgeving van de Audience Manager is een kleinschalige, zelfstandige versie van de productieomgeving. Alle gegevens die u wilt testen, moeten in deze omgeving worden ingevoerd en verzameld.
seo-title: Bètaomgeving
solution: Audience Manager
title: Bètaomgeving
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---


# Bètaomgeving {#beta-environment}

De bètaomgeving is bedoeld voor het testen van implementaties van Audience Managers. Wijzigingen in bèta hebben geen invloed op de productiegegevens. De bètaomgeving van de Audience Manager is een kleinschalige, zelfstandige versie van de productieomgeving. Alle gegevens die u wilt testen, moeten in deze omgeving worden ingevoerd en verzameld.

## Overzicht {#overview}

<!-- beta_environment_admin.xml -->

| Service | URL/hostnaam | Stappen voor levering |
|--- |--- |--- |
| S3 |  | Zie [Voorziening Amazon S3 Buckets](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https&amp;colon;//dcs-beta.demdex.net/... | Geen extra stappen nodig van onze kant. Zie [Toegang tot DCS in het milieu van Beta](admin-beta-environment.md#access-dcs-beta-environment). |
| UI | https&amp;colon;//bank-beta.demdex.com | Gegevens worden maandelijks van de productie naar de bètaomgeving gekopieerd. Referenties voor productie zijn geldig voor bèta. |
| API | https&amp;colon;//api-beta.demdex.com/... | Gegevens worden maandelijks van de productie naar de bètaomgeving gekopieerd. Referenties voor productie zijn geldig voor bèta. |

## Voorziening Amazon S3-emmertjes {#provision-s3-buckets}

>[!NOTE]
>
>We gaan weg van het gebruik van [!DNL FTP/SFTP]. Ook, gelieve te merken op dat de uitgaande gegevensoverdrachten niet voor het bètamilieu werken.

Aan voorziening [!DNL S3] emmers voor binnenkomende gegevens:

1. Gebruik [**SKMS Verzoek TechOps Help**](https://skms.adobe.com/) eigenschap.
1. Ga naar **[!UICONTROL Request TechOps Help]** in de linkernavigatieregel.
1. Typ in **[!UICONTROL Request Search]** in Audience Manager in het zoekveld.
1. Blader omlaag in de zoekresultaten en klik op **Audience Manager - S3 Binnenkomend / Uitgaande Account Provisioning**.
1. Vul de velden in het inrichtingsvenster in en geef **Sandbox-omgeving** op in het veld **[!UICONTROL Environment]**.

>[!NOTE]
>
>We ontmoedigen het gebruik van [!DNL FTP/SFTP] en moedigen het gebruik van [!UICONTROL Amazon S3] aan. De redenen waarom wij het gebruik van [!UICONTROL Amazon S3] aanmoedigen zijn vermeld in [Amazon S3:About](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html).

## Open DCS in het milieu van Beta {#access-dcs-beta-environment}

Om tot [!UICONTROL DCS] in het bètamilieu toegang te hebben:

1. Maak een [!UICONTROL DCS] vraag, gebruikend [!DNL curl] [bevel](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] is een hulpmiddel om gegevens van of naar een server over te brengen, gebruikend één van vele gesteunde protocollen.

   Bijvoorbeeld: `curl -v https://dcs-beta.demdex.net/event`

1. Verifieer dat uw verzoek door de bèta [!UICONTROL DCS] door &quot;[!DNL sandbox]&quot;in [!UICONTROL DCS] reactiekop te zoeken werd gediend.

   Bijvoorbeeld:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->