---
description: Instruerar Livefyre att hämta användarinformation från en tidigare angiven URL för användarsynkronisering. Returnerar ett booleskt värde.
seo-description: Instruerar Livefyre att hämta användarinformation från en tidigare angiven URL för användarsynkronisering. Returnerar ett booleskt värde.
seo-title: syncUser-nätverksmetod
solution: Experience Manager
title: syncUser-nätverksmetod
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# syncUser Network Method{#syncuser-network-method}

Instruerar Livefyre att hämta användarinformation från en tidigare angiven URL för användarsynkronisering. Returnerar ett booleskt värde.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| userId | Sträng | Användar-ID:t som ska synkroniseras med Livefyre. Du måste ange en URL för användarsynkronisering med Livefyre innan du anropar den här metoden. |

## Java-exempel {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

Exempelutdata:

```
true
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

Exempelutdata:

```
true
```

## PHP-exempel {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

Exempelutdata:

```
true
```

## Python-exempel {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

Exempelutdata:

```
True
```

## Ruby-exempel {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

Exempelutdata:

```
True
```
