---
description: Skapa ett nätverksobjekt.
seo-description: Skapa ett nätverksobjekt.
seo-title: Nätverksklassmetoder
solution: Experience Manager
title: Nätverksklassmetoder
uuid: 4130beda-dd09-49ae-aafb-f6b956e30b51
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 2%

---


# Nätverksklassmetoder{#network-class-methods}

Skapa ett nätverksobjekt.

När du har skapat ett nätverksobjekt förutsätter resten av sidan att du har ett instansierat Network-objekt i sessionen.

## Nätverksobjekt

| Parameter | Typ | Beskrivning |
|---|---|---|
| *`network`* | Sträng | Ditt Livefyre-nätverk. Exempel: “`labs.fyre.co`”. |
| *`networkKey`* | Sträng | Den hemliga nyckeln för nätverket tillhandahålls av Livefyre. |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
