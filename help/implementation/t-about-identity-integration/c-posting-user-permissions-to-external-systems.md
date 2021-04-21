---
description: Livefyre använder ett PUSH-gränssnitt för att skicka en extern systeminformation om ändringar i användarbehörigheter.
title: Publicera användarbehörigheter till externa system (valfritt)
exl-id: 335c9ff2-e392-4310-aad2-7890c8e82eba
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---

# Publicera användarbehörigheter till externa system (valfritt){#posting-user-permissions-to-external-systems-optional}

Livefyre använder ett PUSH-gränssnitt för att skicka en extern systeminformation om ändringar i användarbehörigheter.

## Typer av användare i Livefyre Studio

| Användartyp | Beskrivning |
|--- |--- |
| ägare | Den här användaren är ägare och kan både moderera innehåll och tilldela nya moderatorer. |
| admin | Den här användaren är moderator och kan moderera innehåll. |
| medlem | Den här användaren är en lista över tillåtna användare. Publicerat innehåll passerar inte genom skräppost eller svordomsfilter och kräver inte godkännande i förmodererade strömmar. |
| ingen | Den här användaren är en standardanvändare och har inga särskilda behörigheter. |
| outcast | Den här användaren har förbjudits att delta i konversationer. |

Om du vill publicera användarbehörigheter till externa system måste du registrera en URL som tar emot behörighetsdata som POSTEN begär.

Exempel:

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| Parameter | Beskrivning |
|--- |--- |
| networkName | Ditt Livefyre-nätverksnamn angavs. |
| token | Giltig systemtoken. |
| url | URL att registrera. |

Den registrerade URL:en ska acceptera POST:er med följande data som innehållstyp: application/x-www-form-urlencoded.

| Parameter | Beskrivning |
|--- |--- |
| jid | JID för den användare vars anknytning ändras. Ett JID är en sträng i formatet `user_id@network`. |
| anknytning | Namnet på de tilldelade behörigheterna, som måste vara något av följande:  `{admin | member | none | outcast | owner}` |

Mer information om hur du uppdaterar användartillhörighetsinställningar finns i [API-referens för Lägg till användaranknytning](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
