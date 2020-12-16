---
description: Installera autentiseringspaketet för att aktivera användarautentisering så att användarna kan interagera med dina appar.
seo-description: Installera autentiseringspaketet för att aktivera användarautentisering så att användarna kan interagera med dina appar.
seo-title: Autentiseringspaket
solution: Experience Manager
title: Autentiseringspaket
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# Autentiseringspaket{#authentication-package}

Installera autentiseringspaketet för att aktivera användarautentisering så att användarna kan interagera med dina appar.

Livefyre-appar använder det globala autentiseringspaketet för att associera användare med appåtgärder. Autentiseringspaketet är tillgängligt via `Livefyre.require`.

Om du vill aktivera autentisering på sidan lägger du först till `Livefyre.js` i `<head>`-elementet för webbsidan eller webbplatsmallen.

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

Användning av Livefyre.require för att aktivera autentisering liknar användning av require to call other packages. Integrationskoden som kräver autentisering ser ut så här:

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## Metoder {#section_ojx_1lz_fz}

När autentiseringsmodulen har inkluderats enligt ovan med `Livefyre.require`, visas följande metoder som du kan anropa för att meddela andra appar på sidan om autentiseringsrelaterade händelser.

| Metod | Beskrivning |
|--- |--- |
| `.login(callback)` | Utlös inloggningsflödet som implementerats av det registrerade AuthDelegate-objektet. Vanligtvis är det bara appar med autofunktioner som kan anropa detta, inte själva värdsidan. |
| `.logout(callback)` | Meddela autentiseringen att slutanvändaren har loggat ut på något externt sätt och att alla förlitande appar ska rensa autentiseringsstatusen fram till nästa inloggning. Detta rensar den interna sessionen som underhålls av Auth. |
| `.authenticate(credentials)` | Meddela Auth att en användare har autentiserats på något externt sätt och att en Livefyre Authentication Token har erhållits för slutanvändaren. Använd det här alternativet om du anger en cookie med Livefyre-token, eller om du har en token för användaren och vill logga in användaren explicit. Exempel: <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | Delegera implementeringsinformationen för autentisering (till exempel ditt anpassade autentiseringsflöde) till ett objekt som du definierar. Detta måste anropas av värdsidan för att aktivera interaktiva funktioner i Livefyre-appar. |

