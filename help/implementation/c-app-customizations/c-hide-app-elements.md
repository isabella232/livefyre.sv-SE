---
description: Ta bort standardkomponenter för Livefyre-appen från din app.
seo-description: Ta bort standardkomponenter för Livefyre-appen från din app.
seo-title: Dölj appelement
solution: Experience Manager
title: Dölj appelement
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Dölj appelement{#hide-app-elements}

Ta bort standardkomponenter för Livefyre-appen från din app.

Använd CSS för att dölja standardelementen i Livefyre App på sidan, så att du kan anpassa användarupplevelsen efter dina behov.

Om du vill dölja element från appen anger du helt enkelt Ingen för visning.

Exempel:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```

