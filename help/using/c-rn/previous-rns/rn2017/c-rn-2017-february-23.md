---
description: Versionsinformation för februari 23, 2017.
title: 23 februari 2017
exl-id: 3a5708a1-4be6-447f-ae6e-8f5a37171ed7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# 23 februari 2017{#february}

Versionsinformation för februari 23, 2017.

## Produktionsrelease

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Förbättring | Android SDK | Android SDK har ordnats om för att se till att exempel- och referensimplementeringskataloger är tydligare beroende på var de finns. |
| Förbättring | Android SDK | Android SDK har ändrats till att nu ha stöd för en SDK-version på minst 14 (ned från 16). |
| Fel | Konversationsappar | Förbättrade konversationsappar som alltid länkar ut till användarprofiler, även utan fullständig auth-integrering. |
| Fel | Mosaik | Korrigerade ett fel som nu visar alla Twitter-bilder via HTTPS. |
| Förbättring | Sök och strömmar | Lagt till möjlighet att söka på Instagram Platser (incheckningar) i Library Instagram Search och Instagram Stream Rules. |
| Fel | Inställningar | Ett fel som gjorde att Twitter Social-konton inte kunde sparas har korrigerats. |
| Fel | Social sökning | Korrigerade ett fel som gjorde att alternativet &quot;Koppla explicita bilder&quot; inte fungerade korrekt. |
| Förbättring | Storify 2 | Förbättrad Storify 2 som stöd för att öppna modala länkar (tidigare rullade programmet till postplatsen på sidan). I Storify 2’s Designer har vi lagt till en konfiguration för att växla mellan Scroll och Modal Peralink. Modalt beteende för permanent länk är standardbeteende. |
| Förbättring | Storify 2 | Förbättrade integreringen mellan Storify 2 och Google AMP för att skapa en mindre CSS-fil. |
| Förbättring | Strömmar | Korrigerade ett fel med Facebook-regler som gjorde att innehåll hämtades in med ofullständiga metadata. |
| Fel | Strömmar | Förbättrat innehåll (bilder och videoklipp) från regler för e-postström som ska vara tillgängligt via HTTPS. |
| Fel | Strömmar | En etikett har lagts till för värdet för Mjuk radie i kartor i Twitter Stream Rules. |
| Fel | Strömmar | Korrigerade ett fel med Facebook och Facebook Page Steam Rules för att hämta inlägg med flera bifogade mediefiler på rätt sätt. |
| Förbättring | Strömmar | En ny funktion har lagts till så att användare kan välja att tillämpa eller inaktivera SAFE-regler per strömregel. |
| Förbättring | Studio | Korrigerade ett fel som gjorde att innehåll inte publicerades eller sparades korrekt om det redan fanns. |
| Fel | Studio | Korrigerade ett fel som gjorde att flera &amp;:er inte lades till på webbadressen när filter användes i Studio. |
| Fel | Studio | Korrigerade ett fel som förhindrade att vissa kryssrutor i Studio-filter kunde avmarkeras. |

## UAT-release

| **Ärendetyp** | **Komponent** | **Versionsinformation** |
|---|---|---|
| Fel | Appar | Korrigerade ett fel för att visa innehåll i mediemoduler med rätt proportioner. |
| Fel | Media Wall | Korrigerade ett fel som orsakade att Medieväggar inte återges om särskilda främmande tecken inkluderades. |
| Fel | Sök | Korrigerade ett fel som gjorde att sidor lästes in felaktigt vid bläddring genom sökresultat med alternativet &quot;Bekräfta explicita bilder&quot; aktiverat. |
| Förbättring | Studio | Ökad sessionstid innan inloggningssessionerna för Studio-användare går ut. När en Studio-session upphör omdirigeras användaren till inloggningen igen. |
| Fel | Studio | Korrigerade ett fel som ibland hindrade användare från att spara Instagram-autentiseringsuppgifter. |
| Fel | Studio | Korrigerade ett fel som gjorde att &quot;Feature Tag&quot; inte kunde sparas korrekt när det tillämpades. |
