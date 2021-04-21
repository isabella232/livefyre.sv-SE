---
description: Skapa ett nätverksobjekt.
title: Nätverksklassmetoder
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 3%

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
