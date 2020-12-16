---
description: Ändra ikonen som visas för Livefyre-användare på menyn @mention.
seo-description: Ändra ikonen som visas för Livefyre-användare på menyn @mention.
seo-title: Ändra @mention-ikon
solution: Experience Manager
title: Ändra @mention-ikon
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 30%

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
