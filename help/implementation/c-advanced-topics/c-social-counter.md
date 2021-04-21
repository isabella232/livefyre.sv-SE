---
description: Räkna antalet kuraterade sociala objekt.
title: Socialräknare
exl-id: def7fba4-1c2e-4c7b-84f7-f9ede592d675
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Räknare för sociala medier{#social-counter}

Räkna antalet kuraterade sociala objekt. En fullständig lista över tillgängliga slutpunkter finns i avsnittet Livefyre [API Reference](https://api.livefyre.com/docs).

Socialräknarens API returnerar antal matchade kurationsregler i en given samling för intervall över en tidsperiod.

>[!NOTE]
>
>Detta API är bara tillgängligt för Twitter hashtags.

API för räknare för sociala nätverk:

* Resurs
* Regeltyper
* Svar

## Resurs {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** Ditt Livefyre-nätverksnamn har tillhandahållits. Till exempel: *labb* i `labs.fyre.co`.
* **fråga:** Den URL-säkra base64-kodade hash-koden för alla webbplatser, artikel-ID, regeltypstupplar för vilka räkningsinformation ska hämtas (förkodad)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >Frågan är begränsad till 10 plats-, artikel-ID- och regeltypstupplar. (Det föregående exemplet skulle innehålla 3 tupplar.)

* **från** `(optional)` anger den relativa eller absoluta tidsperioden till graf, från anger början och standardvärdet för 24 timmar sedan, om det utelämnas.
* **tills** `(optional)` titel anger den relativa eller absoluta tidsperioden till graf, tills anger början och standardvärdet är den aktuella tiden (nu), om detta utelämnas.

### Relativ tid

| Förkortning | Enhet |
|---|---|
| s | Sekunder |
| min | Minuter |
| h | Timmar |
| d | Dagar |
| w | Veckor |
| mon | 30 dagar (månad) |
| y | 365 dagar (år) |

Exempel:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-7d&until=-6d
```

## Absolut tid {#section_xqr_jgc_11b}

FORMAT: HH:MM_ÅÅÅMMDD

| Förkortning | Betydelse |
|---|---|
| HH | Timmar (i 24-timmarsformat) |
| MM | Minuter |
| YYYY | Fyrsiffrigt år |
| MM | Månad |
| DD | Dag |

Exempel:

```
https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=04:00_20130709 
```

## Regeltyper {#section_v53_xqb_11b}

| Värde | Typ |
|---|---|
| 2 | Twitter |

Exempel:

Om du vill få antal under den sista minuten för plats `123456` och artikel-ID `some-article-id` och regeltyp `2`, till exempel: `123456:some-article-id;2:`

```
curl -XGET "https://labs-t402.bootstrap.fyre.co/api/v3.0/stats.collections.curate/MTIzNDU2OnNvbWUtYXJ0aWNsZS1pZDsy.json&from=-1min" 
```

Exempelsvar:

```
{ 
    "status": "ok", 
    "code": 200, 
    "data": { 
        "123456": { 
            "some-article-id": { 
                "2": [ 
                    [ 
                        2, 
                        1374770460 
                    ], 
                    [ 
                        4, 
                        1374770470 
                    ], 
                    [ 
                        3, 
                        1374770480 
                    ], 
                    [ 
                        1, 
                        1374770490 
                    ], 
                    [ 
                        0, 
                        1374770500 
                    ], 
                    [ 
                        7, 
                        1374770510 
                    ] 
                ] 
            } 
        } 
    } 
}
```
