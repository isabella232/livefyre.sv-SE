---
description: Med översättningsuppsättningar kan du ange ett annat språk för appar.
title: Översättningsuppsättningar
exl-id: 1de99602-b97e-42e9-8450-39abd4ba2f9b
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 0%

---

# Översättningsuppsättningar{#translation-sets}

Med översättningsuppsättningar kan du ange ett annat språk för appar.

Använd översättningsinställningar för att lokalisera appar på olika språk eller för att ange alternativ text för flera appar från en plats i Studio. Du kan till exempel se till att alla spanska webbplatser använder spanska för alla programfält. Du kan också ändra texten så att alla fält matchar rösten och känslan på platsen eller nätverket.

Du kan ange översättningsinställningar för alla program, förutom Storify 2. Mer information om vilka fält du kan lokalisera finns i [Lokalisera strängar](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md#c-localize-strings).

Kommentarer, Live-blogg och Chatt delar samma uppsättning strängar i en översättningsuppsättning.

Ange en översättningsuppsättning för ett nätverk, en webbplats, en app eller med ett API.

Översättningsuppsättningarna på olika nivåer åsidosätter varandra enligt det här mönstret:

API-översättningsuppsättningen åsidosätter alla översättningsuppsättningar på alla nivåer (app, nätverk och webbplats)
Programöversättningsuppsättningen åsidosätter översättningsuppsättningar på nätverksnivå och på webbplatsnivå.
Översättningsuppsättningar på platsnivå åsidosätter översättningsuppsättningar på nätverksnivå.

## Granska textsträngar {#c_review_text_strings}

Anpassa textsträngarna för Livefyre-recensioner.

På den här sidan visas och beskrivs de strängar som är tillgängliga för anpassning i granskningsappar. Strängarna som listas här är utöver och åsidosätter standardsträngarna för kärnapparna Livefyre, som listas i String Customizations. I de fall dubbletter visas är strängarna i de här tabellerna standard för granskningsappar.

Implementering
Gransknings-/värderingsgränssnitt
Direktuppspelningsinformation
Författare/Innehållsinformation
Användaråtgärder
Bokför funktioner
Fel

## Implementering {#section-vsy-1k4-xz}

Om du vill implementera den här funktionen skickar du en 1-1-objektmappning av strängarna som du vill åsidosätta till Javascript-konfigurationsobjektet. Om du inte anger något fält används standardtexten.

Exempel:

```
var customStrings = {
   postAsButton: "New Post As Text",
   postEditButton: "New Post Edit Text" };
networkConfig["strings"] = customStrings; fyre.conv.load(
   networkConfig,
   [convConfig],
   function(){}
);
```

## Gransknings-/värderingsgränssnitt {#section_iyv_zj4_xz}

Strängar som är tillgängliga för användargränssnittet Granska och Klassificera.

| Element | Nyckel | Standardtext |
|--- |--- |--- |
| Knappar | editReviewBtn | Redigera granskning |
|  | reviewBtn | Skriv recension |
|  | granskningarStängda | Granskningar stängda |
|  | showReviewBtn | Visa granskning |
|  | följ | Jag är intresserad |
|  | shareText | Jag skrev just en recension. Kolla in den! |
| Tips för klassificeringsverktyg | ratingValues | En array. Standard = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Obs! Värdena i arrayen måste dupliceras för att tilldela både den vänstra och den högra halvan av varje stjärna samma namn. |
| Klassificera underdelar | ratingSubpartPlaceholder | En array. Standard = [] |
|  | ratingSubpartTitles | En array. Standard = [] |
|  | reviewStreamTitle | Tom som standard. Titel på sammanfattningsavsnittet i granskningen. |
| Diverse | AverageRating | Genomsnittlig användarklassificering |
|  | breakHeader | Värderingsfördelning |
|  | hjälpsam | %s av %s hittade användbar |
|  | hjälpsamPlural | %s av %s hittade användbar |
|  | outOf | / |
|  | ratingType | stjärna |

## Direktuppspelningsinformation {#section_wmv_yj4_xz}

Strängar som är tillgängliga för information och visning av innehållsströmmar.

| Element | Nyckel | Standardtext |
|---|---|---|
| Sortering | sortBy | *Tom som standard.* |
|  | sortHighestRated | Högsta omdöme |
|  | sortLowestRated | Lägsta omdöme |
|  | sortMostHelpful | Mest användbara |
| Strömfel. | showMore | Visa fler |
| Strömma hög hastighet | newComment | Ny granskning |
|  | newComments | Nya granskningar |
| Lyssnarantal | listenerCount | personavlyssning |
|  | listenerCountPlural | personer som lyssnar |
| Antal kommentarer | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| Antal kommentarsaviserare | commentNotifier | Ny granskning |
|  | commentNotifierPlural | Nya granskningar |

## Författare/Innehållsinformation {#section_osx_xj4_xz}

Inställningar som är tillgängliga för information om författare och individuellt innehåll.

| Element | Nyckel | Standardtext |
|---|---|---|
| Trådbrytning | reviewsInnehållHittadeMsg | Den här granskningen visas inte längre |
|  | backToComments | Tillbaka till Recensioner |

## Användaråtgärder {#section_tlx_wj4_xz}

Strängar som är tillgängliga för användaråtgärder: flagga, dela och markera befintligt innehåll som användbart.

| Element | Nyckel | Standardtext |
|---|---|---|
| Kommentarsidfot | wasReviewHelpful | En bra hjälp? |
|  | wasReviewHelpfulMobile | En bra hjälp? |
|  | ownwasReviewHelpful | Hjälpte. |
|  | reviewwasHelpful | Ja |
|  | hjälpsamDelare | &amp;vert; |
|  | reviewwasNotHelpful | Nej |
| Rösta modalt | voiceTitle | Hjälpte den här recensionen? |
|  | röstaNedröst | Nej |
|  | voiceReplyTitle | Hjälpte svaret? |
|  | voiceTitle | Hjälpte kommentaren? |
|  | voiceUpvoice | Ja |
| Flagga modal | flagTitle | Flagga %s granskning |
|  | flagSuccessMsg | Granskningen har flaggats. |
| Flag Mobile | flagConfirmationMessage | Flagga %s som %s? |
| Ange modal | mentionDefaultText | Jag nämnde dig i en Livefyre-recension! |
| Dela modalt | shareTitle | Dela granskning |

## Bokför funktioner {#section_yl1_wj4_xz}

Strängar som är tillgängliga för användare som publicerar recensioner.

| Element | Nyckel | Standardtext |
|---|---|---|
| Redigerare | bodyPlaceholder | Skriv granskning... |
|  | postEditButton | Redigera |
|  | postEditCancelButton | Avbryt |
|  | postAsButton | Eftergranska som... |
|  | postButton | Eftergranskning |
|  | postSvaraSomKnapp | Bokför som... |
|  | postReplyButton | Bokför |
|  | shareButton | Dela |
|  | titlePlaceholder | Titel... |

## Fel {#section_jbc_vj4_xz}

Strängar som är tillgängliga för allmänna felmeddelanden.

| Element | Nyckel | Standardtext |
|---|---|---|
| Fel | errorAlreadyPosted | Du kan bara publicera en granskning. |
|  | errorAuthError | Du har inte behörighet att publicera en granskning på den här konversationen |
|  | errorCommentsNotAllowed | Det går inte att bokföra granskningar just nu |
|  | errorDislikeOwnComment | Du kan inte ogilla din egen granskning |
|  | errorDuplicate | Så mycket du tyckte om din recension får du inte publicera den två gånger. |
|  | errorEditDuplicate | Du måste ändra texten i granskningen när du redigerar den. |
|  | errorEditNotAllowed | Du får inte redigera granskningar för den här konversationen. |
|  | errorEditTimeExceeded | Din granskningsperiod har gått ut. |
|  | errorEmpty | Det verkar som att du försöker publicera en tom granskning. |
|  | errorEmptyTitle | Det verkar som att du försöker publicera en tom titel |
|  | errorFieldRating | stjärnklassificering |
|  | errorFieldReview | recension |
|  | errorFieldTitle | title |
|  | errorMaxChars | Din granskning är för lång. Redigera och försök igen. |
|  | errorMissingFields | Ange |
|  | errorRatingEmpty | Du kan inte skicka en tom klassificering |
|  | errorRatingNotSet | Alla klassificeringar måste anges |
|  | errorRatingNotValid | Klassificeringen måste vara ett objekt |
|  | errorShowMore | Ett fel uppstod när fler granskningar lästes in. |
|  | errorTitleMaxChars | Din titel är för lång. Redigera och försök igen. |
|  | errorvoiceOwnComment | Du kan inte rösta på din egen recension |

## Textsträngar för sidenotes {#c_sidenotes_text_strings}

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
|  | datetimeMonths | En array. Standard =[&quot;januari&quot;,&quot;februari&quot;,&quot;mars&quot;,&quot;april&quot;,&quot;maj&quot;,&quot;juni&quot;,&quot;juli&quot;,&quot;augusti&quot;,&quot;september&quot;,&quot;oktober&quot;,&quot;november&quot;,&quot;december&quot; ] |
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
