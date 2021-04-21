---
description: Kunder som använder Janrain Capture och Backplane kan använda Livefyre Auth för enkel inloggning (SSO), vilket gör att användare kan använda dina Livefyre-appar direkt när de loggar in på din webbplats.
title: Janrain Capture/Backplane
exl-id: c7e6cfef-7570-4f9c-9d2c-79f890ee5c49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# Janrain Capture/Backplane{#janrain-capture-backplane}

Kunder som använder Janrain Capture och Backplane kan använda Livefyre Auth för enkel inloggning (SSO), vilket gör att användare kan använda dina Livefyre-appar direkt när de loggar in på din webbplats.

För att kunna dra nytta av den inbyggda integreringen av Capture/Backplane måste du göra konfigurationsändringar i både Capture-appen och LiveFyre.js-integreringen.

>[!NOTE]
>
>Hoppa över det här avsnittet om du inte använder Janrain Capture.

Mer information finns i [dokumentationen för Janrain’s Backplane](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/).

1. [Konfigurera Capture.](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (Valfritt) [Lägg till Livefyre-standardvärden till Capture App](#c_janrain_capture_backplane/section_z2s_txt_bbb).
1. [Bygg AuthDelegate-objektet.](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [Synkronisera med Livefyre med Ping for Pull.](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## Steg 1: Konfigurera hämtning {#section_r2f_kxt_bbb}

Livefyre behöver vissa autentiseringsuppgifter från din Janrain Capture-app.

1. Konfigurera appen Janrain Capture.
1. Samla in följande information för Livefyre:

   * Åtkomst till din Janrain Capture-instans.
   * Åtkomst till din Janrain Engage-panel.
   * Dina hämtningsinställningar och autentiseringsuppgifter.
   * Dina inloggningsuppgifter.
   * Din identitet-URL.

>[!NOTE]
>
>Livefyre får data direkt från CNAME. Därför kan den här identitets-URL:en inte vara en CNAMEd-post (en vanity-URL CNAME) som matchar Janrain Capturs faktiska CNAME.

## Steg 2: (Valfritt) Lägg till Livefyre-standardvärden i Capture-appen {#section_z2s_txt_bbb}

Lägg till Livefyre som standard till användare som lagras i Capture-appen så att du kan skicka e-postmeddelanden till användare eller låta dem automatiskt följa konversationer som användare kommenterar i.

1. Slutför [steg 1: Konfigurera Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb).
1. Lägg till följande standardfält för Livefyre. Alla fält är valfria.

| Parameter | Typ | Beskrivning |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | Sträng | Meddela användaren när någon kommenterar en artikel som han/hon följer. Kan vara omedelbart, ofta eller aldrig. |
| **[!UICONTROL livefyre_likes]** | Sträng | Meddela användaren när någon gillar något av deras inlägg. Kan vara omedelbart, ofta eller aldrig. |
| **[!UICONTROL livefyre_replies]** | Sträng | Meddela användaren när någon svarar på ett av sina inlägg.Kan vara omedelbart, ofta eller aldrig. |
| **[!UICONTROL livefyre_moderator_comments]** | Sträng | Meddela moderatorn när någon kommenterar en konversation som de modererar.Kan vara omedelbart, ofta eller aldrig. |
| **[!UICONTROL livefyre_moderator_flags]** | Sträng | Meddela moderatorn när någon flaggar ett inlägg i en konversation som de modererar.Kan vara omedelbart, ofta eller aldrig. |
| **[!UICONTROL livefyre_autofollow_conversations]** | Boolean | Låt användaren följa en konversation automatiskt när han/hon lämnar ett inlägg. Kan vara sant eller falskt. |

## Steg 3: Bygg AuthDelegate-objektet för Janrain-integrering {#section_asv_vyt_bbb}

Livefyre.require har en plugin som gör att auth kan lyssna på Janrain Backplane-bussen.

### Inloggning {#login}

När ett identitets-/inloggningsmeddelande skickas i bakplanskanalen anropas auth.authenticate() åt dig med användarens Livefyre Authentication-token. Du måste fortfarande implementera en AuthDelegate.

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>Objektet window.Backplan måste definieras på sidan innan du anropar auth.plugin med plugin-programmet Livefyre Backplane. Om du vill vara säker på att Backplane-objektet är tillgängligt anropar du Livefyre-instansieringskoden från ett onReady-återanrop. Kontakta din Janrain-kontakt för att avgöra när andra program får använda objektet Backplane.



>[!NOTE]
>
>Din auth-delegat varierar beroende på din Janrain-instans.

Nedan följer några exempel på hur en auth-delegat kan leta efter en Janrain Capture-integrering.

* `errback`: Det återanrop som skickas till autentiseringsdelegatens inloggningsmetod
* `janrain`: Referensen till din Janrain-fångstvariabel.
* `window.Backplane`: En referens till objektet Backplan.

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

### Logga ut {#logout}

* `finishLogout`: Det återanrop som skickas till autentiseringsdelegatens inloggningsmetod.

* `window.Backplane`: En referens till objektet Backplan.

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

### Redigera profil {#editprofile}

Detta kan länka till den del av webbplatsen som du vill att användarna ska besöka för att visa sin egen profilsida. I det här exemplet skrivs bara författarobjektet som skickats ut.

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### Visa profil {#viewprofile}

Precis som Redigera profil bör detta länka till en användarsida som skiljer sig från den inloggade användaren. Detta kan implementeras hur du vill. I det här exemplet loggas bara författarparametern till konsolen.

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## Steg 4: Synkronisera med Livefyre med Ping for Pull för Janrain-integrering {#section_ilv_bzt_bbb}

Om du vill synkronisera Livefyre-fjärrprofiler med ditt Capture-användarhanteringssystem måste du utföra en serie steg som kallas Ping for Pull. Den här processen kräver att du hämtar en giltig åtkomsttoken från Janrain och sedan skickar den token till en slutpunkt som anges i steg 3 nedan.

1. Få en åtkomstkod från Janrain.

   Om du vill hämta åtkomstkoden anger du de nödvändiga inloggningsuppgifterna, anger user_type som &quot;user&quot; och uuid som den aktuella användarens uuid som ska uppdateras. Mer information finns i [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/).

1. Byt åtkomstkod för en åtkomsttoken. Ange de nödvändiga inloggningsuppgifterna, åtkomstkoden som togs emot från steg 1 och ange grant_type som &quot;permission_code&quot;.

   Mer information finns i [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/).

1. Tryck på slutpunkten &quot;Ping to pull Capture&quot; för Livefyre.

   Slutpunkts-URL: [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] där ***{networkName}*** är det nätverksnamn som tillhandahålls av Livefyre, och jrtoken är den token som tas emot från Janrain i steg 2.

   När du nått den här slutpunkten får du ett svar från 202 och Livefyre påbörjar en asynkron process.

## Så här fungerar allt {#concept_mty_f31_2cb}

För att kunna dra nytta av den inbyggda integreringen av Capture/Backplane måste du göra några konfigurationsändringar i både Capture-appen och LiveFyre.js-integreringen.

Janrain skickar lyckade inloggnings-/utloggningsmeddelanden via Backplane-bussen, som Livefyre-appen lyssnar på när den är korrekt konfigurerad. Dessa meddelanden innehåller all information som behövs för att visa appanvändare som inloggade eller utloggade. Utvecklare kan visa Backplane-bussmeddelanden genom att granska fliken Nätverk i webbläsarens utvecklarkonsol.

## Exempel på inloggningskod {#section_ftt_tvp_mz}

Begäran:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

Svar:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

Tomt svar:

```
Backplane.response([]);
```

## Exempel på utloggningskod {#section_t52_svp_mz}

Begäran:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

Svar:

```
Backplane.finishInit("{CHANNEL}");
```

Om de här meddelandena inte visas i dina nätverksbegäranden kommer Livefyre inte att känna till inloggnings-/utloggningsförsöken och därför kommer Livefyre inte att kunna integrera användaren i appen.
