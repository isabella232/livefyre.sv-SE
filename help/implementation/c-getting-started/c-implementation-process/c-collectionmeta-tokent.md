---
description: Skapa en unik token på servern som identifierar alla samlingar du skapar.
seo-description: Skapa en unik token på servern som identifierar alla samlingar du skapar.
seo-title: CollectionMeta-token
solution: Experience Manager
title: CollectionMeta-token
uuid: d5db0b0f-2807-4392-874a-94ac3c1e7550
translation-type: tm+mt
source-git-commit: 6978f0f36b5698c9c599c1828edea67703423397
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---


# CollectionMeta-token{#collectionmeta-token}

Skapa en unik token på servern som identifierar alla samlingar du skapar.

Livefyre tilldelar varje samling du skapar en unik identifierare. Livefyre tilldelar en titel, URL och andra parametrar, bland annat:

## collectionMeta-tokenparametrar

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| networkName | Sträng (valfritt) | Namnet på Livefyre-nätverket (tillgängligt från [!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials] ). Detta är valfritt när du använder biblioteket för att skapa en collectionMeta-token. |
| networkKey | Sträng (valfritt) | Den hemliga nyckeln för det specifika nätverket (finns i Studio > Settings > Integration Settings > Credentials). Detta är valfritt när du använder biblioteket för att skapa en collectionMeta-token. |
| siteId | Sträng (valfritt) | ID för platsen (tillgängligt från [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). Valfritt när du använder biblioteket för att skapa en collectionMeta-token. |
| siteKey | Sträng (valfritt) | Den hemliga nyckeln för webbplatsen (finns i [!UICONTROL Studio > Settings > Integration Settings > Credentials] ). |
| articleId | Sträng (valfritt) | Ett unikt ID för samlingen. |
| title | Sträng (valfritt) | Titeln som du vill använda för samlingen. Vanligtvis motsvarar detta titeln på sidan som visar appen. <br>Till exempel: &quot;Integrationen är så mycket rolig!&quot; <br>Obs!  Titeln får innehålla högst 255 tecken. Titelfältet stöder inte HTML-entiteter. Koda specialtecken med UTF-8. |
| url | Sträng (valfritt) | Den absoluta kanoniska URL som du vill bifoga till den här samlingen. Den här URL:en används för att generera länkar tillbaka till appen från innehåll som delas på Facebook och Twitter, e-postmeddelanden och Livefyre Studio. <br>Obs!  Om du testar lokalt använder du en giltig bas-URL-domän (till exempel: giltig: `https://customer.com`; ogiltig: `https://localhost:5995`). |
| taggar | Sträng (valfritt) | En kommaavgränsad lista med enstaka nyckelord eller fraser. Sök i samlingar efter taggar med Studio.  </br>Obs!  Taggar får inte innehålla blanksteg. Använd understreck om du vill att ett mellanslag ska visas i användargränssnittet. |
| tillägg | JSON (valfritt) | En JSON-formaterad uppsättning parametrar som ska skickas till samlingen. |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## NodeJS {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE]
>
>Livefyre tar emot den collectionMeta-token som du skapar och fastställer unika egenskaper genom att kombinera siteId (Livefyre tillhandahålls) och articleId (kunden anges).
