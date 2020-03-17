---
description: 'null'
seo-description: 'null'
seo-title: Anpassade sidenotes-strängar
title: Anpassade sidenotes-strängar
uuid: 73745273-d3fb-4569-8910-d149fb37a7b4
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Anpassade sidenotes-strängar{#sidenotes-custom-strings}

Anpassade strängar tillämpas genom ett objekt som injiceras i Sidenotes-konstruktorn och åsidosätter standardsträngar som används i programmet. Dessa kan användas för att anpassa valfri del av språket så att det passar din stil eller dina språkspecifikationer. Strängar sammanfogas automatiskt med standardvärden.

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| Nyckel | Standard |
|---|---|
| appName | Sidenotes |
| commentModeratorTag | Mod |
| commentPendingTag | Väntande |
| commentReadMoreLink | Läs mer |
| commentReplyLink | Se {number} svar |
| commentReplyLinkSing | Se svar |
| commentvoiceCount | röster |
| commentvoiceCountSing | röst |
| editorPlaceholder | Vad tycker du? |
| editorPostBtn | Post Sidenote |
| editorPostBtnMobile | Bokför |
| editorPosting | Bokför... |
| editorReplyBtn | Posta svar |
| editorReplyTitle | Skriv svar |
| editorTitle | Skriv anteckning |
| emptyImageBlockTxt | Vad tycker du? |
| emptyTextBlockTxt | + |
| errorConnection | Oj. Du verkar inte ha någon bra koppling. |
| errorDuplicate | Vi gillar din anteckning också, men du kan inte publicera den två gånger. |
| errorGeneral | Ett fel har inträffat. Försök igen. |
| errorServer | Något gick fel med vår server. Försök igen? |
| facebookShareCaption | SideNotes på {title} |
| menuAuthSignedInMsg | Du måste vara inloggad på {action} |
| menuAuthSignInBtn | Logga in |
| menuBackBtn | Bakåt |
| menuConfirmAccept | Ja, {action} |
| menuConfirmCancel | Avbryt |
| menuConfirmTitle | Är du säker? |
| menuEtcOptionApprove | Godkänn |
| menuEtcOptionDelete | Ta bort |
| menuEtcOptionEdit | Redigera |
| menuEtcOptionFlag | Flagga |
| menuEtcOptionShare | Dela |
| menuEtcPostedAt | Anslaget den {date} |
| menuEtcTitle | Mer |
| menuFlagOptionDisagree | Avböja |
| menuFlagOptionOffensive | Stötande |
| menuFlagOptionOffTopic | Av ämne |
| menuFlagOptionSpam | Spam |
| menuFlagTitle | Flagga som... |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | Hjälp |
| menuInfoLivefyreLink | Besök Livefyre.com |
| menuRepliesViewReply | Svara på konversation |
| menuRepliesViewTitle | Detaljer |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copy Permalink |
| menuShareOptionLinkComplete | Kopierad |
| menuShareOptionLinkFailed | Kopieringen misslyckades |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | Dela |
| notificationApproved | Godkänd |
| notificationDeleted | Borttagen |
| notificationFlagged | Flaggad |
| permanentLinkBackBtn | Alla |
| allowLinkTitle | Permalink |
| questionFörklaring | Nu kan du läsa och skriva kommentarer direkt på meningar, stycken, bilder och citat.<br><br>Markera text och klicka på ikonen&quot;fycon-write&quot; eller klicka på ikonen&quot;fycon-action-view&quot; i slutet av varje stycke. |
| questionMockText | Det som är &quot;välkänt&quot; är inte riktigt känt, bara för att det är &quot;välbekant&quot;. |
| questionTitle | Vad är en Sidenote? |
| queuedCommentsPlural | {number} Nya sidobjekt |
| queuedCommentsSingular | 1 ny sidenote |
| queuedRepliesPlural | {number} nya svar |
| queuedRepliesSingular | 1 nytt svar |
| replyBtn | Svara |
| signInToPost | Logga in för att skriva ett sidomeddelande |
| sliderCommentTally | av |
| sliderInviteRead | Läs |
| sliderInviteWrite | Skriv |
| sliderWriteText | Vad tycker du? Tryck för att skriva |
| threadCollapseBtn | Komprimera |
| threadExpandBtnPlural | Expandera {number} svar |
| threadExpandBtnSingular | Expandera 1 svar |
| threadReplyBtn | Svara på konversation |
