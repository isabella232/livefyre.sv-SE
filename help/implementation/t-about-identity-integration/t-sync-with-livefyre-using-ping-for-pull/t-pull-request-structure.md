---
description: Bygg upp pull-begärandestrukturen för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
seo-description: Bygg upp pull-begärandestrukturen för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
seo-title: Pull Request Structure
solution: Experience Manager
title: Pull Request Structure
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

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

där `lftoken` är en JSON Web Token som har signerats med din nätverksnyckel, och **[!UICONTROL {userAuthToken}]** är den användarautentiseringstoken som genereras av Livefyre.

1. Validera `lftoken` att begäranden till din Ping for Pull URL skickades av Livefyre och inte av en skadlig agent.
1. För alla inkommande begäranden:

   * Se till att frågesträngen finns på begäran `lftoken` .
   * Använd `validateLivefyreToken` metoden i Livefyre-biblioteken för att kontrollera att den `lftoken` signerades med din nätverksnyckel.

   * Om `lftoken` inte finns, eller inte godkänns, ska du inte tillåta slutpunkten att svara med profilinformation. Svara istället med en 403-statuskod (förbjuden) och inget svarstext.

1. `userAuthToken` genereras av Livefyre- `buildUserAuthToken` metoden för användaren med användar-id &quot;system&quot;. Den här användaren är den första användaren som skapas för varje nytt nätverk.
