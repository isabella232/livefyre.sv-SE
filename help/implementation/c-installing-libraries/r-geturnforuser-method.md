---
description: Den här metoden returnerar URN för det här nätverkets användare.
seo-description: Den här metoden returnerar URN för det här nätverkets användare.
seo-title: getUrnForUser-nätverksmetod
solution: Experience Manager
title: getUrnForUser-nätverksmetod
uuid: b70b8b0f-2b3a-4a1d-90d0-93a97a137ad4
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getUrnForUser-nätverksmetod{#geturnforuser-network-method}

Den här metoden returnerar URN för det här nätverkets användare.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| userId | Sträng | Det userId som ska användas i URN. |

## Java-exempel {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Python-exempel {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ruby-exempel {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
