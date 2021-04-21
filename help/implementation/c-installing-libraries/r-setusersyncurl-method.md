---
description: Informerar Livefyre att uppdatera nätverkets URL för användarsynkronisering till den angivna. Returnerar ett booleskt värde.
title: setUserSyncUrl-nätverksmetod
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# setUserSyncUrl-nätverksmetod{#setusersyncurl-network-method}

Informerar Livefyre att uppdatera nätverkets URL för användarsynkronisering till den angivna. Returnerar ett booleskt värde.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| urlTemplate | Sträng | Den URL som ska registreras hos Livefyre för synkronisering av användar-ID:n. Kräver att `{id}` är en del av den angivna URL-strängen. |

## Java-exempel {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exempelutdata:

```
true
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

Exempelutdata:

```
true
```

## PHP-exempel {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

Exempelutdata:

```
true
```

## Python-exempel {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exempelutdata:

```
True
```

## Ruby-exempel {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

Exempelutdata:

```
True
```
