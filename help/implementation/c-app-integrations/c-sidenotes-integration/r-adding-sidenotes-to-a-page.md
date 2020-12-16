---
description: 'null'
seo-description: 'null'
seo-title: Lägga till sidomärken på en sida
solution: Experience Manager
title: Lägga till sidomärken på en sida
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# Lägga till sidobjekt på en sida {#adding-sidenotes-to-a-page}

I Livefyre finns flera konfigurationsalternativ för att placera Sidenotes på sidan:

* Alternativet Väljare definierar elementen som sidotecken ska visas på.
* Fästpunkter representerar element som kan placeras sida vid sida.
* Med den anpassade trådbehållaren kan du definiera var typografitråden ska placeras i relation till det underställda innehållet.
* Med alternativet Antal sidenotes kan du visa antalet sidenotes som lagts till på den angivna platsen.
* Använd flera `ConvConfig`-objekt för att lägga till sidobjekt i flera artiklar på en sida.

## Väljare {#section_wyj_4sv_sy}

Med alternativet Väljare kan Sidenotes hitta innehåll på sidan. Värdet för det här alternativet låter dig dynamiskt avgöra vilka element som ska användas. Det kan vara en väljarsträng (till exempel&quot;#content p, #content img&quot;), ett jQuery-objekt (till exempel `$(‘#content’)`), en array med DOM-element eller ett objekt med två egenskaper: inkludera och exkludera. Sidenotes-appen använder sedan antingen de angivna elementen eller de matchande elementen på sidan. Om du använder egenskaperna include och exclude, tolkar Sidenotes först sidan för att hitta alla element på egenskapen include och tar sedan bort alla element som finns på egenskapen exclude.

## Ankarpunkter {#section_ehq_psv_sy}

Fästpunkter är ett element vars innehåll kan placeras sida vid sida. Ett ankarelement kan innehålla text eller en bild. Alternativet för väljare som skickas under appkonstruktionen avgör ankarelementen.

## Ankarens ID {#section_rsb_rsv_sy}

Ankarpunkter på sidan identifieras med en `data-lf-anchor-id`.

Om du vill ange ID:t för ett ankare själv lägger du till attributet `data-lf-custom-anchor-id` i elementet som du vill mappa till ett ankare. Detta är praktiskt om automatisk identifiering av ankare skulle misslyckas.

Om du t.ex. tänker använda en annan URL-adress för dator- och mobilversionerna av en bild, kan två olika URL-adresser mappas till olika ankarpunkter. Om HTML-koden i stället innehåller ett `data-lf-custom-anchor-id`-värde som är samma på både mobilen och datorn, behandlas bildelementet som en enda ankarpunkt.

Fästpunkter har en typ som bestäms dynamiskt, men som också kan anges explicit med attributet `data-lf-custom-anchor-type`.

>[!NOTE]
>
>Uppräkningens nummervärde måste användas.

Tillgängliga typer är:

* **Text:** 1
* **Bild:** 2
* **Media:** 3
* **Rich:** 4

Mer information om hur du använder metoden [updateAnchors](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) för att lägga till Sidenote-innehåll dynamiskt på sidan finns i &lt;a0/>updateAnchors method&lt;a1/>.`updateAnchors`

## Anpassad trådbehållare {#section_jdh_btv_sy}

Använd alternativet `threadContainerEl` om du vill ange en annan plats för en typografitråd än standardpositionen. När en ankarpunkt är aktiverad visas de som standard intill eller under det aktuella innehållet. Om du vill ändra det här standardvärdet använder du `threadContainerEl` och anger elementet där tråden ska visas.

Det här värdet för det här alternativet fungerar på samma sätt som väljaralternativet, förutom att bara det första giltiga elementet används.

## Sidenotes Count {#section_pld_ntv_sy}

Använd alternativet `numSidenotesEl` om du vill bädda in en valfri widget för antal sidobjekt på sidan. Det här alternativet accepterar samma indata som väljaralternativet, men använder bara det första giltiga elementet i inmatningsarrayen.

Widgeten kommer att dekorera det angivna eller matchade elementet, och kommer att innehålla indataikonen för Sidenotes, antalet Sidenotes som anges på den här positionen samt en hjälpikon.

När du klickar på widgeten visas en pekare med en kort förklaring av sidobjekt och hur du använder dem.

Både förklaringen och exempeltexten kan konfigureras med anpassade strängar ( `questionExplanation` och `questionMockText`). Utseendet på räkningswidgeten och povern kan också konfigureras med anpassade format ( `numSidenotes` respektive `numSidenotesPopover`).

## Lägga till samlingar med flera sidobjekt på en sida {#section_pjl_ptv_sy}

Med Livefyre kan du lägga till flera sidoteckensnittssamlingar på en sida. Om sidan till exempel innehåller tre nyhetsartiklar kanske du vill inkludera tre separata versioner av appen Sidenotes. För att göra detta måste du definiera ett separat `ConvConfig`-objekt för varje instans av Sidenotes som du vill skapa. Exempel:

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
