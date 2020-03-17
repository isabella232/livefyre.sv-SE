---
description: Räkna antalet kuraterade sociala objekt.
seo-description: Räkna antalet kuraterade sociala objekt.
seo-title: Socialräknare
solution: Experience Manager
title: Socialräknare
uuid: fa9aa1a8-6a04-4bc1-9bfe-e42c1250fd48
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Socialräknare{#social-counter}

Räkna antalet kuraterade sociala objekt. En fullständig lista över tillgängliga slutpunkter finns i avsnittet om Livefyre [API-referens](https://api.livefyre.com/docs) .

Socialräknarens API returnerar antal matchade kurationsregler i en given samling för intervall över en tidsperiod.

>[!NOTE]
>
>Detta API är bara tillgängligt för Twitter-hashtaggar.

API för räknare för sociala nätverk:

* Resurs
* Regeltyper
* Svar

## Resurs {#section_p2s_2hc_11b}

```
GET https://{networkName}.bootstrap.fyre.co/api/v3.0/stats.collections.curate/{query}.json
```

* **networkName:** Ditt Livefyre-nätverksnamn angavs. Till exempel: *labb* in `labs.fyre.co`.
* **fråga:** Den URL-säkra bas64-kodade hash-koden för alla webbplatser, artikel-ID och regeltyper som räkningsinformation ska hämtas för (förkodad)

   ```
   {site ID}:{article ID};{rule-type},  {article ID};{rule-type}|{site ID}:{article ID};{rule-type}
   ```

   >[!NOTE]
   >Frågan är begränsad till 10 plats-, artikel-ID- och regeltypstupplar. (Det föregående exemplet skulle innehålla 3 tupplar.)

* **från** `(optional)` specificera den relativa eller absoluta tidsperioden till graf, från anger början och standardvärdet för 24 timmar sedan, om det utelämnas.
* **till** dess att `(optional)` den relativa eller absoluta tidsperioden för diagram anges, tills anger början och standardvärdet är den aktuella tiden (nu), om detta utelämnas.

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

Så här erhåller du antal under den sista minuten för webbplats- `123456` och artikel-ID `some-article-id` och regeltyp `2`till exempel: `123456:some-article-id;2:`

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
