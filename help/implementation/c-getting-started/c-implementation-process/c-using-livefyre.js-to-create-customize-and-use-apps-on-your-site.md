---
seo-title: Bädda in en app
solution: Experience Manager
title: Bädda in en app
uuid: e75caf0e-04ea-4b04-89ed-fea1183ecf63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Bädda in en app{#embed-an-app}

Lägg till Livefyre-appar på dina webbsidor med hjälp av kodstrukturen Livefyre.js.

Denna dokumentation är avsedd för en teknisk målgrupp. För [icke-teknisk information om appar](/help/using/c-about-apps/c-about-apps.md).

I det här avsnittet beskrivs den kodstruktur som du måste inkludera i sidmallen för att bädda in Livefyre-appar på webbplatsen.

1. Skapa en HTML-fil med en Livefyre-platshållare.

   Skapa en ny HTML-fil i valfri textredigerare. Skapa en platshållare för Livefyre `<div>`-elementet där appen ska bäddas in.

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. Inkludera biblioteket Livefyre.js.

   Inkludera sedan Livefyre JS Library. Placera följande referens i ett `<script>`-element i `<head>`-elementet. Öppna sedan sidan i en webbläsare och använd webbläsarens webbläsare för att bekräfta att Livefyre har lästs in.

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. Bygg Livefyre-appen.

   Använd `Livefyre.require` för att konstruera både Core- och SDK-appar genom att skicka in Livefyre-paket som du tänker använda.

   1. Bygg en huvudapp.

      Använd följande struktur för att skapa en huvudapp (kommentarer, Live-blogg eller chatt):

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. Bygg en SDK-app.

      Använd följande struktur om du vill skapa en SDK-app som medievägg eller feed:

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      Se [mer information om specifika appar](/help/using/c-about-apps/c-about-apps.md). Vi rekommenderar att du fäster vid den senaste större versionen av paketet (som finns via [Livefyre.require](https://cdn.livefyre.com/packages.html)) för att undvika oväntade brutna integreringar.

Nästa: Lägg till autentisering på webbplatsen så att användarna kan lägga in kommentarer.
