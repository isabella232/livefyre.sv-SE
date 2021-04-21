---
description: Livefyre.js är ett litet basbibliotek som tillhandahåller autentisering för appar på din webbplats.
title: Lägg till Livefyre.js på sidan
exl-id: 4c5dfb31-b7e5-48f7-826c-cddbee06d876
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# Lägg till Livefyre.js på sidan{#add-livefyre-js-to-the-page}

Livefyre.js är ett litet basbibliotek som tillhandahåller autentisering för appar på din webbplats.

Så här aktiverar du autentisering:

1. Lägg till Livefyre.js i `<head>`-elementet för webbsidan eller webbplatsmallen.
1. Lägg till något av följande på sidan:

   * `globalwindow.Livefyre` variabel
   * `Livefyre.require` för att läsa in andra Livefyre-paket på begäran

      ```
      <script src="//cdn.livefyre.com/Livefyre.js"></script>
      ```
