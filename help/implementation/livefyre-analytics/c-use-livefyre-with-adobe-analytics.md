---
description: Konfigurera Adobe Analytics och Dynamic Tag Manager (DTM) för att samla in data för Livefyre-appar.
title: Använd Livefyre med Adobe Analytics och Dynamic Tag Manager (DTM)
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Använd Livefyre med Adobe Analytics och Dynamic Tag Manager (DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

Konfigurera Adobe Analytics och Dynamic Tag Manager (DTM) för att samla in data för Livefyre-appar.

## Steg 1: Konfigurera händelser i Adobe Analytics {#section_iks_kgd_4cb}

Mappa Livefyre-händelser till en eller flera anpassade lyckade händelser i Adobe Analytics Report Suite Manager.

Mer information om Report Suite Manager finns i [Report Suite Manager](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en).

1. Logga in på Adobe Analytics som Administratörsanvändare.
1. Öppna Adobe Analytics Admin Report Suite Manager.
1. Skapa en ny rapportsvit eller välj en befintlig.
1. Redigera rapportsviten genom att klicka på den rapportsserie som du vill ändra och navigera sedan till **[!UICONTROL Edit Settings > Conversion > Success Events]**.
1. Mappa Livefyre-händelser till en eller flera anpassade lyckade händelser.

## Steg 2: Ställ in konverteringsvariabler

Mappa Livefyre-konverteringsvariabler (eVars) till konverteringsvariabler i Adobe Analytics Admin Report Suite Manager. Konverteringsvariabler fungerar som en sorteringsfunktion som avgör hur du ska identifiera data som samlats in från Livefyre-händelser.

1. Klicka på **[!UICONTROL Edit Settings > Conversion > Conversion Variables]** i Report Suite Manager.
1. Välj de anpassade konverteringsvariabler (eVars) som ska användas och mappa dem till konverteringsvariablerna Livefyre. Så här mappar du en Livefyre-konverteringsvariabel till en anpassad konverteringsvariabel:

   * Aktivera konverteringsvariabeln
   * Namnge konverteringsvariabeln
   * Ge konverteringsvariabeln en typ

1. Spara de anpassade konverteringsvariablerna.

## Steg 3: Använd DTM för att lägga till din Report Suite med Livefyre Events {#section_t15_2hd_4cb}

Använd taggar för att integrera Analytics med Livefyre-händelser. Det gör du genom att skapa en ny egenskap och ett nytt verktyg och lägga till den nya rapportsviten med Livefyre-händelser till egenskapen. Mer information finns i [Översikt över taggar](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).

Du behöver inte utföra det här steget om du redan har ställt in en egenskap eller ett verktyg för rapportsviten som du konfigurerade med Livefyre-händelser.

1. Skapa eller redigera en befintlig egenskap i DTM.
1. Skapa eller redigera ett befintligt Adobe Analytics-verktyg.
1. Om det inte finns något Adobe Analytics-verktyg klickar du på **[!UICONTROL Add a Tool]**.
Ange följande parametrar för verktyget:

   * Ange **[!UICONTROL Tool Type]** till **[!UICONTROL Adobe Analytics]**.
   * Aktivera **[!UICONTROL Automatic Configuration]**.
   * Aktivera **[!UICONTROL Authenticate via Marketing Cloud]**.
1. Lägg till eller bekräfta namnet på rapportsviten med Livefyre-händelser i fältet **[!UICONTROL Report Suites]**.

## Steg 4: Konfigurera en sidinläsningsregel för att konfigurera analyshantering {#section_jfj_j3d_4cb}

Ställ in en sidinläsningsregel för att hämta alla data. Med sidinläsningsregeln kan du lägga in anpassat javascript i regeln som spelar in händelsen när sidan läses in.

>[!NOTE]
>
>Använd inte händelsebaserade regler eller regler för direktsamtal.

1. Välj fliken **[!UICONTROL Rules]** i DTM.
1. Klicka på **[!UICONTROL Page Load Rules]**.
1. Klicka på knappen **[!UICONTROL Create New Rule]**.
1. Öppna avsnittet **[!UICONTROL Conditions]** genom att klicka på knappen **[!UICONTROL Plus]**.
1. Utlös regeln. Välj utlösartyperna **[!UICONTROL DOM Ready]** eller **[!UICONTROL Onload]** om du vill fördröja eller implementera regeln asynkront.
1. (Valfritt) Lägg till ytterligare parametrar för att begränsa vilka sidor som visas i Livefyre-appar. Mer information om ytterligare konfigurationsalternativ finns i [Översikt över taggar](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html).
1. Klicka på fliken **[!UICONTROL Non-sequential]** under **[!UICONTROL Javascript/ Third Party Tags]** och klicka sedan på **[!UICONTROL Add New Script]**.
1. Välj **[!UICONTROL Sequential HTML]** som skripttyp.
1. Lägg till följande skript i kodredigeraren och klicka på **[!UICONTROL Save Code]**.

   Följande skript anropar regeln `livefyre_analytics` för direktanrop efter att Livefyre JavaScript har lästs in. Följande skriptexempel kontrollerar var 400:e ms för att se om `livefyre.analytics` finns på sidan. När sidan har lästs in skickar livefyre.analytics spårningsinformation.

   ```
   /**
   * Poll for Livefyre.analytics object to exist since it gets loaded via the
   * Livefyre.js JavaScript file. Depending on the timing, this could already
   * exist or need a little time.
   */
   function pollForAnalytics() {
   if (Livefyre.analytics) {
     _satellite.track('livefyre_analytics');
       return true;
     }
     setTimeout(pollForAnalytics, 400);
   }
   setTimeout(pollForAnalytics, 400);
   ```

1. Klicka på **[!UICONTROL Save Code]**.
1. Klicka på **[!UICONTROL Save Rule]**.

## Steg 5: Skapa en regel för direktanrop för att konstruera Adobe Analytics Mapping-konfigurationen för Livefyre {#section_gvp_b1g_pdb}

Det finns andra sätt att implementera Livefyre med DTM genom att använda anpassade händelser, Adobe Analytics-gränssnittsfält i DTM och dataelement. I det här dokumentet används anpassad JavaScript för att uppnå samma effekt.

1. I DTM väljer du fliken **Regler** och klickar sedan på **Direct Call Rules**.
1. Klicka på knappen **Skapa ny regel**.
1. Ge den nya regeln namnet **Livefyre Analytics**.
1. Expandera konfigurationsområdet **villkor**.
1. I fältet **String** anger du `livefyre_analytics`.
1. Expandera avsnittet JavaScript/tagg från tredje part och klicka på knappen **Lägg till nytt skript**.
1. Ange **Livefyre Analytics Config** i **taggens namn**-inmatningsrutan.
1. Välj **Icke-sekventiellt JavaScript**.
1. Ange följande Livefyre-konfigurationskod i kodredigeraren och klicka på knappen **Spara kod**.

   ```
   var s = _satellite.getToolsByType('sc')[0].getS();
   
   var evarMap = {
     appId: 'eVar81',
     appType: 'eVar82'
   };
   
   var eventMap = {
     FlagCancel: 'event82',
     FlagClick: 'event82',
     FlagDisagree: 'event82',
     FlagOffensive: 'event82',
     FlagOffTopic: 'event82',
     FlagSpam: 'event82',
     Like: 'event82',
     Load: 'event81',
     RequestMore: 'event82',
     ShareButtonClick: 'event82',
     ShareFacebook: 'event82',
     ShareOnPostClick: 'event82',
     ShareTwitter: 'event82',
     ShareURL: 'event82',
     SortStream: 'event82',
     TwitterLikeClick: 'event82',
     TwitterReplyClick: 'event82',
     TwitterRetweetClick: 'event82',
     TwitterUserFollow: 'event82'
   };
   
    function trackLivefyreEvent(data) {
     var event = eventMap[data.type];
     console.log('Track:', data.type, event);
   
     if (!event) {
       console.warn(data.type, 'is not mapped   to an event in AA');
       return;
     }
     var vars = ['events'];
     switch (event) {
       case 'event82': s.eVar83 = data.type;
         vars.push('eVar83');
         break;
       default:
     }
       ['generator', 'evars'].forEach(function (type) {
       var obj = data[type];
       for (var d in obj) {
         if (obj.hasOwnProperty(d) && evarMap[d]) {
           s[evarMap[d]] = obj[d];
           vars.push(evarMap[d]);
         }
       }
     });
     s.linkTrackVars = vars.join(',');
     s.linkTrackEvents = event;
     s.events = event;
   
     console.log('linkTrackVars:',  s.linkTrackVars);
     console.log('linkTrackEvents:',  s.linkTrackEvents);
     console.log('events:', s.events);
     s.tl();
     }
     ]
   
     /**
   ```

   * Lägger till en analyshanterare för alla analyshändelser från Livefyre. För varje händelse anges data för ett globalt objekt och sedan skickas händelsen.

   ```
   */
   function addAnalyticsHandler() {
     Livefyre.analytics.addHandler(function (events) {
       (events || []).forEach(function (data) {
         console.log('Event handled:', data.type);
         trackLivefyreEvent(data);
       });
     });
   }
   addAnalyticsHandler();
   ```

1. Klicka på **Spara regel**.

## Steg 6: Godkänn ändringar för sidinläsningsregel {#section_pxc_11t_ycb}

1. Gå till fliken **[!UICONTROL Approvals]**.
1. Klicka på **[!UICONTROL Approve]**.
1. Klicka på **[!UICONTROL Yes, approve]** för att bekräfta ditt godkännande.
1. Gå till **[!UICONTROL Overview > Publish Queue]**.
1. Välj den regel som ska publiceras.
1. Klicka på **[!UICONTROL Publish Selected]**.
1. Klicka på **[!UICONTROL Publish]** för att bekräfta att du vill publicera.

## Skript {#section_xkb_vft_mcb}

I följande exempelkod mappas de specifika eVars till tillgängliga Livefyre eVars. Livefyre-konverteringsvariabelns namn ( `eVar`) (till exempel `appId`) mappas till det namn du angav i Report Suite Manager (till exempel `eVar81`). Ändra `eVar`-namnen i det här skriptet till anpassade konverteringsvariabler.


```
var s = _satellite.getToolsByType`('sc')[0]`.getS();
var evarMap = {
  appId: 'eVar81',
  appType: 'eVar82'
};
```

Följande exempelkod mappar de specifika händelser som du ställer in i Report Suite Manager med tillgängliga Livefyre-händelser. I det här exemplet ställs `event82` in som en användarinteraktionshändelse utan att differentiera vilken typ av användarinteraktionshändelse (till exempel länkning eller delning av innehåll). Detta är ett effektivt sätt att registrera all användarinteraktionsinformation i ett -block. Du kan också mappa händelserna i DTM Analytics-gränssnittet med dataelementsreferenser.

```
var eventMap = {
  FlagCancel: 'event82',
  FlagClick: 'event82',
  FlagDisagree: 'event82',
  FlagOffensive: 'event82',
  FlagOffTopic: 'event82',
  FlagSpam: 'event82',
  Like: 'event82',
  Load: 'event81',
  RequestMore: 'event82',
  ShareButtonClick: 'event82',
  ShareFacebook: 'event82',
  ShareOnPostClick: 'event82',
  ShareTwitter: 'event82',
  ShareURL: 'event82',
  SortStream: 'event82',
  TwitterLikeClick: 'event82',
  TwitterReplyClick: 'event82',
  TwitterRetweetClick: 'event82',
  TwitterUserFollow: 'event82'
};
```

I följande exempel anges att om det inte finns någon händelse i den här listan ska du inte göra någonting. Du behöver inte ändra det här kodavsnittet.

```
function trackLivefyreEvent(data) {
  var event = eventMap[data.type];
  console.log('Track:', data.type, event);

  if (!event) {
    console.warn(data.type, 'is not mapped to an event in AA');
    return;
  }
```

Följande kod skiljer de händelsetyper som `event82` spelar in. Konverteringsvariabeln `eVar83` registrerar typen av användarinteraktion och skriptet ställer in `eVar83` för att separera användarinteraktionsdata efter typ. Med `eVar83` kan du dela upp inspelade data i specifika typer av användarinteraktioner.

```
  var vars = ['events'];
  switch (event) {
    case 'event82': s.eVar83 = data.type;
      vars.push('eVar83');
      break;
    default:
  }

  ['generator', 'evars'].forEach(function (type) {
    var obj = data[type];
    for (var d in obj) {
      if (obj.hasOwnProperty(d) && evarMap[d]) {
        s[evarMap[d]] = obj[d];
        vars.push(evarMap[d]);
      }
    }
  });

  s.linkTrackVars = vars.join(',');
  s.linkTrackEvents = event;
  s.events = event;

  console.log('linkTrackVars:', s.linkTrackVars);
  console.log('linkTrackEvents:', s.linkTrackEvents);
  console.log('events:', s.events);

  s.tl();
}
```

Följande kodexempel lägger till en hanterare som lyssnar på alla händelser som inträffar. Den använder sidinläsningsregeln vid inläsning, väntar på att händelser ska finnas, ställer in hanterare för alla händelser från appen och spårar dem. Du behöver inte ändra den här koden.

```
/**
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event.
*/
function addAnalyticsHandler() {
  Livefyre.analytics.addHandler(function (events) {
    (events || []).forEach(function (data) {
      console.log('Event handled:', data.type);
      trackLivefyreEvent(data);
    });
  });
}
```

## Mer info

Mer information om ämnen som behandlas på den här sidan finns i:

* [Report Suite Manager](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)
* [Översikt över taggar](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
