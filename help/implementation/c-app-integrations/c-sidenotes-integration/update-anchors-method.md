---
description: Huvudbiblioteket Livefyre använde för att driva Livefyre på er webbplats.
title: Livefyre.js
uuid: null
exl-id: 5f60ce54-5669-4768-912d-c1b13946d8b8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '96'
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
