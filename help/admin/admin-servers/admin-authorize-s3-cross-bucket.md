---
description: Sommige klanten willen hun toegang tot Amazon Simple Storage Service (Amazon S3) of geheime sleutels aan Adobe mogelijk niet verlenen om het uploaden van bestemmingsgegevens naar hun emmers toe te staan.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: Amazon S3 Bucket-toegang voor meerdere accounts autoriseren voor batchbestemmingen
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Amazon S3 Bucket-toegang voor meerdere accounts autoriseren voor batchbestemmingen{#authorize-cross-account-bucket-batch}

Sommige klanten willen hun [!DNL Amazon S3] toegang tot of geheime sleutels tot Adobe om bestemmings gegevens toe te staan uploaden aan hun emmers.

Een alternatief dat wij onze klanten kunnen aanbieden is [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Dit proces wordt beschreven in het dialoogvenster [AWS-documentatie](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Volg onderstaande stappen om dit alternatief in Audience Manager in te schakelen:

1. Ga naar **[!UICONTROL Servers]** en selecteert u **[!UICONTROL Create Server]**.
1. Selecteren **[!UICONTROL S3]** in de **[!UICONTROL Protocol/Credentials]** vervolgkeuzemasker.
1. Controleer de **[!UICONTROL Use Internal Adobe Key]** optie.
1. Gebruik de naam van uw account en emmer in [!DNL Amazon S3].
1. Zorg ervoor dat de witte lijst van uw klant de [!DNL Amazon S3] account `975822914085` op hun [!DNL S3] emmertje.

>[!NOTE]
>
>Onze Uitgaande uitgever zorgt ervoor dat het toestemmingsniveau `bucket-owner-full-control` wordt ingesteld op geüploade gegevens, zodat uw klant eigenaar kan zijn van die gegevens.
