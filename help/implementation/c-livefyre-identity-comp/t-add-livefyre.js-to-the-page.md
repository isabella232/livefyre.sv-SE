---
description: Livefyre.js är ett litet basbibliotek som tillhandahåller autentisering för appar på din webbplats.
seo-description: Livefyre.js är ett litet basbibliotek som tillhandahåller autentisering för appar på din webbplats.
seo-title: Lägg till Livefyre.js på sidan
title: Lägg till Livefyre.js på sidan
uuid: fe52446e-4911-4160-a68c-7413e9bc6222
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '87'
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

