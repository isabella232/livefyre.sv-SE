---
description: Paketet Livefyre.js Auth ser till att alla sociala komponenter på sidan kan upptäcka en enda autentiseringsintegrering.
seo-description: Paketet Livefyre.js Auth ser till att alla sociala komponenter på sidan kan upptäcka en enda autentiseringsintegrering.
seo-title: Initiera Livefyre-identitet
title: Initiera Livefyre-identitet
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '112'
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
