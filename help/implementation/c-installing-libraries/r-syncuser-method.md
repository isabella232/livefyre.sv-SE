---
description: Instruerar Livefyre att hämta användarinformation från en tidigare angiven URL för användarsynkronisering. Returnerar ett booleskt värde.
title: syncUser-nätverksmetod
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
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
