---
description: Paketet Livefyre.js Auth ser till att alla sociala komponenter på sidan kan upptäcka en enda autentiseringsintegrering.
title: Initiera Livefyre-identitet
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Initiera Livefyre-identitet{#initialize-livefyre-identity}

Paketet Livefyre.js Auth ser till att alla sociala komponenter på sidan kan upptäcka en enda autentiseringsintegrering.

Livefyre tillhandahåller ett `lfep-auth-delegate`-paket som gör ett lämpligt autentiseringsdelegat åt dig. Auth måste anges som ett AuthDelegate-objekt som kan utföra autentiseringsåtgärder, som inloggning och utloggning.

1. Lägg till Livefyre.js på din webbsida.
1. Om du vill att Auth ska delegera dessa åtgärder till Livefyre Identity lägger du till följande:

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
