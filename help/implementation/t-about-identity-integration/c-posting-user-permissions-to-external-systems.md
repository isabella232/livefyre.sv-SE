---
description: Livefyre använder ett PUSH-gränssnitt för att skicka en extern systeminformation om ändringar i användarbehörigheter.
seo-description: Livefyre använder ett PUSH-gränssnitt för att skicka en extern systeminformation om ändringar i användarbehörigheter.
seo-title: Publicera användarbehörigheter till externa system (valfritt)
solution: Experience Manager
title: Publicera användarbehörigheter till externa system (valfritt)
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Publicera användarbehörigheter till externa system (valfritt){#posting-user-permissions-to-external-systems-optional}

Livefyre använder ett PUSH-gränssnitt för att skicka en extern systeminformation om ändringar i användarbehörigheter.

## Typer av användare i Livefyre Studio

| Användartyp | Beskrivning |
|--- |--- |
| ägare | Den här användaren är ägare och kan både moderera innehåll och tilldela nya moderatorer. |
| admin | Den här användaren är moderator och kan moderera innehåll. |
| medlem | Den här användaren är vitlistad. Publicerat innehåll passerar inte genom skräppost eller svordomsfilter och kräver inget godkännande i förmodererade strömmar. |
| ingen | Den här användaren är en standardanvändare och har inga särskilda behörigheter. |
| outcast | Den här användaren har förbjudits att delta i konversationer. |

Om du vill publicera användarbehörigheter till externa system måste du registrera en URL som tar emot behörighetsdata som POST-begäranden.

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
| jid | JID för den användare vars anknytning ändras. Ett JID är en sträng i formuläret `user_id@network`. |
| anknytning | Namnet på de tilldelade behörigheterna, som måste vara något av följande:  `{admin | member | none | outcast | owner}` |

Mer information om hur du uppdaterar inställningarna för användaranknytning finns i API-referens för [Lägg till användaranknytning](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post).
