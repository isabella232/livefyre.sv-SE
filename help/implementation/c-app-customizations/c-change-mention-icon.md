---
description: Ändra ikonen som visas för Livefyre-användare på menyn @mention.
seo-description: Ändra ikonen som visas för Livefyre-användare på menyn @mention.
seo-title: Ändra @mention-ikon
solution: Experience Manager
title: Ändra @mention-ikon
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5

---


# Ändra `@mention` ikon {#change-mention-icon}

Change the icon displayed for Livefyre users in the `@mention` pulldown menu.

Ändra Livefyre-ikonen som används i listrutan till en ikon som du väljer, så att du kan ange dina communitymedlemmar med en egen ikon. `@mention`

## Exempel

Om du vill ändra den här ikonen lägger du till följande CSS i formatmallen. Ersätt &lt;*din resurs*>-URL med URL:en för bilden som valts för att ersätta standardmärket Livefyre.

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
