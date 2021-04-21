---
description: Den här metoden returnerar URN för det här nätverkets användare.
title: getUrnForUser-nätverksmetod
exl-id: 272e724e-d09d-4d7d-9967-a229707ff47f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

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
