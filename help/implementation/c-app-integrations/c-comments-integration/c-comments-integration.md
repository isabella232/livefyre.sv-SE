---
description: Aktivera live-kommentarer på sidan.
title: Kommentarer
exl-id: d62b3dc1-3c5e-45f6-9b21-ea1edcda9812
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# Kommentarer{#comments}

Aktivera live-kommentarer på sidan. Med kommentarer kan du ersätta ditt standardkommentarsystem med realtidskonversationer på sidan.

## Integrering {#concept_4093E8BAA96A464BA74D263DA031C0B0}

När du bäddar in kommentarappen följer du processen för att bädda in en huvudapp som beskrivs i Komma igång > Bädda in en app.

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
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
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

Så som beskrivs i avsnittet Building CollectionMeta är CollectionMeta ett kodat JSON-objekt. I ovanstående exempel har JSON-objektet följande format innan det är JWT-kodat:

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

## NetworkConfig-objekt {#c-networkconfig-object}

Objektet `NetworkConfig` är ett JSON-objekt som anpassar autentiseringssystemet för nätverksanvändare.
Objektet `NetworkConfig` är ett JSON-objekt som innehåller följande parametrar:

| Parameter | Typ | Beskrivning |
|---|---|---|
| **authDelegate** | **  requiredObject | Används för att anpassa autentiseringssystemet för anpassade nätverksanvändare. |
| **nätverk** | Sträng *krävs* | Ett namn som tillhandahålls av Livefyre. Till exempel: *namn.fyre.co.* |
| **attachmentDelegate** | ** alternativt objekt | Används för att ange vilka typer av mediebilagor som visas i appströmmen. Mer information finns i [Begränsa media](/help/implementation/c-app-customizations/c-restrict-media.md#c_restrict_media). |
| **strängar** | ** alternativt objekt | Används för att anpassa textsträngar för HTML-elementen i någon av nyckelapparna Livefyre. Mer information finns i [Stränganpassningar](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md). |

## ConvConfig-objekt {#c-convconfig-object}

Objektet `convConfig` är ett JSON-objekt som används för att ange innehållet som Livefyre-appen återger på sidan.

>[!NOTE]
>
>Objektparametrarna `convConfig` som anges här gäller inte för appen Recensioner. Integrationsinformation om appen Recensioner med objektet `convConfig` finns i Granska integrering.

Objektet `ConvConfig` innehåller följande obligatoriska parametrar:

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| **articleId** | *obligatorisk* sträng | Identifierar unikt en samling inom din webbplats. Vanligtvis motsvarar detta en databasprimärnyckel eller ett Post-ID i ditt CMS-system. Till exempel: &quot;post-42&quot;. Högst 255 tecken.  Obs!  Om du använder artikel-URL:en som artikel-ID kontrollerar du att strängen är MD5- eller SHA-1-kodad. |
| **authPageRelload** | **  valfri boolesk | Gäller kommentarsappen: Används för att styra om en användares kommentar lagras lokalt under autentiseringsprocessen. Om värdet är true, om en användare anger en kommentar och sedan loggar in i appen, lagras kommentaren lokalt och skrivs in igen i innehållsfältet efter inloggning och uppdatering av sidan. Om värdet är false rensas det angivna innehållet under inloggningsprocessen och måste skrivas in igen. |
| **collectionMeta** | *obligatorisk* sträng | JWT-kodade metadata om samlingen. Mer information finns i [CollectionMeta](#c_collectionmeta_object) Object. |
| **el** | *obligatorisk* sträng | ID:t för ett DOM-element som innehållsströmmen ska återges i. |
| **siteId** | *obligatorisk* sträng | Det Livefyre-tillhandahållna ID:t för den webbplats eller det program som samlingen tillhör. Till exempel: &quot;303617&quot;. |

>[!NOTE]
>
>Parametern `app` krävs inte för en implementering av kommentarsappen.

Objektet `ConvConfig` kan även innehålla följande valfria parametrar:

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| **actionButtons** | ** optionalarray | En array med anpassade åtgärdsknappar som du kan lägga till i en del av innehållet bredvid knapparna Dela och Flagga. Mer information finns i Lägga till anpassade knappar. |
| **animeringar** | ** valfri boolesk | Definierar om animeringar ska köras i Livefyre-appen. Ange som false om du vill inaktivera animeringar. Standardvärdet är true. |
| **anonymousFlaggingEnabled** | ** valfri boolesk | Definierar om gästanvändare har möjlighet att flagga innehåll. Standardvärdet är true. |
| **browserType** | ** valfri sträng | Definierar enheten som visningsinnehåll ska genereras för. Detta gör att CSS och vissa funktioner ändras så att de passar indataenhetstypen. Alternativen är stationära, mobila eller surfplattor. (Om inget anges används standardinställningen för Google Agent-bestämning för visningsformatet.) |
| **checksum** | *Rekommenderad* sträng | Identifierar det aktuella tillståndet för CollectionMeta. Om du ändrar det här värdet kommer Livefyre att uppdatera data på servern med de nya värdena i CollectionMeta. |
| **datetimeFormat** | *objektfunktion*  för alternativsträngar | Anger datum/tid-formatet för direktuppspelat innehåll. Mer information finns i Anpassa datum- och tidsstämplar. |
| **disableAvatars** | ** valfri boolesk | Förhindrar att avatarer återges i appströmmen och minskar därmed antalet objekt som läses in i webbläsaren. Standardvärdet är false. |
| **disableIE8Shim** | ** valfri boolesk | Inaktiverar den standardskiftning som används av Livefyre för att polyfyll Internet Explorer 8 så att HTML5-element stöds. Livefyre använder följande projekt:  [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) . Standardvärdet är false.  Obs!  Om det här värdet är false måste någon typ av polyfill användas innan Livefyre Chat anropas för Internet Explorer 8-stöd. |
| **disableThirdPartyAnalytics** | ** valfri boolesk | Inaktiverar analyssystem från tredje part (Quantserve och Google Analytics) som Livefyre kan använda för interna mätningar. Standardvärdet är false. |
| **editorCss** | ** alternativt objekt | Används för att anpassa kommentarredigerarens format. Du kan formatera redigeringsfältets bakgrundsfärg samt teckensnittsfärg, storlek och familj för texten som visas i redigeraren.  Exempel: `{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| **initialNumVisible** | ** valfritt heltal | Gör att du kan ange det standardantal kommentarer som visas i appen vid inläsning. Detta kan vara ett heltal mellan 1 och 50. |
| **initialNumVisibleLegacy** | ** valfritt heltal | Gör att du kan ange standardantalet äldre innehållsobjekt som visas i appen vid inläsning. Detta kan vara ett heltal mellan 1 och 50. Om den här parametern inte anges används initialNumVisible som standard.  Till exempel: Om din samling innehåller 100 aktiva och 100 äldre kommentarer anger du initialNumVisible:10 och initialNumVisibleLegacy:5 för att visa 10 aktiva kommentarer (med knappen Visa mer) + 5 arkivkommentarer (med knappen Visa mer). |
| **maxVisible** | ** valfritt heltal | Anger det maximala antalet synliga delar av innehåll på översta nivån i chattappen. Om nya innehållsdelar direktuppspelas i tas innehåll längst ned i flödet bort från sidan. Om du klickar på knappen Visa fler.. ignoreras parametern och användaren kan visa så mycket innehåll som du vill. (Använd den här parametern för att styra antalet objekt som visas på sidan i strömmar med hög hastighet.) |
| **postToButtons** | ** optionalarray | Används för att konfigurera vilka leverantörer som ska visas när du bäddar in Live Blog App. Det finns två alternativ (Twitter), fb (Facebook) och li (LinkedIn). Standardvärdet är [ tw, fb ]. |
| **readOnly** | ** valfri boolesk | Inaktiverar all interaktivitet för samlingen. Om värdet är true kan användarna inte logga in i strömmen och kan inte publicera, redigera, svara på eller gilla-innehåll. När värdet är true kan användarna flagga och dela innehåll. Standardvärdet är false. |
| **stream** | ** alternativt objekt | Innehåller alternativ för att konfigurera direktuppspelning av appen. |
| **stream.catchup** | ** valfritt heltal | Anger antalet sekunder som strömmen ska läsas in innan den aktuella tidpunkten. Som standard läser Livefyre in 50 innehållsdelar och läser sedan in allt innehåll som skickas mellan dessa och den aktuella tiden. I mycket snabba fall kan innehåll publiceras för snabbt för att appen ska kunna&quot;hinna ifatt&quot;. Använd den här inställningen för att definiera hur många sekunder före nu som innehållet ska bokföras (efter den första inläsningen av innehållet). |
| **stream.delay** | ** valfritt heltal | Anger antalet sekunder mellan direktuppspelningsbegäranden. Använd den här parametern för att styra innehållsflödet och fördröja hur ofta DOM uppdateras.  Obs!  Om den är för stor kan strömmen hamna på efterkälken. |


>[!NOTE]
>
>Du kan skicka ett eller flera `convConfig`-objekt under appinitieringen för att visa flera appar på samma sida. Tänk på att extra appar använder webbläsarresurser och prestanda kan försämras när antalet ökar.

## CollectionMeta-objekt {#c-collectionmeta-object}

Objektet `CollectionMeta` är ett JSON-objekt som anger vilka metadata som ska lagras i samlingen.

`CollectionMeta` är alltid kodad innan den skickas till Livefyre av säkerhetsskäl. Det kodade värdet skickas till `ConvConfig`-objektet som visas ovan.

>[!NOTE]
>
>Du måste lägga till kod på serversidan för att koda JSON-objektet `CollectionMeta`. Mer information finns i Skapa token på serversidan.

| Parameter | Typ | Beskrivning |
|--- |--- |--- |
| **articleId** | *obligatorisk* sträng | Ett unikt ID för samlingen. |
| **title** | *obligatorisk* sträng | Titeln som du vill använda för samlingen. Detta motsvarar ofta titeln på sidan som visar appen.  Till exempel: &quot;Integrationen är så mycket rolig!&quot; <br>**Obs!**  Titelns maximala teckenlängd är 255 tecken. Titelfältet stöder inte HTML-entiteter. Koda specialtecken med UTF-8. |
| **url** | *obligatorisk* sträng | Den absoluta kanoniska URL som du vill bifoga till den här samlingen. Den här URL:en används för att generera länkar tillbaka till appen från innehåll som delas på Facebook och Twitter, e-postmeddelanden och Livefyre Studio.  <br>**** NoteLivefyre kräver ett fullständigt domännamn. portnumret eller ett återanrop för att lösa den lokala konfigurationen krävs inte. Om du testar lokalt måste du vara säker på att du använder en giltig bas-URL-domän. <br>Till exempel:  `https://customer.com` är giltig, men  `https://localhost:5995` inte. När du har konfigurerat den lokala webbservern så att den accepterar ett fullständigt kvalificerat domännamn behövs inga återanrop eller upplösningar och den lokala utvecklingen kan fortsätta som förväntat. |
| **type** | *obligatorisk* sträng | Samlingstypen. Måste vara `livechat`. |

Objektet `CollectionMeta` kan även innehålla följande valfria parameter:

| Parameter | Typ | Beskrivning |
|---|---|---|
| **taggar** | ** valfri sträng | En kommaavgränsad lista med enstaka nyckelord eller fraser. Sök i samlingar efter taggar i Studio eller med söknings-API:t. <br> **Obs!** Taggar som läggs till via Studio kan innehålla mellanslag, men det går inte att använda taggar som anges via API. Använd understreck för att definiera taggar som visar mellanslag i användargränssnittet. (Exempel: använd `Monday_Quarterback` för att visa måndag-kvarterback i Studio.) |

## Lägga till en händelsehanterare {#concept_06D8B811C98B4CC6B38C6340EBA176E5}

Om du vill registrera händelsehanterare använder du widget.on-anropet i appens callback-funktion.

### Exempel

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```
