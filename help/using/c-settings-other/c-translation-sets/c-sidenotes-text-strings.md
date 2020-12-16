---
description: Anpassa textsträngar för Livefyre Sidenotes
seo-description: Anpassa textsträngar för Livefyre Sidenotes
seo-title: Textsträngar för sidenotes
solution: Experience Manager
title: Textsträngar för sidenotes
uuid: a3735237-e55d-4bc0-b88d-8a323980ee09
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---


# Sidenotes Text Strings{#sidenotes-text-strings}

Anpassa textsträngar för Livefyre Sidenotes

På den här sidan listas och beskrivs alla strängar som är tillgängliga för anpassning i appar för sidoteckensnitt. Mer information om tillgängliga strängar för de viktigaste Livefyre-apparna finns i String Customizations.

Implementering
Autentisering
Direktuppspelningsinformation
Författare/Innehållsinformation
Användaråtgärder
Bokför funktioner
Moderatorgränssnitt
Fel

## Implementering {#section_wp2_ql4_xz}

Om du vill implementera den här funktionen skickar du en 1-1-objektmappning av strängarna som du vill åsidosätta till Javascript-konfigurationsobjektet. Om du inte anger något fält används standardtexten.

Exempel:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## Autentisering {#section_pqf_3l4_xz}

Strängar som är tillgängliga för autentiseringsprocessen och från de autentiserade användarmenyerna.

| Element | Nyckel | Standardtext |
|---|---|---|
| Autentiseringsmenysträngar | menuAuthSignInBtn | Logga in |
|  | menuAuthSignedInMsg | Du måste vara inloggad på {action} |
|  | menuUserEditProfile | Redigera profil |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | Logga ut |
|  | menuUserBackBtn | Alla |

## Direktuppspelningsinformation {#section_wpy_gl4_xz}

Strängar som är tillgängliga för information och visning av innehållsströmmar.

| Element | Nyckel | Standardtext |
|---|---|---|
| Alternativ på menyn Info | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | Hjälp |
|  | menuInfoLivefyreLink | Besök Livefyre.com |

## Författare/Innehållsinformation {#section_dhb_gl4_xz}

Inställningar som är tillgängliga för information om författare och individuellt innehåll.

| Element | Nyckel | Standardtext |
|---|---|---|
|  | commentModeratorTag | Mod |
|  | commentPendingTag | Väntande |
|  | commentReadMoreLink | Läs mer |
|  | commentReplyLink | Se {number} svar |
|  | commentReplyLinkSing | Se svar |
|  | commentvoiceCount | röster |
|  | commentvoiceCountSing | röst |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | En array. Standard =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionFörklaring | Nu kan du läsa och skriva kommentarer direkt på meningar, stycken, bilder och citat.<br><br><span class="&rdquo;lf-highlight-text&rdquo;">Markera </span> texten och klicka på  <span class="&rdquo;fycon-write&rdquo;"></span> ikonen eller klicka på  <span class="&rdquo;fycon-action-view&rdquo;"></span> ikonen i slutet av varje stycke. |
|  | questionMockText | Det som är &quot;välkänt&quot; är inte riktigt känt, bara för att det är &quot;välbekant&quot;. |
|  | questionTitle | Vad är en Sidenote? |

## Användaråtgärder {#section_qxd_fl4_xz}

Strängar som är tillgängliga för användaråtgärder: flagga, dela och gilla befintligt innehåll.

| Element | Nyckel | Standardtext |
|---|---|---|
| Alternativ på menyn Svara | menuRepliesViewTitle | Detaljer |
|  | menuRepliesViewReply | Svara på konversation |
| Alternativ på menyn Dela | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | Dela |
| Alternativ på menyn Flagga | menuFlagOptionDisagree | Avböja |
|  | menuFlagOptionOffensive | Stötande |
|  | menuFlagOptionOffTopic | Av ämne |
|  | menuFlagOptionSpam | Spam |
|  | menuFlagTitle | Flagga som... |
|  | facebookShareCaption | Sidenotes on {title} |
| Mobila användaralternativ | sliderCommentTally | av |
|  | sliderInviteRead | Läs |
|  | sliderInviteWrite | Skriv |
|  | sliderLoading | Läser in... |
|  | sliderWriteText | Vad tycker du? Tryck för att skriva. |

## Bokför funktioner {#section_xzf_2l4_xz}

Strängar som är tillgängliga för användare som publicerar innehåll.

| Element | Nyckel | Standardtext |
|---|---|---|
|  | editorEditBtn | Spara |
|  | editorEditPosting | Sparar... |
|  | editorEditReplyTitle | Redigera svar |
|  | editorEditTitle | Redigera sidotext |
|  | editorPlaceholder | Vad tycker du? |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBtnMobile | Bokför |
|  | editorPosting | Bokför... |
|  | editorReplyBtn | Posta svar |
|  | editorReplyTitle | Skriv svar |
|  | editorTitle | Skriv sidenote |
|  | emptyImageBlockTxt | Vad tycker du? |
|  | emptyTextBlockTxt | + |
|  | replyBtn | Svara |
|  | threadReplyBtn | Svara på konversation |
| Ta bort menyalternativ | menuConfirmAccept | Ja, {action} |
|  | menuConfirmCancel | Avbryt |
|  | menuConfirmTitle | Är du säker? |
| Alternativ på ETT-menyn | menuEtcOptionApprove | Godkänn |
|  | menuEtcOptionDelete | Ta bort |
|  | menuEtcOptionEdit | Redigera |
|  | menuEtcOptionFlag | Flagga |
|  | menuEtcOptionShare | Dela |
|  | menuEtcPostedAt | Anslaget den {date} |
|  | menuEtcTitle | Mer |

## Moderatorgränssnitt {#section_o5f_dl4_xz}

Strängar som är tillgängliga för det användarautentiserade moderatorgränssnittet.

| Element | Nyckel | Standardtext |
|---|---|---|
| Bekräftelsemeddelanden från menyn Mer | notificationApproved | Godkänd |
|  | notificationDeleted | Borttagen |
|  | notificationFlagged | Flaggad |

## Fel {#section_gtk_cl4_xz}

Strängar som är tillgängliga för allmänna felmeddelanden.

| Element | Nyckel | Standardtext |
|---|---|---|
|  | errorConnection | Oj. Du verkar inte ha någon bra koppling. |
|  | errorDuplicate | Vi gillar din anteckning också, men du kan inte publicera den två gånger. |
|  | errorGeneral | Ett fel har inträffat. Försök igen. |
|  | errorServer | Något gick fel med vår server. Försök igen? |

