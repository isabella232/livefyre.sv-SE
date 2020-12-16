---
description: Versionsinformation för februari 23, 2017.
seo-description: Versionsinformation för februari 23, 2017.
seo-title: 23 februari 2017
title: 23 februari 2017
uuid: 9b08acf4-15e9-43b7-8abc-c0d720b156e6
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '475'
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
| Förbättring | Sök och strömmar | Lagt till möjlighet att söka efter Instagram Places (incheckningsprogram) i Library Instagram Search och Instagram Stream Rules. |
| Fel | Inställningar | Ett fel som gjorde att Twitter-konton inte kunde sparas har korrigerats. |
| Fel | Social sökning | Korrigerade ett fel som gjorde att alternativet &quot;Koppla explicita bilder&quot; inte fungerade korrekt. |
| Förbättring | Storify 2 | Förbättrad Storify 2 som stöd för att öppna modala länkar (tidigare rullade programmet till postplatsen på sidan). I Storify 2’s Designer har vi lagt till en konfiguration för att växla mellan Scroll och Modal Peralink. Modalt beteende för permanent länk är standardbeteende. |
| Förbättring | Storify 2 | Förbättrade integreringen mellan Storify 2 och Google AMP för att skapa en mindre CSS-fil. |
| Förbättring | Strömmar | Korrigerade ett fel med Facebook-regler som gjorde att innehåll hämtades in med ofullständiga metadata. |
| Fel | Strömmar | Förbättrat innehåll (bilder och videoklipp) från regler för e-postström som ska vara tillgängligt via HTTPS. |
| Fel | Strömmar | En etikett har lagts till för värdet för Mjuk radie i kartor i Twitter-flödesregler. |
| Fel | Strömmar | Korrigerade ett fel med Facebook och Facebook Page Steam Rules för att hämta in inlägg med flera mediebilagor på rätt sätt. |
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

