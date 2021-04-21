---
description: Automatisera processen med API:erna för funktioner
title: Funktions-API:er
exl-id: 765e47fe-a406-44e6-b4fb-b2e85fc83c01
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Funktions-API:er{#feature-apis}

Automatisera processen med API:erna för funktioner

Använd funktions-API:erna för att automatisera den process som innehåll visas med. När du t.ex. skapar en Live-blogg eller Kommentarsapp kan du använda funktionen för att styra konversationen och skapa konsekvens i strömmen.

Livefyre erbjuder API:er för både Function och Unfeature.

## Funktion {#section_jpw_nqw_xz}

**Resurs**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

&#x200B; Ange användartoken för den valda moderatorn.

**Bokför data**

```
{value: <number>} 
```

Värdet används för att sortera aktuellt innehåll, som är det största till det minsta (10 visas före 1 i innehållslistan). Som standard är det här värdet **now** i epok, så aktuella kommentarer sorteras vanligen från nyaste till äldsta.

**Exempel på svar**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Datafältet används inte ännu.

## Avaktivera {#section_knh_mqw_xz}

**Resurs**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

Ange användartoken för den valda moderatorn.

**Exempel på svar**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>Datafältet används inte ännu.
