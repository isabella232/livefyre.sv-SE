---
description: Huvudbiblioteket Livefyre använde för att driva Livefyre på er webbplats.
seo-description: Huvudbiblioteket Livefyre använde för att driva Livefyre på er webbplats.
seo-title: updateAnchors-metod
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# updateAnchors-metod {#updateAnchorsMethod}

Använd metoden updateAnchors om du vill lägga till innehåll som är placerat på sidan dynamiskt.

Den här metoden är användbar för sidnumrering, eller i andra fall där platshållarinnehåll läggs till dynamiskt på sidan. Den här metoden definierar nya ankare för de matchade elementen och tar ett argument: newSelectors.

**newSelectors**. Väljarna som ska läggas till i sidobjekt. Detta kan vara en väljarsträng, ett jQuery-objekt eller en array med element (någon av de typer som accepteras av väljarargumentet som skickas under appkonstruktionen).
Format:

```
app.updateAnchors(newSelectors);
```

Exempel:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
