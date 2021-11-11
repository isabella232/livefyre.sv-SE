---
description: Hantera innehåll i Livefyre-nätverket.
title: Fliken Appinnehåll
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
source-git-commit: 600c9712366f5de303de27cf39045beccd4145eb
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Fliken Appinnehåll{#app-content-tab}

Hantera innehåll i Livefyre-nätverket.

På fliken Appinnehåll i biblioteket kan du söka efter och moderera innehåll som publicerats i olika appar. The **[!UICONTROL App Content]** Med -fliken kan du använda flera sökfilter med jokertecken för att snabbare och enklare definiera sökparametrar.

Använd fliken Appinnehåll för att:

* Sök efter innehåll
* Visa innehållshistorik
* Modernt innehåll
* Lägg till en tagg
* Innehåll
* Associera innehåll med produkter från produktkatalogen

Mer information om hur du modererar innehåll med fliken Appinnehåll finns i [Moderera innehåll med fliken App Content](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## Sökning med jokertecken {#section_jvr_ntm_zz}

Livefyre-sökfält har stöd för jokertecken, som gör att du kan lägga till en asterisk ( * ) till ord (eller ordfragment) för att fånga partiella matchningar.

Exempel:

* ball returnerar bara ball
* ball* returnerar boll och ballong
* *ball returns ball and ball
* *ball* returnerar ball och uniball samt snöballad

## Sök efter innehåll {#section_fw1_mtm_zz}

På panelen Appinnehåll kan du begränsa sökningen med hjälp av flera olika alternativ för innehållsfiltrering.

![](assets/PublishedState-1024x367.png)

Använd **[!UICONTROL Quick Filters]** pulldown to nardown returned content to **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]**, eller **[!UICONTROL Rights Requests]** status. Välj sedan en **[!UICONTROL Filter by]** och använda kryssrutorna eller inmatningsfälten för att begränsa sökningen.

Använd listrutemenyn för att sortera innehållet i listan efter **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** eller **[!UICONTROL Most liked]**.

## Filtrera efter alternativ {#section_aqn_xqm_zz}

Använd **[!UICONTROL Filter by]** fält för att filtrera efter följande alternativ:

* **Läge** Används för att filtrera efter innehållets aktuella modereringstillstånd:** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]**, eller **[!UICONTROL Bozo]**.

* **Källa** Gör att du kan filtrera efter innehållets källa. Välj **[!UICONTROL Livefyre]** för att lista användargenererat innehåll som publicerats direkt i flödet. Välj **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]**, eller **[!UICONTROL RSS]** för att inkludera innehåll som hämtas in i apparna från dessa källor.

* **Flaggor** Om du väljer flaggor kan du filtrera efter **[!UICONTROL User Flags]** (Spam, Offtopic, Offensive eller Disagree), **[!UICONTROL System Flags]** tillämpas av SAFE (Profanity, Spam eller Magically Moderated), eller **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **Datum/tid** Gör att du kan filtrera efter när innehållet ursprungligen fanns **[!UICONTROL Created]** (eller hämtas till appen via SocialSync eller en Stream), eller senast **[!UICONTROL Modified]** (redigerad, flaggad eller statusen ändrad).

* **Upphovsman** Gör att du kan filtrera efter författarens **[!UICONTROL IP]** adress, **[!UICONTROL Display Name]** (finns på panelen Användare eller ovanför det innehåll som författaren publicerat), eller **[!UICONTROL User ID]**(finns på panelen Användare).

* **Innehåller** Med det här alternativet kan du filtrera de senaste 90 dagarnas innehåll efter **[!UICONTROL Keyword]** eller **[!UICONTROL Content Tag]**. Välj **[!UICONTROL Media]** om du bara vill returnera innehåll som innehåller media. (Om du vill söka efter allt innehåll bläddrar du nedåt genom allt innehåll i listan och klickar sedan på **[!UICONTROL Search full data]**.)

   **Obs!** Det går inte att söka efter flera nyckelord och innehållstaggar. Om du anger flera nyckelord eller taggar används det sista ordet i sökningen.

   När du söker efter innehållstagg fylls de föreslagna taggarna i automatiskt när du skriver i sökfältet. Sökresultaten returnerar allt innehåll som någonsin har tilldelats taggen. (Använd det här fältet om du vill söka efter Aktuellt innehåll eller klicka på **[!UICONTROL Featured]** etikett på allt innehåll i Studio.)

   **Obs!** Använd ett minustecken (-) före ett taggnamn om du vill söka efter innehåll som inte innehåller den taggen. Till exempel: Sök efter&quot;-Miley&quot; om du vill söka efter allt innehåll som inte innehåller&quot;Miley&quot;-taggen.

* **App** Gör att du kan filtrera efter **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]**, eller **Överordnat ID**. Filtrering med överordnat ID returnerar allt innehåll som är ett svar på inmatat innehålls-ID. (Filtrera efter flera taggar genom att ange taggar avgränsade med kommatecken.)

* **Rättigheter** Gör att du kan filtrera efter status för rättighetsbegäranden:** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]**, eller **[!UICONTROL Expired]**.

