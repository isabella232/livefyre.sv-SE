---
description: Implementera sidobjekt med .js-implementering.
seo-description: Implementera sidobjekt med .js-implementering.
seo-title: Sidenotes Implementation
solution: Experience Manager
title: Sidenotes Implementation
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 26%

---


# Sidenotes Implementation{#sidenotes-implementation}

## Implementera sidobjekt med .js-implementering

Om du vill implementera den här funktionen skickar du en 1-1-objektmappning av strängarna som du vill åsidosätta till Javascript-konfigurationsobjektet. Om du inte anger något fält används standardtexten.

### Exempel

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
