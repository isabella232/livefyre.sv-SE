---
description: Lägg till en användartagg i ett konto för att lägga till en användare i en grupp.
seo-description: Lägg till en användartagg i ett konto för att lägga till en användare i en grupp.
seo-title: Lägga till användare i grupper
solution: Experience Manager
title: Lägga till användare i grupper
uuid: 3633f2df-8d60-4cdd-b9a2-3807218c74a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Lägga till användare i grupper{#adding-users-to-groups}

Lägg till en användartagg i ett konto för att lägga till en användare i en grupp.

Användartaggar kan implementeras för både egna system och företagsprofilsystem och kan läggas till på konton på flera sätt:

* Om du skapar ägare och moderatorer via Studio tilldelas användartaggen&quot;Moderator&quot; till kontot.
* När du skapar användargrupper och lägger till användare via Studio, används automatiskt användartaggar med namnet på gruppen för de valda användarna.
* Användartaggar kan även användas direkt på konton med HTTP [-anropet](https://api.livefyre.com/docs#add-user-tag) Lägg till användartagg eller Ping for Pull.

>[!NOTE]
>
>Båda API-metoderna, HTTP Add User Tag call och metoden Ping for Pull, skriver över taggar som tidigare tilldelats kontot på andra sätt. Välj därför en metod och använd den konsekvent genom hela processen.

## Lägga till en användare i en grupp från sidan Användare i Studio {#section_qgq_nbw_xz}

* Klicka **[!UICONTROL Add Group]** eller gruppetiketten under ett användarnamn för att öppna gruppmenyn.
* Bläddra igenom listan och hitta gruppen som du vill lägga till användaren i. Du kan ange ett gruppnamn i **[!UICONTROL Search]** rutan högst upp i listrutan.
* Klicka i kryssrutan bredvid gruppen/grupperna som användaren ska läggas till i och tryck sedan på Retur.

Användarens profil visar antingen namnet på gruppen (om användaren bara är i en grupp) eller antalet grupper som användaren tillhör.

## Lägga till en användare i en grupp med anropet Lägg till användartagg {#section_kn3_gbw_xz}

Skicka användarens LFToken och ditt valda taggnamn i med POST-begäran

Exempel:

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


Mer information finns i API-referens > [Lägg till användartagg](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post).

## Lägga till en användare i en grupp med Ping for Pull {#section_kyj_11w_xz}

Använd taggarrayen för att tilldela användare till användargrupper. (Taggar kan innehålla 1-63 alfanumeriska tecken och understreck.)

Exempel:

```
"tags": ["moderator", "brand_advocate"],
```

## Lägga till en användare i en grupp med hjälp av fjärrprofiler {#section_uyn_scv_xz}

Lägg till användartaggar i fjärrprofilen, som används för att synkronisera användardata mellan ditt anpassade profilsystem och Livefyre, för specifika användare.
