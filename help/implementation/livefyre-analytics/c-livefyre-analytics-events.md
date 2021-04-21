---
title: Livefyre Analytics Events
description: Livefyre Analytics Events
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Livefyre Analytics Events

## Händelseobjektsdefinition {#section_dh1_yhn_pdb}

Följande kod definierar de fält i händelseobjektet som tas emot av analyshanteraren på en sida.

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Livefyre Analytics Events och eVars {#section_u3k_tft_mcb}

Följande Livefyre-händelser som ska mappas till anpassade händelser som ska användas i rapporter med Report Suite Manager. Mer information om rapportsviter i Adobe Analytics finns i [Report Suite Manager](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html). Mer information om hur du använder Livefyre-händelser med Report Suite Manager finns i [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb).

## Livefyre Analytics Events

| Händelse | Beskrivning |
|---|---|
| Init | När en sida som innehåller minst en Livefyre-app läses in |
| Läs in | När som helst när en app lästes in på en sida oavsett användarvy |
| Visa | När en app gick in i visningsrutan för första gången. |
| Bokför | Varje gång en användare skriver in en kommentar eller ett innehåll, inklusive ex: inlägg på högsta nivån, svar, recensioner, medieväggsöverföringar |
| Bokfört | När ett inlägg lyckades. |
| Twitter_Svara | En användare svarade när som helst på Twitter |
| Twitter_Gilla | Var innehåll delades: Retweet |
| Livefyre_Like | När som helst används livefyllliknande funktion i en app |
| Livefyre_Till skillnad | När som helst ogillar en användare en |
| ShareOnPost | Varje gång en användare publicerar innehåll och använder funktionen för delning efter publicering |
| ShareButtonClick | Varje gång en användare klickar på delningsknappen på en kommentar |
| ShareTwitter | När du klickar på Dela till Twitter |
| ShareFacebook | När du klickar på Dela till Facebook |
| ShareURL | När textområdet Dela till URL är markerat/kopierat. |
| ExpanderaSvar | När en användare klickar på länken + eller Expandera för att visa alla svar på ett inlägg på den översta nivån |
| KomprimeraSvar | När en användare klickar på länken - eller Komprimera för att visa alla svar på ett inlägg på den översta nivån |
| FlaggaKlicka | När som helst när en användare öppnar flaggmodulen |
| FlagSpam | När en användare flaggar innehåll som skräppost |
| FlaggaAcceptera inte | När en användare flaggar innehållet som oense |
| FlagOffensive | När en användare flaggar innehåll som stötande |
| FlaggaAvÄmne | När en användare flaggar innehåll som utanför ämne |
| FlaggaAvbryt | När som helst när en användare klickar på X eller &quot;avbryter&quot; när en flagga skickas |
| FöljSamling | När som helst efter en konversation (&quot;jag är intresserad&quot; i recensioner) |
| UnfollowCollection | När en konversation inte följs |
| RequestMore | När som helst när en användare har läst in mer innehåll i en app (måste vara för hög hastighet också) |
| ModalView | Varje gång en användare klickar för att visa innehåll i en modal |
| TwitterRetweetKlicka | Var innehåll delades: Retweet |
| PostButtonClick | När en användare klickar på inlägget (&quot;Vad vill du ha?&quot;) knapp |
| Inloggning | När som helst när en användare loggade in |
| Utloggning | När som helst när en användare loggade ut |

Nedan följer en lista med konverteringsvariabler (eVars) som finns i Livefyre.

## Konverteringsvariabler - eVars

| Händelse | Beskrivning |
|--- |--- |
| Nätverks-ID | Nätverks-ID/namn i Livefyre |
| Program-ID | Programmets URN |
| Kontext-ID | Innehålls-ID i Livefyre |
| Apptyp | Livefyre-apptyp. Alternativ: <br><ul><li>Live Blog  </li><li> Funktionskort</li><li>Carousel</li><li>Chatt </li><li>Kommentarer</li><li>Bildband</li><li>Karta</li><li>Mosaik</li><li>Media Wall</li><li>Trender</li><li>Knappen Överför</li></ul> |
| Innehållstyp | Instagram, Twitter, Facebook, LiveFyre, YouTube m.m. |

## Mer info {#section_b3d_4yl_pdb}

Mer information om ämnen som behandlas på den här sidan finns i:

* [Report Suite ](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[ManagerDTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [Regler](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
