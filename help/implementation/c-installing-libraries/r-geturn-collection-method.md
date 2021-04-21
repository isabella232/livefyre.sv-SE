---
description: Den här metoden returnerar URN för den här samlingen. Du måste köra createOrUpdate() innan du kör den här metoden.
title: getUrn-samlingsmetod
exl-id: bea04805-8f02-4c06-9a1a-6b057de831ab
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# getUrn-samlingsmetod{#geturn-collection-method}

Den här metoden returnerar URN för den här samlingen. Du måste köra createOrUpdate() innan du kör den här metoden.

## Java-exempel {#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
collection.getUrn(); 
```

Exempelutdata:

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection.urn() 
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection.urn
```

Exempelutdata:

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```
