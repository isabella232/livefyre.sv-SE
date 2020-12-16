---
description: Tillgängliga händelser som du kan binda JavaScript till för konversationsappar (till exempel kommentarer, chatt, live-blogg, granskningar och sidobjekt).
seo-description: Tillgängliga händelser som du kan binda JavaScript till för konversationsappar (till exempel kommentarer, chatt, live-blogg, granskningar och sidobjekt).
seo-title: JavaScript Events-definitioner och exempel
solution: Experience Manager
title: JavaScript Events-definitioner och exempel
uuid: 61da2e2e-8fcd-482d-93df-c946f0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 15%

---


# Definitioner och exempel för JavaScript-händelser{#javascript-events-definitions-and-examples}

Tillgängliga händelser som du kan binda JavaScript till för konversationsappar (till exempel kommentarer, chatt, live-blogg, granskningar och sidobjekt).

Livefyre tillhandahåller JavaScript-händelser för att spåra användaraktivitet i Livefyre-appar. Du kanske vill uppdatera sidan när användare gillar eller delar innehåll på Twitter eller Facebook, eller när nytt innehåll publiceras.

Med Livefyre kan du även lägga till händelser i tredjepartsanalyser (Adobe Analytics JS, Google Analytics, Dynamic Tag Management osv.) för att spåra apphändelser. Mer information får du om du samarbetar med en integrationshanterare från tredje part för att få fram rätt händelser.

Om du vill binda till dessa händelser lägger du till följande kod på sidan när du initierar appen på en sida. Ersätt händelsenamnet för `{eventName}`:

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>Dataobjekt tillhandahålls för alla händelsehanterare. Exempeldataobjekt följer varje händelse.

## commentPosted {#section_qfr_51p_xz}

En användare publicerade en kommentar.

* En överordnad till null är en ny kommentar.
* En överordnad till Ingen är en kommentar som har redigerats.
* Ett nummer för överordnad är det överordnade ID:t för svaret.

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## commentFlagged {#section_szy_s1p_xz}

En användare flaggade en kommentar.

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

En användare gillade en kommentar.

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

En användare delade en kommentar från strömmen. (Den här händelsen utlöses inte när användare delar från kommentarredigeraren.) Den här händelsen utlöses när användaren klickar på knappen Dela.

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

Det totala antalet synliga kommentarer i den här konversationen har ändrats (antingen ökat eller minskat).

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

En användare har loggat in.

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

En användare har loggat ut.

data är odefinierade.

## socialMention {#section_a1w_tz4_xz}

En användare inkluderade ett @mention i en kommentar. Returnerar en array med följande:

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatured

En moderatoranvändare visade en kommentar. Returnerar en array med följande:

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

Kommentarströmmen har lästs in och den inledande uppsättningen innehåll har hämtats från servern och visats för användaren.

data är odefinierade.

## showMore {#section_pqg_nz4_xz}

En användare klickade på knappen **[!UICONTROL Show More]**.

data är odefinierade.

## userFollowed {#section_xxw_jz4_xz}

Returnerar true när en användare klickar på **[!UICONTROL Follow]**-knappen och false när innehållet skickas till strömmen.

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnfollowed {#section_wm1_gz4_xz}

Returnerar true när en användare klickar på knappen **Följ inte** och false när innehåll skickas till strömmen.

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

