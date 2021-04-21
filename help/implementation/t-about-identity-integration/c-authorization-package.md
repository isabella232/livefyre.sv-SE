---
description: Installera autentiseringspaketet för att aktivera användarautentisering så att användarna kan interagera med dina appar.
title: Autentiseringspaket
exl-id: 639032ee-ed7d-4cb0-83ba-f11d3dc607b6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '263'
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
