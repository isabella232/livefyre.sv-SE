---
description: Ändra ikonen som visas för Livefyre-användare på menyn @mention.
title: Ändra @mention-ikon
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---

# Ändra `@mention`-ikon {#change-mention-icon}

Ändra ikonen som visas för Livefyre-användare på menyn `@mention`.

Ändra Livefyre-ikonen som används i listrutan `@mention` till en ikon som du väljer, så att du kan ange dina communitymedlemmar med en egen ikon.

## Exempel

Om du vill ändra den här ikonen lägger du till följande CSS i formatmallen. Ersätt &lt;*din resurs*-URL med URL:en för bilden som valts för att ersätta standardmärket för Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
