---
description: Lär dig hur du ändrar från en konversationsapp till en annan.
title: Apptyper för switchkärnor
exl-id: f18c97e8-8f39-4831-b907-afd438097e9e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Byt bastappyper{#switch-core-app-types}

Lär dig hur du ändrar från en konversationsapp till en annan.

Med Lifefyre kan du ändra samlingar från en typ av Livefyre Core-program till en annan (Comments, Live Blog eller Chat) genom att helt enkelt ändra vissa inställningar i dina `collectionMeta`-data.

Om du vill implementera en viss typ av app lägger du till ett nytt fält i `collectionMeta`-objektet. Kommentarer är standard så du behöver inte göra dessa uppdateringar om det är det program du vill använda. Om du vill byta till en annan app efter att en samling har skapats skickar du ett kontrollsummevärde under appinitieringen. Läs mer om hur du skapar ett kontrollsummevärde i vår `collectionMeta`-tokendokumentation.

## Live-blogg {#section_kvj_3jj_11b}

### PHP-exempel

```
use LivefyreLivefyre; 
  
$articleId = "1"; 
$articleTitle = "Title 1"; 
$articleURL = "https://dev.livefyre.com"; 
$articleTags = "tag1,tag2"; 
$lfType = "livecomments"; 
  
$network = Livefyre::getNetwork(networkName, networkKey); 
$site = network->getSite(siteId, siteKey); 
  
$collectionMeta = $site->buildCollectionMetaToken( 
   $articleTitle, 
   $articleURL, 
   $articleTags, 
   $lfType 
); 
  
$convConfig = array( 
   "el" => "targetElement", 
   "checksum" => $checksum, 
   "collectionMeta" => $collectionMeta, 
   "siteId" => <YOUR SITE ID>, 
   "articleId" => <ARTICLE ID> 
);
```

### Python-exempel

```
from livefyre import Livefyre 
  
article_id = "1" 
article_title = "Title 1" 
article_url = "https://dev.livefyre.com" 
article_tags = "tag1,tag2" 
lf_type = "livecomments" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token( 
   article_title, 
   article_url, 
   article_tags, 
   lf_type, 
) 
  
conv_config = dict( 
   "el" = "targetElement", 
   "checksum" = checksum, 
   "collectionMeta" = collection_meta_token, 
   "siteId" = <YOUR SITE ID>, 
   "articleId" = <ARTICLE ID> 
)
```

### Ruby-exempel

```
require 'livefyre'  
article_id = "1"  
title = "Title 1"  
link = "https://dev.livefyre.com"  
tag_str = "tag1,tag2"  
lf_type = "livecomments"  
  
network = Livefyre.get_network(networkName, networkKey)  
site = network.get_site(siteId, siteKey)  
  
collection_meta = site.build_collection_meta_token( 
   title, 
   link, 
   tag_str || "", 
   lf_type, 
)  
  
conv_config = { 
   :el => targetElement, 
   :checksum => checksum, 
   :collectionMeta => collection_meta_token, 
   :siteId => <YOUR SITE ID>, 
   :articleId => <ARTICLE ID> 
}
```

## Live-blogg {#section_bqt_cjj_11b}

### PHP-exempel

```
use LivefyreLivefyre; 
  
$articleId = "1"; 
$articleTitle = "Title 1"; 
$articleURL = "https://dev.livefyre.com"; 
$articleTags = "tag1,tag2"; 
$lfType = "liveblog"; 
  
$network = Livefyre::getNetwork(networkName, networkKey); 
$site = network->getSite(siteId, siteKey); 
  
$collectionMeta = $site->buildCollectionMetaToken( 
   $articleTitle, 
   $articleURL, 
   $articleTags, 
   $lfType 
); 
  
$convConfig = array( 
   "el" => "targetElement", 
   "checksum" => $checksum, 
   "collectionMeta" => $collectionMeta, 
   "siteId" => <YOUR SITE ID>, 
   "articleId" => <ARTICLE ID>  
);
```

### Python-exempel

```
from livefyre import Livefyre 
  
article_id = "1" 
article_title = "Title 1" 
article_url = "https://dev.livefyre.com" 
article_tags = "tag1,tag2" 
lf_type = "liveblog" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token( 
   article_title, 
   article_url, 
   article_tags, 
   lf_type, 
) 
  
conv_config = dict( 
   "el" = "targetElement", 
   "checksum" = checksum, 
   "collectionMeta" = collection_meta_token, 
   "siteId" = <YOUR SITE ID>, 
   "articleId" = <ARTICLE ID> 
)
```

### Ruby-exempel

```
require 'livefyre' 
  
article_id = "1" 
title = "Title 1" 
link = "https://dev.livefyre.com" 
tag_str = "tag1,tag2" 
lf_type = "liveblog" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token( 
   title, 
   link, 
   tag_str || "", 
   lf_type, 
) 
  
conv_config = { 
   :el => targetElement, 
   :checksum => checksum, 
   :collectionMeta => collection_meta_token, 
   :siteId => <YOUR SITE ID>, 
   :articleId => <ARTICLE ID> 
}
```

## Chatt {#section_dqm_w3j_11b}

### PHP

```
use LivefyreLivefyre; 
  
$articleId = "1"; 
$articleTitle = "Title 1"; 
$articleURL = "https://dev.livefyre.com"; 
$articleTags = "tag1,tag2"; 
$lfType = "livechat"; 
  
$network = Livefyre::getNetwork(networkName, networkKey); 
$site = network->getSite(siteId, siteKey); 
  
$collectionMeta = $site->buildCollectionMetaToken 
   $articleTitle, 
   $articleURL, 
   $articleTags, 
   $lfType 
); 
  
$convConfig = array( 
   "el" => "targetElement", 
   "checksum" => $checksum, 
   "collectionMeta" => $collectionMeta, 
   "siteId" => <YOUR SITE ID>, 
   "articleId" => <ARTICLE ID> 
);
```

### Python-exempel

```
from livefyre import Livefyre 
  
article_id = "1" 
article_title = "Title 1" 
article_url = "https://dev.livefyre.com" 
article_tags = "tag1,tag2" 
lf_type = "livechat" 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token(  
   article_title,  
   article_url,  
   article_tags,  
   lf_type,  
)

conv_config = dict( "el" = "targetElement", 
   "checksum" = checksum, 
   "collectionMeta" = collection_meta_token, 
   "siteId" = <YOUR SITE ID>, 
   "articleId" = <ARTICLE ID> 
)
```

### Ruby-exempel

```
require 'livefyre' 
  
article_id = "1" 
title = "Title 1" 
link = "https://dev.livefyre.com" 
tag_str = 'tag1,tag2' 
lf_type = 'livechat' 
  
network = Livefyre.get_network(networkName, networkKey) 
site = network.get_site(siteId, siteKey) 
  
collection_meta = site.build_collection_meta_token(  
   title,  
   link, 
   tag_str || "", 
   lf_type, 
) 
  
conv_config = { 
   :el => targetElement, 
   :checksum => checksum, 
   :collectionMeta => collection_meta_token, 
   :siteId => <YOUR SITE ID>, 
   :articleId => <ARTICLE ID> 
}
```
