---
description: Sommige klanten willen hun Amazon Simple Storage Service (Amazon S3) geen toegang of geheime sleutels aan Adobe geven om het uploaden van doelgegevens naar hun emmers te autoriseren.
seo-description: Sommige klanten willen hun Amazon Simple Storage Service (Amazon S3) geen toegang of geheime sleutels aan Adobe geven om het uploaden van doelgegevens naar hun emmers te autoriseren.
seo-title: Over het autoriseren van toegang tot Amazon S3 Emmertje voor andere accounts voor batchbestemmingen
title: Over het autoriseren van toegang tot Amazon S3 Emmertje voor andere accounts voor batchbestemmingen
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Over het autoriseren van toegang tot Amazon S3 Emmertje voor andere accounts voor batchbestemmingen{#authorize-cross-account-bucket-batch}

Sommige klanten willen Adobe mogelijk geen [!DNL Amazon S3] toegang of geheime sleutels geven om het uploaden van doelgegevens naar hun emmers toe te staan.

Een alternatief dat wij onze klanten kunnen aanbieden is [!UICONTROL Cross-Account Bucket Permissions] in [!DNL Amazon S3]. Dit proces wordt beschreven in de documentatie [van](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)AWS. Voer de onderstaande stappen uit om dit alternatief in Audience Manager in te schakelen:

1. Ga naar **[!UICONTROL Servers]** en selecteer **[!UICONTROL Create Server]**.
1. Selecteer **[!UICONTROL S3]** in het **[!UICONTROL Protocol/Credentials]** vervolgkeuzemasker.
1. Schakel de **[!UICONTROL Use Internal Adobe Key]** optie in.
1. Gebruik de naam van het account en de emmernaam van uw klant in [!DNL Amazon S3].
1. Zorg ervoor dat de witte lijst van uw klant van de [!DNL Amazon S3] rekening `975822914085` op hun [!DNL S3] emmertje.

>[!NOTE]
>
>Onze Uitgaande uitgever zorgt ervoor dat het toestemmingsniveau op geüploade gegevens `bucket-owner-full-control` wordt geplaatst, zodat uw klant die gegevens kan bezitten.