## Bozo-innehåll {#section_afl_vqm_zz}

I appar **[!UICONTROL Bozo]** innehållet visas endast för den som skapat innehållet. På så sätt kan användaren tro att deras innehåll har godkänts, samtidigt som det döljs för alla andra användare och moderatorer.

>[!NOTE]
>
>Socialt innehåll som kommer från SocialSync eller Streams **[!UICONTROL cannot]** bli inställd på Bozo.

Du kan använda Bozo-innehåll av följande skäl:

* Innehåll som identifieras som spam av SAFE anges automatiskt till Bozo-läge.
* Allt innehåll från Banned Users anges automatiskt till Bozo.
* Innehåll kan vara märkt med Bozo från Studio.
* Moderatorer kan ha Bozo-innehåll direkt i strömmen.

## Visa innehållshistorik {#section_ayz_tqm_zz}

På innehållspanelen kan du granska historiken för allt innehåll i listan, inklusive förmoderering, skräppostfiltrering, publiceringsdatum och eventuella användarflaggor eller anteckningar som har tilldelats objektet.

Använd flikarna längst ned på innehållspanelen för att visa historiken.

* **[!UICONTROL More Info:]** innehåller en lista över all aktivitet i det här innehållet, inklusive överföring, redigering, skräppostkontroll, tillståndsändring och anteckningar. Livefyres innehålls-ID och användarens IP-adress visas också i det här avsnittet.
* **[!UICONTROL Replies:]** innehåller högst sex svar. Klicka **[!UICONTROL Show all replies]** för att visa alla svar på inlägget.

* **[!UICONTROL Flags & Reports:]** visar alla användarflaggor, med avataren för den användare som flaggade innehållet och alla rapporter (anteckningar som lades till av användaren när innehållet flaggas).
* **[!UICONTROL Add a note:]** gör att du kan lägga till en anteckning som är synlig för andra administratörer eller moderatorer.
* **[!UICONTROL Request Rights:]** öppnar **[!UICONTROL New Rights Request]** dialogrutan, från vilken en rättighetsbegäran kan utfärdas.

* **[!UICONTROL Save as Asset:]**öppnar **[!UICONTROL Advanced Options]** som gör att du kan spara det markerade objektet i ditt resursbibliotek, publicera det i en app eller begära återanvändningsbehörighet från författaren.

![](assets/PublishedMoreInfo-1024x462.png)

## Lägga till en tagg i innehållet {#section_xb4_mxr_rdb}

Genom att tagga innehåll kan du kategorisera och ordna innehåll för enkel hämtning och anpassning av format, eller markera innehåll som det är.

Om du vill lägga till taggar klickar du på plustecknet ( **[!UICONTROL +]**) under innehållet. Ange en ny tagg eller välj i en lista med befintliga taggar.

![](assets/PublishedAddTag-1024x338.png)

## Söka efter bilder i alla resurser {#section_zxf_hsf_wcb}

När du har lagt till innehållet i biblioteket kan du söka efter innehåll med smarta taggar.

I biblioteket under Alla resurser kan du söka efter befintliga bilder genom att klicka på **[!UICONTROL Show Filters]** och sedan:

* Ange text att söka i sökfältet
* Sortering efter relevans
* Skriva text i **[!UICONTROL Tags]** fält att söka efter med smarta taggar. Rankningsalgoritmen för smarta taggar filtrerar innehåll med hjälp av ett smart kodkonfidensresultat, hur nytt innehållet är och hur många stjärnor en användare gav innehållet.

## Innehåll {#section_emb_kqm_zz}

Välj standard **[!UICONTROL Featured]** markera innehållet som aktuellt och markera det som viktigt för användarna. När du har taggat det kan du använda anpassade formateringsalternativ för att anpassa det aktuella innehållet i dina appar.

## Till innehåll eller ta bort funktion {#section_ojx_3qm_zz}

* I Studio klickar du på **[!UICONTROL +]** signera bredvid en del av innehållet, markera **[!UICONTROL Featured]** i listrutan och klicka på **[!UICONTROL Enter]** till Innehåll. Taggen sparas och visas bredvid innehållet.

* Om du vill ta bort funktionen klickar du på **[!UICONTROL x]** på **[!UICONTROL Featured]** -tagg som visas på innehållet.

* Håll muspekaren över det innehåll du vill använda och klicka på **[!UICONTROL Feature]**. Om du vill ta bort en funktion håller du muspekaren över innehållet och klickar **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>På grund av utrymmesbegränsningar kan chattinnehåll endast visas eller inte visas med Studio, och kan inte visas inifrån själva appen.

## Redigera innehåll {#section_pyw_hqm_zz}

De flesta vanliga åtgärder för innehåll kan utföras på Aktuellt innehåll, med undantag för följande:

* Det aktuella innehållet kan inte flaggas.
* Användarna kan inte redigera sitt innehåll efter att det har funnits, men de kan fortfarande ta bort det om de vill. Moderatorer kan redigera aktuellt innehåll.
