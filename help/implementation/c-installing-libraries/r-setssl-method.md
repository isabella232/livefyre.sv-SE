---
description: Anger SSL för att API-anrop ska vara aktiverade eller inaktiverade.
title: setSSL-nätverksmetod
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# setSSL-nätverksmetod{#setssl-network-method}

Anger SSL för att API-anrop ska vara aktiverade eller inaktiverade.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| ssl | Boolean | Standardvärdet är true. om du vill ha SSL aktiverat, annars false. <br><ul><li>Sant - SSL på </li><li>Falskt - SSL av</li></ul> |

## Java-exempel {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python-exempel {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby-exempel {#section_enh_gds_rz}

```
network.ssl = false 
```
