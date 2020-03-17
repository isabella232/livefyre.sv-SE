---
description: Den här metoden returnerar URN för den här samlingen. Du måste köra createOrUpdate() innan du kör den här metoden.
seo-description: Den här metoden returnerar URN för den här samlingen. Du måste köra createOrUpdate() innan du kör den här metoden.
seo-title: getUrn-samlingsmetod
solution: Experience Manager
title: getUrn-samlingsmetod
uuid: 2f4d7796-2ae5-4b74-a958-40825c6bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

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

