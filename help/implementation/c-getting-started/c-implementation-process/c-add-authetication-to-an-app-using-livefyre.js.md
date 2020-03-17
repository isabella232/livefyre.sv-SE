---
description: Använd Livefyre.js för att lägga till sidövergripande autentisering för dina Livefyre-appar.
seo-description: Använd Livefyre.js för att lägga till sidövergripande autentisering för dina Livefyre-appar.
seo-title: Lägg till autentisering i ett program med Livefyre.js
solution: Experience Manager
title: Lägg till autentisering i ett program med Livefyre.js
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# Lägg till autentisering i en app med Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}

Använd Livefyre.js för att lägga till sidövergripande autentisering för dina Livefyre-appar.

`Livefyre.js Aut`Han är ett JavaScript-paket som utvecklats av Livefyre och som gör att alla appar på webbplatsen kan dela en enda autentiseringsintegrering. Med Auth kan du definiera hur användarna ska registrera, logga in och logga ut genom att delegera dessa flöden till ett AuthDelegate-objekt som du definierar.

## Steg 1: Aktivera autentisering för en sida {#section_pgp_jtt_bbb}

Använd `Livefyre.js` för att aktivera autentisering för en sida så att användare kan logga in och interagera med appar med ditt befintliga autentiseringssystem.

1. Om du vill aktivera autentisering på en sida lägger du `Livefyre.js` till *&lt;head>* -elementet för webbsidan eller webbplatsmallen.

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. Används `Livefyre.require` för att aktivera autentisering. Att använda `Livefyre.require` påminner om att anropa andra paket genom att använda require. Integrationskoden som kräver autentisering ser ut så här:

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## Steg 2: Registrera en AuthDelegate {#section_oqm_15t_bbb}

Om du vill aktivera autentisering skapar du en `AuthDelegate` och skickar den till `Livefyre.js` Autentisering.

Ett objekt `AuthDelegate` är ett objekt som du definierar och som avgör hur användare ska logga in, logga ut och visa profiler.

1. Skapa en `AuthDelegate`. Hur du konstruerar en `AuthDelegate` beror på din identitetsleverantör. Mer information finns i Identitetsintegrering.

1. Skicka `AuthDelegate` till `Livefyre.js` autentisering. Det enklaste `AuthDelegate` loggar in samma användare när en användare utlöste den delegerade inloggningsmetoden från ett program:

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## Steg 3: Synkronisera användardata {#section_u4m_j5t_bbb}

Synkronisera informationen om användarprofilen mellan Livefyre och din identitetsleverantör.

Du måste synkronisera din användarprofilinformation mellan Livefyre och din identitetsleverantör. Mer information finns i [Janrain Capture Integration](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md).
