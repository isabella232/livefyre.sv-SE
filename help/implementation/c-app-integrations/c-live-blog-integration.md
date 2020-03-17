---
description: Med Live Blog kan du visa uppdateringar och bilder i realtid från webbplatsens egna redigerare när du täcker in en live-händelse.
seo-description: Med Live Blog kan du visa uppdateringar och bilder i realtid från webbplatsens egna redigerare när du täcker in en live-händelse.
seo-title: Live Blog
solution: Experience Manager
title: Live Blog
uuid: 5ca373f1-2008-45ab-9ec2-1e295af4e368
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934

---


# Live Blog{#live-blog}

Med Live Blog kan du visa uppdateringar och bilder i realtid från webbplatsens egna redigerare när du täcker in en live-händelse.

## Live Blog {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

Med Live Blog kan du visa uppdateringar och bilder i realtid från webbplatsens egna redigerare när du täcker in en live-händelse.

## Integrering {#c_live_blog_integration}

Med Live Blog kan du visa uppdateringar och bilder i realtid från webbplatsens egna redigerare när du täcker in en live-händelse.

Följ proceduren för att bädda in ett Live-blogginlägg när du vill bädda in ett program. Se [Bädda in ett program](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Följande är ett exempel på hur ett inbäddat Live Blog App ser ut.

### Exempel

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(blogWidget) {}); 
        auth.delegate({ 
          login: function (callback) { 
            callback(null,{livefyre:'<userauthtoken>'}); 
          }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

CollectionMeta är ett kodat JSON-objekt. I ovanstående exempel har JSON-objektet följande format innan det är JWT-kodat:

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## NetworkConfig-objekt {#c-networkconfig-object}

Objektet `NetworkConfig` är ett JSON-objekt som anpassar autentiseringssystemet för nätverksanvändare.

Objektet är ett JSON- `NetworkConfig` objekt som innehåller följande parametrar:

| Parameter | Typ | Beskrivning |
|---|---|---|
| **authDelegate** | *obligatoriskt* objekt | Används för att anpassa autentiseringssystemet för anpassade nätverksanvändare. |
| **nätverk** | *obligatorisk* sträng Ett namn som tillhandahålls av Livefyre. Till exempel: *namn.fyre.co.* |
| **attachmentDelegate** | *valfritt* objekt | Används för att ange vilka typer av mediebilagor som visas i appströmmen. Mer information finns i [Begränsa media](../c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **strängar** | *valfritt* objekt | Används för att anpassa textsträngar för HTML-elementen i någon av nyckelapparna Livefyre. Mer information finns i [Stränganpassningar](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## ConvConfig-objekt {#c-convconfig-object}

Objektet är ett JSON-objekt som används för att ange det innehåll som Livefyre-appen återger på sidan. `convConfig`

>[!NOTE]
>
>Objektparametrarna som anges här gäller inte för appen Recensioner. `convConfig` Integrationsinformation om appen Recensioner med objektet finns i Granska integrering. (på `convConfig` engelska).

Objektet `ConvConfig` innehåller följande obligatoriska parametrar:

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| **articleId** | *obligatorisk* sträng | Identifierar unikt en samling inom din webbplats. Vanligtvis motsvarar detta en databasprimärnyckel eller ett Post-ID i ditt CMS-system. Till exempel: &quot;post-42&quot;. Högst 255 tecken.  Obs!  Om du använder artikel-URL:en som artikel-ID kontrollerar du att strängen är MD5- eller SHA-1-kodad. |
| **collectionMeta** | *obligatorisk* sträng | JWT-kodade metadata om samlingen. Mer information finns i CollectionMeta Object. |
| **el** | *obligatorisk* sträng | ID:t för ett DOM-element som innehållsströmmen ska återges i. |
| **siteId** | *obligatorisk* sträng | Det Livefyre-tillhandahållna ID:t för den webbplats eller det program som samlingen tillhör. Till exempel: &quot;303617&quot;. |

>[!NOTE]
>
>Parametern `app` krävs inte för en implementering av kommentarappen.

Objektet kan också innehålla följande valfria parametrar: `ConvConfig`

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| **actionButtons** | *valfri* array | En array med anpassade åtgärdsknappar som du kan lägga till i en del av innehållet bredvid knapparna Dela och Flagga. Mer information finns i Lägga till anpassade knappar. |
| **animeringar** | *valfri* boolesk | Definierar om animeringar ska köras i Livefyre-appen. Ange som false om du vill inaktivera animeringar. Standardvärdet är true. |
| **anonymousFlaggingEnabled** | boolesk | Definierar om gästanvändare har möjlighet att flagga innehåll. Standardvärdet är true. |
| browserType | *optional* String | Definierar enheten som visningsinnehåll ska genereras för. Detta gör att CSS och vissa funktioner ändras så att de passar indataenhetstypen. Alternativen är stationära, mobila eller surfplattor. (Om inget anges används standardinställningen för Google Agent-bestämning för visningsformatet.) |
| **checksum** | *valfri* sträng (rekommenderas) | Identifierar det aktuella tillståndet för CollectionMeta. Om du ändrar det här värdet kommer Livefyre att uppdatera data på servern med de nya värdena i CollectionMeta. |
| **datetimeFormat** | *valfri* strängobjektfunktion | Anger datum/tid-formatet för direktuppspelat innehåll. Mer information finns i Anpassa datum- och tidsstämplar. |
| disableAvatars | *valfri* boolesk | Förhindrar att avatarer återges i appströmmen och minskar därmed antalet objekt som läses in i webbläsaren. Standardvärdet är false. |
| disableIE8Shim | *valfri* boolesk | Inaktiverar den standardskiftning som används av Livefyre för att polyfyll Internet Explorer 8 så att HTML5-element stöds. Livefyre använder följande projekt:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . Standardvärdet är false.  Obs!  Om det här värdet är false måste någon typ av polyfill användas innan Livefyre Chat anropas för Internet Explorer 8-stöd. |
| **disableThirdPartyAnalytics** | *valfri* boolesk | Inaktiverar analyssystem från tredje part (Quantserve och Google Analytics) som Livefyre kan använda för interna mätningar. Standardvärdet är false. |
| **editorCss** | *valfritt* objekt | Används för att anpassa kommentarredigerarens format. Du kan formatera redigeringsfältets bakgrundsfärg samt teckensnittsfärg, storlek och familj för texten som visas i redigeraren.  Till exempel: {background: #ccc, color: &quot;red&quot;, teckensnitt: &quot;30px &quot;Helvetica Neue&quot;, Helvetica, Arial, Genève, sans-serif&quot;} |
| **initialNumVisible** | *valfritt* heltal | Gör att du kan ange det standardantal kommentarer som visas i appen vid inläsning. Detta kan vara ett heltal mellan 1 och 50. |
| **initialNumVisibleLegacy** | *valfritt* heltal | Gör att du kan ange standardantalet äldre innehållsobjekt som visas i appen vid inläsning. Detta kan vara ett heltal mellan 1 och 50. Om den här parametern inte anges används initialNumVisible som standard.  Till exempel: Om din samling innehåller 100 aktiva och 100 äldre kommentarer anger du initialNumVisible:10 och initialNumVisibleLegacy:5 för att visa 10 aktiva kommentarer (med knappen Visa mer) + 5 arkivkommentarer (med knappen Visa mer). |
| **maxVisible** | *valfritt* heltal | Anger det maximala antalet synliga delar av innehåll på översta nivån i chattappen. Om nya innehållsdelar direktuppspelas i tas innehåll längst ned i flödet bort från sidan. Om du klickar på knappen Visa fler.. ignoreras parametern och användaren kan visa så mycket innehåll som du vill. (Använd den här parametern för att styra antalet objekt som visas på sidan i strömmar med hög hastighet.) |
| **postToButtons** | *valfri* array | Används för att konfigurera vilka leverantörer som ska visas när du bäddar in Live Blog App. Tillgängliga alternativ är två (Twitter), fb (Facebook) och li (LinkedIn). Standardvärdet är [ tw, fb ]. |
| **readOnly** | *valfri* boolesk | Inaktiverar all interaktivitet för samlingen. Om värdet är true kan användarna inte logga in i strömmen och kan inte publicera, redigera, svara på eller gilla-innehåll. När värdet är true kan användarna flagga och dela innehåll. Standardvärdet är false. |
| **stream** | *valfritt* objekt | Innehåller alternativ för att konfigurera direktuppspelning av appen. |
| stream.catchup | *valfritt* heltal | Anger antalet sekunder som strömmen ska läsas in innan den aktuella tidpunkten. Som standard läser Livefyre in 50 innehållsdelar och läser sedan in allt innehåll som skickas mellan dessa och den aktuella tiden. I mycket snabba fall kan innehåll publiceras för snabbt för att appen ska kunna&quot;hinna ifatt&quot;. Använd den här inställningen för att definiera hur många sekunder före nu som innehållet ska bokföras (efter den första inläsningen av innehållet). |
| **stream.delay** | *valfritt* heltal | Anger antalet sekunder mellan direktuppspelningsbegäranden. Använd den här parametern för att styra innehållsflödet och fördröja hur ofta DOM uppdateras.  Obs!  Om den är för stor kan strömmen hamna på efterkälken. |


>[!NOTE]
>
>Du kan skicka ett eller flera `convConfig` objekt under appinitieringen för att visa flera appar på samma sida. Tänk på att extra appar använder webbläsarresurser och prestanda kan försämras när antalet ökar.

## CollectionMeta-objekt {#c-collectionmeta-object}

Objektet `CollectionMeta` är ett JSON-objekt som anger metadata som ska lagras i samlingen.

`CollectionMeta` är alltid kodad innan den skickas till Livefyre av säkerhetsskäl. Det kodade värdet skickas till det `ConvConfig` objekt som visas ovan.

>[!NOTE]
>
>Du måste lägga till kod på serversidan för att koda `CollectionMeta` JSON-objektet. Mer information finns i Skapa token på serversidan.

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| **articleId** | *obligatorisk* sträng | Ett unikt ID för samlingen. |
| **title** | *obligatorisk* sträng | Titeln som du vill använda för samlingen. Detta motsvarar ofta titeln på sidan som visar appen.  Till exempel: &quot;Integrationen är så mycket rolig!&quot;  Obs!  Titeln får innehålla högst 255 tecken. Titelfältet stöder inte HTML-entiteter. Koda specialtecken med UTF-8. |
| **url** | *obligatorisk* sträng | Den absoluta kanoniska URL som du vill bifoga till den här samlingen. Den här URL:en används för att generera länkar tillbaka till appen från innehåll som delas på Facebook och Twitter, e-postmeddelanden och Livefyre Studio.  Obs!  Livefyre kräver ett fullständigt domännamn. portnumret eller ett återanrop för att lösa den lokala konfigurationen krävs inte. Om du testar lokalt måste du vara säker på att du använder en giltig bas-URL-domän. (Exempel: `https://customer.com` är giltig, men `https://localhost:5995` är inte giltig.) När du har konfigurerat den lokala webbservern så att den accepterar ett fullständigt kvalificerat domännamn behövs inga återanrop eller upplösningar och den lokala utvecklingen kan fortsätta som förväntat. |
| **type** | *required* String | Samlingstypen. Måste vara livechat. |

Objektet kan också innehålla följande valfria parameter: `CollectionMeta`

| Parameter | Typ | Beskrivning |
|---|---|---|
| **taggar** | *valfri* sträng | En kommaavgränsad lista med enstaka nyckelord eller fraser. Sök i samlingar efter taggar i Studio eller med söknings-API:t. **Obs!** Taggar som läggs till via Studio kan innehålla mellanslag, men det går inte att använda taggar som anges via API. Använd understreck för att definiera taggar som visar mellanslag i användargränssnittet. (Exempel: använd måndag_kvarterback för att visa måndag-kvarterback i Studio.) |

## Lägga till en händelsehanterare {#concept_D835C710A7214F6D921571E0770B6BC5}

Om du vill registrera händelsehanterare använder du widget.on-anropet i appens callback-funktion.

Exempel:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

