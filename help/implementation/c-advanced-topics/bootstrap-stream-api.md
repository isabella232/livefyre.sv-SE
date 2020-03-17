---
description: Använd Bootstrap- och Stream API med Livefyre-appar.
seo-description: Använd Bootstrap- och Stream API med Livefyre-appar.
seo-title: Använd Bootstrap- och Stream API med Livefyre-appar
solution: Experience Manager
title: Visa kontoinformation
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# Använd Bootstrap- och Stream API med Livefyre-appar {#bootstrap-stream-api}

## Bootstrap-API {#bootstrap-api}

### Hur hämtar jag innehåll som är äldre än de senaste 50 bitarna? {#howcontentolder}

Bootstrap är allt innehåll i en Livefyre-app. Det är cachelagrade data, vanligtvis 12-20 minuter gamla. Den levereras i grupper om 50 delar och är sidnumrerad så att du kan hämta innehåll som är äldre än 50 delar.

[API-referens](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[Exempelbegäran](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

Exempelbegäran ovan läser in `init` sidan som innehåller samlingsinställningar och den enda ursprungliga uppsättningen ~50 bitar av det senaste innehållet. Om du vill avsöka äldre innehåll måste du läsa in efterföljande startsidor med `N` sidnumret:

Begäran: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

Ett exempelprogram har t.ex. 120 innehållsdelar. Innehållet&quot;1&quot; är det äldsta innehållet och Innehåll&quot;70&quot; är det senaste innehållet.

* `Init` läser in ~120-70 innehållsdelar i fallande ordning: [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` läser in ~ 1-50 innehållsdelar i stigande ordning: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` läser in ~ 51-100 innehållsdelar i stigande ordning: [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` läser in ~101-120 innehållsdelar i stigande ordning:[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[Klicka här för att se Bootstrap Poll FlowChart.](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## API för direktuppspelning {#stream-api}

Vad är Stream API?
Strömmen är en lång omröstning som enligt design ska vara öppen i cirka 30 sekunder. Beskrivning av tekniken Lång avsökning finns här: [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

Denna slutpunkt för långvarig avsökning strömmar nytt innehåll (t.ex. en användare skickar en kommentar), innehållsstatusändringar (t.ex. användaren tar bort sin kommentar, gilla-markering) och modereringsändringar av innehållet (t.ex. moderatorn godkänner ett visst innehåll) till en Livefyre-app.

Begäran till Stream API ska vara ~30 sekunder (långavsökning) med förväntad tidsgräns efter 30 sekunder när inget nytt innehåll strömmas in.

API-referens: [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

Exempelbegäran:

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

Observera: Svaret `maxEventId` i ett Stream API är det högsta händelse-ID:t för uppdateringarna i det här svaret. Använd det här värdet som `lastEventId` path-parameter när du skapar URL:en för nästa Stream API-begäran för att få uppdateringar efter alla uppdateringar i det här svaret.

Exemplet nedan är baserat på en kommentarsapp:

Kommentaren &quot;Första kommentaren&quot; publicerades först. &quot;Andra kommentaren&quot; publicerades efter.

API-svar för första kommentarströmmen:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Svaret `maxEventId` i är &quot;1520289700953369&quot;, som kommer att användas för `lastEventId` att avfråga slutpunkten för att få uppdateringar (dvs. den andra kommentaren) som inträffar efter alla uppdateringar i det här svaret.

Andra kommentarströmmens API-svar:

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

Svaret `maxEventID` &quot;1520289700953369&quot; bör i sin tur användas som `lastEventID` ett sätt att skapa Stream API-svar för nästa uppdatering.