---
description: Ta bort standardkomponenter för Livefyre-appen från din app.
title: Dölj appelement
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
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
