---
description: Lär dig övervaka och lagra användargenererat innehåll som flödar genom Livefyre-systemet.
seo-description: Lär dig övervaka och lagra användargenererat innehåll som flödar genom Livefyre-systemet.
seo-title: Aktivitetsström
solution: Experience Manager
title: Aktivitetsström
uuid: f40deec1-58ab-41c9-aac4-d2d8c9192bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Aktivitetsström {#activity-stream}

Lär dig övervaka och lagra användargenererat innehåll som flödar genom Livefyre-systemet.

Använd API:t för aktivitetsström för att förbruka användargenererade data som flödar genom Livefyre-systemet i ditt nätverk eller på din webbplats. Till exempel: använda data från detta API för att uppdatera dina sökindex baserat på klassificering, eller för att hantera användarnas emblem i ett tredjepartssystem baserat på deras aktivitet.

API för aktivitetsström:

En fullständig lista över tillgängliga slutpunkter finns i avsnittet för LiveFyre API-referens.

## Resurser {#section_aql_n4l_b1b}

Det finns två slutpunkter, en för staging-miljön och en för produktion.

### Mellanlagring

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Produktion

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### Parametrar

* **resurs:** *sträng* A URN för objektet som du begär aktivitetsdata för.

* **sedan:** *heltal* Ett 64-bitars heltal som representerar ID:t för den senaste händelsen som du fick. Ange&quot;0&quot; om du inte har några tidigare data.

## URN-strängar {#section_skl_q4l_b1b}

Exempel:

* **urn:livefyre:** `example.fyre.co` Aktivitetsströmmen för `example.fyre.co`.
* **urn:livefyre:** `example.fyre.co:site=54321` Aktivitetsströmmen för plats 54321 under `example.fyre.co` nätverket.

## Tokenprinciper {#section_nwh_c5j_11b}

API:t för aktivitetsström använder en OAuth Bearer-token för autentisering. Bearer Tokens ingår i specifikationen OAuth 2.0 och beskrivs officiellt [här](https://tools.ietf.org/html/rfc6750#section-1.2).

En token innehåller flera saker:

* Vem skapade token.
* Vem fick en token.
* En tidpunkt då det inte längre är giltigt.
* Det vi jobbar på.
* En lista över behörigheter som har beviljats.

### Steg

Stegen för att skapa en OAuth Bearer-token är bland annat:

* Skapa en karta/ordlista som innehåller utfärdare, målgrupp, ämne, utgångsdatum och omfattning.
* Använd JWT-biblioteket, med din hemlighet, för att koda en JWT-token.
* Lägg till &quot;Autentisering: Bearer&quot; till din HTTP-begäran.

I kodexemplet nedan visas ovanstående steg i Python:

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

Där innehavartokennycklarna definieras enligt följande:

* **is** *(Issuer)* En entitet med behörigheten att generera tokens. Det kan vara Livefyre, en webbplats eller ett nätverk. (För att komma för sent till skolan är det din förälder.)
* **aud** *(Audience)* Personen som denna token genererades för. Om du själv skapar en token är det platsen eller nätverket.
* **sub** *(Subject)* Det ämne för vilket tillstånd ska beviljas. Om du till exempel arbetar med en samling måste ämnet vara identifieraren för samlingen. (I anteckningen från skolans exempel är det du.)
* **exp** *(Expiration)* En tidpunkt då token inte längre är giltig.
* **scope** *(Scope)* Det här är en lista över de behörigheter som har beviljats för ämnet. &quot;Sena för skolan&quot; är ett exempel. Namnet på ett API är ett annat exempel.

## Exempel {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## Svar {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

Ett svar med nya data sedan den senaste begäran:

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## Anteckningar {#section_hj3_crj_11b}

* Ett lyckat anrop till API genererar en HTTP 200-statuskod. Alla andra statuskoder ska betraktas som fel.
* Om värdet inte är null använder du värdet från `data.meta.cursor.next` som `since` parameter i nästa begäran.
* Om värdet från `data.meta.cursor.next` är null betyder det att det inte finns några nya data att använda. Du bör begära om senare med samma `since` värde för att se om nya data har kommit fram.
* I praktiken bör du omedelbart begära mer data om `data.meta.cursor.next` värdet inte är null.
* Det finns ungefär två timmars data tillgängliga via detta API i produktionen.
* Du bör konfigurera processerna så att slutpunkten avfrågas ofta vid kronjobb för att undvika att data saknas. Ett intervall på fem minuter bör vara helt lämpligt för de flesta implementeringar.
