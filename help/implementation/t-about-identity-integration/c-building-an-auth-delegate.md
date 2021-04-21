---
description: Objektet AuthDelegate implementerar det beteende du vill ha för att utföra autentiseringsåtgärder och händelser så att du kan anpassa integreringen med webbplatsens befintliga autentiseringssystem.
title: AuthDelegate-objekt
exl-id: 7c669138-627e-476e-a177-c71346f730df
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# AuthDelegate-objekt{#authdelegate-object}

Objektet AuthDelegate implementerar det beteende du vill ha för att utföra autentiseringsåtgärder och händelser så att du kan anpassa integreringen med webbplatsens befintliga autentiseringssystem.

## Skapar ett autentiseringsdelegat {#section_wmn_tv2_gz}

Autentiseringspaketet måste förses med ett autentiseringsdelegat innan det kan utföra en åtgärd. En auth-delegat är ett JavaScript-objekt som implementerar en av metoderna i det här avsnittet.

## .login(finishLogin) {#section_mpk_lv2_gz}

Logga in en giltig användare och anropa funktionen finishLogin med antingen ett Error-objekt om ett fel uppstod, eller användarens Livefyre-inloggningsuppgifter. Vanliga implementeringar av den här metoden dirigerar om användaren till en inloggningssida eller öppnar ett nytt fönster eller modal.

I det här exemplet meddelas autentiseringen av en Livefyre-användare automatiskt med autentiseringstoken, token:

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

Det enklaste inloggningsombudet kan be slutanvändaren om sin token för Livefyre-autentisering.

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## .logOut(finishLogout) {#section_uqz_2v2_gz}

Logga ut en användare och anropa funktionen finishLogout med antingen ett Error-objekt om ett fel uppstod, eller null för att meddela autentiseringen att utloggningen lyckades.

Exempel:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

Vidta åtgärder för att visa en användares profil.

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

Redigera en användares profil genom att vidta åtgärder.

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

Genom att implementera alla metoder som listas ovan kan autentiseringen konfigureras med ett anpassat autentiseringsdelegat. När en delegat har konstruerats kan den anges för autentisering med hjälp av delegatmetoden.

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```
