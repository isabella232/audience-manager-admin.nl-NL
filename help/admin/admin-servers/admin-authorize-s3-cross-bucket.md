---
description: Sommige klanten willen hun toegang tot Amazon Simple Storage Service (Amazon S3) of geheime sleutels aan Adobe mogelijk niet verlenen om het uploaden van bestemmingsgegevens naar hun emmers toe te staan.
seo-description: Sommige klanten willen hun toegang tot Amazon Simple Storage Service (Amazon S3) of geheime sleutels aan Adobe mogelijk niet verlenen om het uploaden van bestemmingsgegevens naar hun emmers toe te staan.
seo-title: Amazon S3 Bucket-toegang voor meerdere accounts autoriseren voor batchbestemmingen
title: Amazon S3 Bucket-toegang voor meerdere accounts autoriseren voor batchbestemmingen
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Amazon S3 Bucket-toegang voor meerdere accounts autoriseren voor batchdoelen{#authorize-cross-account-bucket-batch}

Sommige klanten willen hun [!DNL Amazon S3] toegang of geheime sleutels niet aan Adobe verstrekken om bestemminggegevens toe te laten uploaden aan hun emmers.

Een alternatief dat wij onze klanten kunnen aanbieden is [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Dit proces wordt beschreven in [AWS documentatie](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Volg onderstaande stappen om dit alternatief in Audience Manager in te schakelen:

1. Ga naar **[!UICONTROL Servers]** en selecteer **[!UICONTROL Create Server]**.
1. Selecteer **[!UICONTROL S3]** in het **[!UICONTROL Protocol/Credentials]** drop-down masker.
1. Schakel de optie **[!UICONTROL Use Internal Adobe Key]** in.
1. Gebruik de naam van uw account en emmer in [!DNL Amazon S3].
1. Zorg ervoor dat de witte lijst van uw klant [!DNL Amazon S3] rekening `975822914085` op hun [!DNL S3] emmertje een lijst maakt.

>[!NOTE]
>
>Onze Uitgaande uitgever zorgt ervoor dat het toestemmingsniveau `bucket-owner-full-control` op geüploade gegevens wordt geplaatst, zodat uw klant die gegevens kan bezitten.
