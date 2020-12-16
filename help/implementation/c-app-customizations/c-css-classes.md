---
description: Använd tillgängliga CSS-klasser för att anpassa hur apparna visas.
seo-description: Använd tillgängliga CSS-klasser för att anpassa hur apparna visas.
seo-title: CSS-klasser
solution: Experience Manager
title: CSS-klasser
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---


# CSS-klasser{#css-classes}

Använd tillgängliga CSS-klasser för att anpassa hur apparna visas.

Finns för chatt, kommentarer, Live-blogg, recensioner och sidobjekt.

Använd CSS för att anpassa Livefyre-apparna för en mer fullständig integrering med sidan genom att helt enkelt åsidosätta standard-CSS för app med din egen formatmall. I det här avsnittet beskrivs tillgängliga CSS-anpassningar.

* [CSS-redigerare](#c_css_classes/section_edx_prh_xz)
* [Sorteringsalternativ, CSS](#c_css_classes/section_btq_4rh_xz)
* [Kommentar-CSS](#c_css_classes/section_mlv_nrh_xz)
* [CSS för kommentarer](#c_css_classes/section_m2v_mrh_xz)
* [Arkiverade kommentarer, CSS](#c_css_classes/section_bs5_lrh_xz)
* [CSS för kommentarmeddelandefunktion](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS Classes](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## Redigerarens CSS {#section_edx_prh_xz}

Använd de här klasserna om du vill ändra gränssnittet för postredigeraren.

| Klass | Beskrivning |
|---|---|
| .fyre-comment-count | Texten som visar antalet kommentarer. |
| .fyre-login-bar | Begränsningsramen som innehåller inloggningsfältet och alternativen. |
| .fyre-live-container | Begränsningsramen runt antalet personer som lyssnar och deras avatarer. |
| .fyre-editor | Begränsningsramen runt .fyre-login-bar, .fyre-live-container och textområdet där användarna skriver sina kommentarer. |
| .fyre-stream-sort | Begränsningsramen runt sorteringsalternativen. |

Du kan också redigera format i själva appkonfigurationen, inklusive bakgrundsfärgen i redigeringsfältet och teckensnittsfärgen, storleken och familjen för texten som visas i redigeraren.

Om du vill anpassa kommentarredigeraren lägger du till objektet editorCss:{} till fyre.conv.load() och inkluderar den formatering du vill använda. Så här uppdaterar du till exempel redigeraren med din anpassade CSS:

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## Sorteringsalternativ, CSS {#section_btq_4rh_xz}

| Klass | Beskrivning |
|---|---|
| .fyre-stream-sort | Hela div för sorteringsalternativ. |
| .fyre-stream-sort-newest | Alternativet &quot;Nyast&quot;. |
| .fyre-stream-sort-oldest | Alternativet Äldst. |
| .fyre-stream-sort-bar | Avgränsarfältet mellan alternativen. |
| .fyre-stream-sort-selected | Det valda sorteringsalternativet. |

HTML-struktur:

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

Dölj&quot;|&quot; som skiljer sorteringsalternativen åt.

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## Kommentar-CSS {#section_mlv_nrh_xz}

| Klass | Beskrivning |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre skapar en CSS-klass i det här formatet för varje användartagg som läggs till via Livefyres Studio, [profilsynkronisering](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md). Den här klassen kan användas för att formatera bakgrunden för allt innehåll som publiceras av användarkonton, inklusive den taggen. |
| .fyre-tag-content-icon- *`tag name`* | Livefyre skapar en CSS-klass i det här formatet för varje innehållstagg som läggs till via Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md). Den här klassen kan användas för att formatera innehåll som du har lagt till taggen i. |
| .fyre-comment-user | Begränsningsramen som innehåller användarprofilbilden. |
| .fyre-comment-username | Användarnamnet. |
| .fyre-moderator | Begränsningsramen för moderatorn. |
| .fyre-comment | Markeringsram runt kommentarstexten/länken. |
| .fyre-comment-article | Begränsningsramen för hela kommentarinnehållet. |
| .fyre-comment-date | Taggen som är kopplad till elementet&quot;time since published&quot;. |
| .fyre-comment-media | Begränsningsramen runt medieinnehållet. |
| .fyre-comment-actions | Begränsningsramen runt de tillgängliga åtgärderna som kan utföras på en kommentar. |
| .fyre-comment-like | Begränsningsramen runt länken Gilla. |
| .fyre-comment-reply | Begränsningsramen runt länken Svara. |

## Aktuella kommentarer, CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>Alla CSS-klasser för kommentarer kan också användas för Aktuellt innehåll.

| Klass | Beskrivning |
|---|---|
| .fyre-featured-content-wrapper | Behållar-div för läsaren. |
| .fyre-featured-header | Det inledande namnfältet. |
| .fyre-featured-header-icon | Rubrikens tystlåtna ikon. |
| .fyre-featured-title | Rubriktexten. |
| .fyre-featured-body | Behållar-div för aktuellt innehåll i läsaren. |
| .fyre-featured-quote | Citattecknet som börjar med varje innehållsobjekt. |

## Arkiverade kommentarer, CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>Alla CSS-klasser för innehåll kan också tillämpas på arkiverat innehåll.

| Klass | Beskrivning |
|---|---|
| .fyre-archive-stream-title | Texten&quot;Från arkivet&quot;. |
| .fyre-archive-stream-title-icon | The logo for the &quot;From the Archive&quot; header. |

## Kommentarsmeddelandets CSS {#section_dy4_krh_xz}

Med dessa klasser kan du anpassa Livefyre Comment Notifier.

| Klass | Beskrivning |
|---|---|
| .fyre-notification | Div för listobjektet (både nytt innehåll och arkiverat innehåll). |
| .fyre-notifier | The wrapper for the contents of the Notifier. |
| .fyre-notifier-archive | Inkapslingen för allt nytt innehåll förutom det senaste inlägget. |
| .fyre-notifier-avatar | Bilden på avataren. |
| .fyre-notifier-avatar-container | Behållar-div för användarens avatar. Gör att du kan definiera placering. |
| .fyre-notifier-avatar-shading | Skuggan för avataren div. |
| .fyre-notifier-banner | Behållaren för meddelandets förhandsgranskningsinnehåll, som visar användarens avatar och ett innehållskuvert för det senast publicerade objektet. |
| .fyre-notifier-base | Behållaren för informationsdelen i Notifier, som visar antalet nya kommentarer, Notifier-beskrivningen och stängningsknappen. |
| .fyre-notifier-base-close | Behållar-div för stängningsknappen (x) för Notifier. |
| .fyre-notifier-base-shadow | Skuggningen för Notifier-basen. |
| .fyre-notifier-caption | Den text som visas för anmälaren. &quot;Nya kommentarer&quot; som standard. |
| .fyre-notifier-close | En knapp som stänger anmälaren. |
| .fyre-notifier-container | Behållaren för Notifier innehåller både banderollen och basen. |
| .fyre-notifier-counter | Behållaren för numret som anges i Notifier. |
| .fyre-notifier-list | Behållaren för det senaste innehållet. |
| .fyre-notifier-message | De första ~30 tecknen i innehållet som visas. |
| .fyre-notifier-message-container | Behållar-div för rubrikmeddelandet. |
