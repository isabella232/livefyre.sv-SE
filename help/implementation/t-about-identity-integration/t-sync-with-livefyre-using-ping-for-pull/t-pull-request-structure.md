---
description: Bygg upp pull-begärandestrukturen för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
seo-description: Bygg upp pull-begärandestrukturen för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
seo-title: Pull Request Structure
solution: Experience Manager
title: Pull Request Structure
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Pull Request Structure{#pull-request-structure}

Bygg upp pull-begärandestrukturen för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.

Livefyre skickar en Pull-begäran till din URL.

Om t.ex. Pull-slutpunktens URL är:

```
https://example.yoursite.com/some_path/?id={id}
```

Livefyre Pull-begäran till denna slutpunkt kommer att vara:

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

där `lftoken` är en JSON Web Token som signerats med din nätverksnyckel, och **[!UICONTROL {userAuthToken}]** är den användarauth-token som genereras av Livefyre.

1. Använd `lftoken` för att validera att begäranden till din Ping for Pull URL skickades av Livefyre och inte av en skadlig agent.
1. För alla inkommande begäranden:

   * Kontrollera att frågesträngen `lftoken` finns på begäran.
   * Använd metoden `validateLivefyreToken` i Livefyre-biblioteken för att kontrollera att `lftoken` har signerats med din nätverksnyckel.

   * Om `lftoken` inte är närvarande, eller misslyckas med valideringen, ska du inte tillåta slutpunkten att svara med profilinformation. Svara istället med en 403-statuskod (förbjuden) och inget svarstext.

1. `userAuthToken` genereras av Livefyre- `buildUserAuthToken` metoden för användaren med användar-id &quot;system&quot;. Den här användaren är den första användaren som skapas för varje nytt nätverk.
