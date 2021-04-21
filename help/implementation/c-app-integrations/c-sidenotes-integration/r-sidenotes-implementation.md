---
description: Implementera sidobjekt med .js-implementering.
title: Sidenotes Implementation
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 20%

---

# Sidenotes Implementation{#sidenotes-implementation}

## Implementera sidobjekt med .js-implementering

Om du vill implementera den här funktionen skickar du en 1-1-objektmappning av strängarna som du vill åsidosätta till Javascript-konfigurationsobjektet. Om du inte anger något fält används standardtexten.

### Exempel

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
