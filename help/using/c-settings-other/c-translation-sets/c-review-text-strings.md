---
description: Anpassa textsträngarna för Livefyre-recensioner.
title: Granska textsträngar
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Granska textsträngar{#review-text-strings}

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

## Gransknings-/klassificeringsgränssnitt {#section_iyv_zj4_xz}

Strängar som är tillgängliga för användargränssnittet Granska och Klassificera.

| Element | Nyckel | Standardtext |
|--- |--- |--- |
| Knappar | editReviewBtn | Redigera granskning |
|  | reviewBtn | [Skriv recension](https://d.pr/i/QscA) |
|  | granskningarStängda | [Granskningar stängda](https://d.pr/i/zr7M) |
|  | showReviewBtn | [Visa granskning](https://d.pr/i/onxU) |
|  | följ | Jag är intresserad |
|  | shareText | Jag skrev just en recension. Kolla in den! |
| Tips för klassificeringsverktyg | ratingValues | En array. Standard = `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`; <br>Obs! Värdena i arrayen måste dupliceras för att tilldela både den vänstra och den högra halvan av varje stjärna samma namn. |
| Klassificera underdelar | ratingSubpartPlaceholder | En array. Standard = `[]` |
|  | ratingSubpartTitles | En array. Standard = `[]` |
|  | reviewStreamTitle | Tom som standard. Titel på sammanfattningsavsnittet i granskningen. |
| Diverse | AverageRating | [Genomsnittlig användarklassificering](https://d.pr/i/QscA) |
|  | breakHeader | [Värderingsfördelning](https://d.pr/i/QscA) |
|  | hjälpsam | %s av %s hittade användbar |
|  | hjälpsamPlural | %s av %s hittade användbar |
|  | outOf | / |
|  | ratingType | stjärna |

## Direktuppspelningsinformation {#section_wmv_yj4_xz}

Strängar som är tillgängliga för information och visning av innehållsströmmar.

| Element | Nyckel | Standardtext |
|---|---|---|
| Sortering | sortBy | Tom som standard. |
|  | sortHighestRated | [Högsta omdöme](https://d.pr/i/huTd) |
|  | sortLowestRated | [Lägsta omdöme](https://d.pr/i/huTd) |
|  | sortMostHelpful | [Mest användbara](https://d.pr/i/huTd) |
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
| Trådbrytning | reviewsInnehållHittadeMsg | [Den här granskningen visas inte längre](https://d.pr/i/svXs) |
|  | backToComments | Tillbaka till Recensioner |

## Användaråtgärder {#section_tlx_wj4_xz}

Strängar som är tillgängliga för användaråtgärder: flagga, dela och markera befintligt innehåll som användbart.

| Element | Nyckel | Standardtext |
|---|---|---|
| Kommentarsidfot | wasReviewHelpful | [En bra hjälp?](https://d.pr/i/Q0mA) |
|  | wasReviewHelpfulMobile | En bra hjälp? |
|  | ownwasReviewHelpful | [Hjälpte.](https://d.pr/i/Q0mA) |
|  | reviewwasHelpful | [Ja](https://d.pr/i/Q0mA) |
|  | hjälpsamDelare | [&amp;Invertera;](https://d.pr/i/Q0mA) |
|  | reviewwasNotHelpful | [Nej](https://d.pr/i/Q0mA) |
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
