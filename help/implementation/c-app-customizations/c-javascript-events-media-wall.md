---
description: Använd Javascript-händelser för att lyssna efter händelser som inträffar i en medievägg och skicka dem till valfritt analysverktyg.
title: JavaScript-händelser för medievägg
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# JavaScript-händelser för medievägg{#javascript-events-for-media-wall}

Använd Javascript-händelser för att lyssna efter händelser som inträffar i en medievägg och skicka dem till valfritt analysverktyg.

Livefyre tillhandahåller JavaScript-händelser för att spåra användaraktivitet i Livefyre-appar. Du kanske vill uppdatera sidan när användare gillar eller delar innehåll till Twitter eller Facebook, eller när nytt innehåll publiceras.

Här är ett exempel på hur du tar emot händelserna. Ersätt `console.log` med koden för att mappa och skicka händelsen till analysintegreringen (Dynamic Tag Management, Adobe Analytics JS, Google Analytics osv.):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

Lista över medieväggshändelser som stöds:

## Media Wall Events

| Händelse | Definition |
|---|---|
| `Init` | När en medievägg inkluderas på en sida. |
| `Load` | När medieväggen lästes in på en sida, oavsett position. |
| `PostButtonClick` | När en användare klickar på knappen Överför på en medievägg. |
| `RequestMore` | När användaren läser in mer innehåll i en medievägg. |
| `TwitterReplyClick` | När en användare klickar på Twitter-svarsknappen från medieväggen. |
| `TwitterRetweetClick` | När en användare klickar på Twitter Retweet från medieväggen. |
| `TwitterLikeClick` | När en användare klickar på Twitter Gilla/Favorite-knappen från medieväggen. |
| `ModalView` | När användaren klickar för att visa innehållet i Media Wall i ett större modalt fönster. |
| `Like` | När en användare klickar på Gilla-knappen från medieväggen. |
| `ShareButtonClick` | Varje gång en användare klickar på delningsknappen på ett medieväggskort. |
| `ShareURL` | När textområdet Dela till URL är markerat/kopierat från medieväggen. |
| `ShareFacebook` | När du klickar på Dela till Facebook från medieväggen. |
| `ShareTwitter` | När du klickar på Dela till Twitter från medieväggen. |
