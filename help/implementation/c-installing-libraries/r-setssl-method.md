---
description: Anger SSL för att API-anrop ska vara aktiverade eller inaktiverade.
seo-description: Anger SSL för att API-anrop ska vara aktiverade eller inaktiverade.
seo-title: setSSL-nätverksmetod
solution: Experience Manager
title: setSSL-nätverksmetod
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '70'
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
