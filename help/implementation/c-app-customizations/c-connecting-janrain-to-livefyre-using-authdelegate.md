---
description: Livefyre.require har en plugin som gör att auth kan lyssna på Janrain Backplane-bussen.
title: Ansluta Janrain till Livefyre med AuthDelegate
exl-id: d0fe0e88-5827-478b-b2ef-03f06fb3902c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Ansluta Janrain till Livefyre med AuthDelegate{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require har en plugin som gör att auth kan lyssna på Janrain Backplane-bussen.

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

Nedan följer några exempel på hur en auth-delegat kan leta efter en Janrain Capture-integrering.

>[!NOTE]
>
>Din auth-delegat varierar beroende på din Janrain-instans.

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* Det återanrop som skickas till autentiseringsdelegatens inloggningsmetod
* Referensen till din Janrain-fångstvariabel.
* : En referens till objektet Backplan.

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

Utloggning

* **finishLogout:** Det återanrop som skickas till autentiseringsdelegatens inloggningsmetod.

* **window.Backplane:** A reference to your Backplane object.

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

Redigera profil

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

Visa profil

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
