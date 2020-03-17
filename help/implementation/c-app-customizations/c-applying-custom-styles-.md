---
description: Om du vill anpassa formatinnehåll för användargrupper måste du först lägga till en användartagg i kontot och sedan formatera innehållet med CSS.
seo-description: Om du vill anpassa formatinnehåll för användargrupper måste du först lägga till en användartagg i kontot och sedan formatera innehållet med CSS.
seo-title: Använda anpassade format
solution: Experience Manager
title: Använda anpassade format
uuid: 0556aa2f-4fcd-4bde-abb5-479ec682f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Använda anpassade format{#applying-custom-styles}

Om du vill anpassa formatinnehåll för användargrupper måste du först lägga till en användartagg i kontot och sedan formatera innehållet med CSS.

För varje användartagg som läggs till via Studio eller Ping for Pull skapar Livefyre två CSS-klasser, som båda kan användas för att formatera gruppens innehåll.

När användartaggar konverteras till CSS-klasser:

* Livefyre skapar två klasser: fyre-author-tag-****&lt;your_group>*** och fyre-tag-author-***&lt;your_group>***. Båda kan användas för att formatera innehållet.

* Alla blanksteg i taggen konverteras till understreck. Till exempel: Favoritanvändare blir favorit_user.
* Unicode-tecken som ingår i gruppnamn konverteras inte och visas som Unicode i klassnamnen. Till exempel: Användargruppen&quot;modérateur&quot; blir fyre-comment-author-tag-modérateur.

När användargrupperna har skapats använder du Livefyres CSS-klasser för att använda anpassad formatering för innehållet.

## Formatera innehåll för moderatorer (och ägare) {#section_vjv_2cv_xz}

* Använd CSS-klassen .fyre-moderator.

   >[!NOTE]
   >
   >Ägare, eftersom de också är moderatorer, kommer att få den här klassen tillämpad även på sitt innehåll i strömmen.

* Skapa en CSS-regel för att visa eller formatera ett märke för gruppen:

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## Formatera innehåll för användargrupper {#section_ghn_s1v_xz}

Skapa en CSS-regel för att visa eller formatera ett märke för gruppen:

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

Använd CSS-klassens fyre-author-tag-****&lt;your_group>*** eller fyre-tag-author-***&lt;your_group>*** för att formatera teckensnittet och bakgrunden för varje objekt som bokförts från ett konto som är associerat med den valda taggen.

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

