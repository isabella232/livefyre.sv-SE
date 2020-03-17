---
description: 'null'
seo-description: 'null'
seo-title: E-post för Livefyre-identitet
solution: Experience Manager
title: E-post för Livefyre-identitet
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# E-post för Livefyre-identitet{#emails-for-livefyre-identity}

Livefyre Identity skickar följande e-postmeddelanden:

* [E-post för återställning av lösenord](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [Verifierings-e-post](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [Skicka e-postverifiering för användare](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [Välkomstmeddelande](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [Skicka välkomstmeddelande till användare](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

Du kan anpassa utseendet och känslan för alla e-postmeddelanden med Livefyre Identity i **[!UICONTROL Integration Settings > Email Notifications.]**

## E-post för återställning av lösenord {#section_nd1_whs_p1b}

Livefyre skickar automatiskt ett e-postmeddelande om lösenordsåterställning när en användare försöker återställa sitt lösenord.

E-postmeddelandet för återställning av lösenord ser ut så här:

**Ämne:** Återställ lösenord

**Brödtext:**

Hej där *&lt;användarnamn>*,

En begäran om att ändra lösenordet för din profil gjordes på *&lt;nätverksnamn>*.

Om du har begärt detta klickar du på följande länk för att välja ett nytt lösenord: *&lt;password reset URL>*.

*&lt;Användarnamn>*, *&lt;nätverksnamn>* och *&lt;URL för återställning av lösenord>* genereras dynamiskt baserat på besökaren och nätverket.

## Verifierings-e-post {#section_ak5_xhs_p1b}

Du kan skicka ett e-postmeddelande som verifierar användarens e-postadress. Om du vill skicka bekräftelsemeddelanden måste du aktivera alternativet i **Integreringsinställningar > Livefyre-identitet**.

Verifieringsmeddelandet ser ut så här:

**Ämne:** E-postverifiering

**Brödtext:**

Hej *&lt;användarnamn>*,

Klicka på följande länk (eller klistra in i webbläsaren) för att verifiera ditt konto: *&lt;verifierings-URL>*.

Länken upphör att gälla om 24 timmar.

Tack!

The *&lt;customer name>* Team

*&lt;Användarnamn>*, *&lt;nätverksnamn>* och *&lt;verifierings-URL>* genereras dynamiskt baserat på besökaren och nätverket.

## Skicka en e-postverifiering till användare {#section_vyv_yhs_p1b}

Du kan skicka ett e-postmeddelande till en användare för att verifiera e-postadressen som de använder för att registrera sig för ett konto. Så här skickar du ett bekräftelsemeddelande:

1. Klicka på kugghjulsikonen i Studio för att ändra nätverksinställningarna.
1. Klicka på **Integreringsinställningar > Livefyre-identitet.**

1. Navigera till **Inloggningstyper**.
1. Klicka på **Kräv e-postverifiering** för att skicka ett e-postmeddelande till användare som verifierar e-postadressen som de använder för att registrera sig för ett konto.
1. Navigera till **Nätverks-e-post** för att konfigurera **logotypen för e-post**, e-postadressen som ska användas som avsändaradress (**E-post från**) och visningsnamnet som ska användas för formuläret från e-postadressen (**e-postvisningsnamn**).

## Välkomstmeddelande {#section_z2v_zhs_p1b}

Du kan skicka ett välkomstmeddelande till användarna. Om du vill skicka välkomstmeddelanden måste du aktivera alternativet i **Integreringsinställningar** > **Livefyre-identitet**.

Välkomstmeddelandet ser ut så här:

**Ämne:** Välkommen till *&lt;kundnamn>*

**Brödtext:**

Hej *&lt;användarnamn>*,

Ett konto skapades för dig på *&lt;kundnamn>*.

Det här kontot skapades på *&lt;hänvisnings-URL>* från IP-adressen *&lt;IP-adress>*.

Om du gjorde detta kan du ignorera det här e-postmeddelandet.

Om du inte gjorde det här kan du kontakta `support@livefyre.com`

Tack

The *&quot;customer name&quot;* Team

*&quot;Användarnamn&quot;, &quot;kundnamn&quot;,* &quot;hänvisnings-URL&quot; och &quot;IP-adress&quot; genereras dynamiskt baserat på besökaren och nätverket.

## Skicka ett välkomstmeddelande till en användare {#section_kjp_c3s_p1b}

Du kan skicka ett välkomstmeddelande till en användare när de har registrerat sig för ett konto. Studio skickar det här e-postmeddelandet när det har skickats ett bekräftelsemeddelande om du skapar ett bekräftelsemeddelande. Så här skickar du ett välkomstmeddelande:

1. Klicka på kugghjulsikonen i Studio för att ändra nätverksinställningarna.
1. Klicka på **[!UICONTROL Integration Settings > Livefyre Identity]**

1. Navigera till **[!UICONTROL Email Settings]**.

1. Klicka **[!UICONTROL Send Welcome Emails To New Users]** för att aktivera sändning av e-post.
1. Navigera till **[!UICONTROL Network Email]** för att konfigurera *logotypen för e-post*, e-postadressen som ska användas som formuläradress (**E-post från**) och visningsnamnet som ska användas för e-postadressen (**e-postvisningsnamn**).
