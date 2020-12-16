---
description: 'null'
seo-description: 'null'
seo-title: SSL-tvång
solution: Experience Manager
title: SSL-tvång
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---


# SSL-tvång{#ssl-enforcement}

För att dina data ska förbli säkra har vi ersatt HTTP till förmån för HTTPS. Adobe Livefyre kommer att inaktivera alla HTTP- och osäkra SSL-/TLS-ciphers helt i slutet av augusti 2018. Det här är en Adobe-standard som är utformad för att skydda din och dina användares integritet.

## Vem påverkas? {#section_jf2_4yz_kcb}

Detta kan påverka Livefyre-kunder som har:

* Server-till-server-anrop från CRM, CMS, WordPress eller annan klient.
* Mobilintegreringar (Android- och iOS-appar)
* Anpassade program eller anpassad kod

## Vad behöver jag göra? {#section_unv_dc5_kcb}

1. Alla Livefyre-kunder måste kommunicera med alla API:er via HTTPS för all trafik, inklusive:

   * Server-till-server-integreringar (CRM, CMS, WordPress osv.)
   * Mobilintegreringar (Android- och iOS-appar)
   * Anpassade program (Streamhub SDK eller direkt kodad).

1. Server till server och Mobile HTTP-klienter måste ha stöd för TLS 1.2
1. Ändra värdnamn från `{*}.<network>.fyre.co` till `<network>.{*}.fyre.co`. Värdnamnet `example.network.fyre.co` ändras till `network.`example.fyre.co&quot;. Exempel:

   * `bootstrap.<network_name>.fyre.co` till  `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` till  `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` till  `<network_name>.admin.fyre.co`

## Hur vet jag om jag har gjort ändringarna? {#section_sqk_5d5_kcb}

Du kan redan använda HTTPS, men Livefyre rekommenderar att du dubbelkontrollerar, särskilt om du har:

* Server-till-server-samtal från CMS eller CRM.
* Anpassad kod eller använd SDK:er för anpassade appar i Javascript eller Mobile.
* Om integreringen är mer än ett år gammal.
* Om tekniken i din hög är äldre än ett år.

Även om du redan använder HTTPS måste du verifiera att dina API-klienter stöder TLS 1.2.

## Hur kan jag verifiera att mina API-klienter stöder TLS 1.2? {#section_nd1_j25_kcb}

En person som arbetar med utvecklingen av din webbplats kan:

* Identifiera klientprogramvaran.
* Identifiera versionen.
* Läs dokumentationen för att kontrollera att API-klienten stöder TLS 1.2.
* Aktivera felsökningsläget om det behövs.

## Java-stöd för TLS 1.2 {#section_lwn_rwk_ycb}

Oracle och OpenJDK JVM för Java 8 och senare konfigureras att använda TLS 1.2 som standard för alla SSL-anslutningar. Du behöver inte vidta några ytterligare åtgärder om du använder Java 8 eller senare.

Användare som har Java 7 eller tidigare bör läsa den offentliga dokumentationen om hur man aktiverar TLS 1.2.

## Varför måste jag ändra mina värdnamn? {#section_d5q_p25_kcb}

Livefyre har inga SSL-certifikat på `{*}.<network>.fyre.co`-domäner. Om du ändrar URL:en till HTTPS bryts programmet.

## Måste jag uppgradera till den senaste versionen av Livefyre SDK:er? {#section_dw5_s25_kcb}

Nej. Du kan korrigera koden i stället. Om du vill korrigera koden ändrar du några statiska strängar och återskapar koden. Om din HTTP-klient är inaktuell måste du uppgradera den också eller använda en annan.

## Hur lång tid tar det här? {#section_lgd_v25_kcb}

Hur lång tid det tar beror på inställningarna. Om ni har en enkel implementering bör det ta lite tid att bekräfta. Om du har många anpassningar måste du testa och distribuera uppdaterad kod till dina servrar eller nya appar till App Stores. För bästa resultat rekommenderar vi att du gör en inledande granskning av arbetet så att du kan planera för ett längre arbete.

## Vilken är tidslinjen för det här arbetet? {#section_kgk_w25_kcb}

Livefyre inaktiverar port 80 (HTTP) till våra tjänster före augusti 2018 och stöder endast anslutningar till 443 (HTTPS). Webbläsare och andra klienter som försöker använda HTTP kommer att misslyckas.

## När behöver jag göra klart det här arbetet? {#section_rvb_x25_kcb}

Alla kunder måste använda HTTPS före slutet av juli 2018. Om du inte kan hålla deadline kontaktar du vårt team på prioritysupport@livefyre.com.
