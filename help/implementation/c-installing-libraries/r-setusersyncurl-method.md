---
description: Informerar Livefyre att uppdatera nätverkets URL för användarsynkronisering till den angivna. Returnerar ett booleskt värde.
seo-description: Informerar Livefyre att uppdatera nätverkets URL för användarsynkronisering till den angivna. Returnerar ett booleskt värde.
seo-title: setUserSyncUrl-nätverksmetod
solution: Experience Manager
title: setUserSyncUrl-nätverksmetod
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncUrl-nätverksmetod{#setusersyncurl-network-method}

Informerar Livefyre att uppdatera nätverkets URL för användarsynkronisering till den angivna. Returnerar ett booleskt värde.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| urlTemplate | Sträng | Den URL som ska registreras hos Livefyre för synkronisering av användar-ID:n. Kräver &quot;`{id}`&quot; som en del av den angivna URL-strängen. |

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
