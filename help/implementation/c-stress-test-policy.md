---
description: Kör stresstester mot Livefyre-plattformen.
title: Princip för stresstest
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Stresstest{#stress-test-policy}

Kör stresstester mot Livefyre-plattformen.

Detta dokument ger vägledning om hur man kör stresstester mot Livefyre-plattformen. Ad hoc-tester av kunder utan meddelanden är strängt förbjudna. Mer information om [otillåtna och tillåtna aktiviteter](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Stresstester är valfria. Du behöver inte eller förväntas utföra ett stresstest. Adobe Livefyre genomför regelbundna stresstester och valideringar som en del av releaseprocessen. Om du väljer att köra tester beskrivs kraven och begränsningarna för att utföra stresstester i det här dokumentet.

## Meddelande {#section_ihs_bfz_vdb}

Du måste meddela din kundframgångsspecialist på Livefyre och Adobe tekniska konsult om dina planerade tester tre eller fler veckor innan du planerar att börja.

Om du vill meddela Livefyre skickar du följande information till en av Livefyres nöjda kunder och Adobe tekniska konsulter:

* Syfte och beskrivning av testet
* Det användningsfall du testar mot
* Lista över alla Livefyre-API:er som du planerar att använda i testet
* Datum, tid och varaktighet för testet
* IP-adresser som du kommer att starta testerna från

## Krav {#section_khs_bfz_vdb}

Du får endast utföra tester om de uppfyller följande krav:

* Du måste få ett uttryckligt, skriftligt godkännande från en teknisk konsult i Adobe minst tre veckor innan du påbörjar testet.
* **Du får endast utföra tester på UAT-nätverket.**
* Du måste testa mot realistiska scenarier. Du kan till exempel inte anta att din egenskap betjänar *miljoner* postbegäranden varje dag, eftersom detta inte är ett realistiskt scenario. Om du behöver hjälp med att avgöra om ditt scenario är realistiskt eller inte kan du fråga din produktspecialist på Livefyre eller Adobe tekniska konsult.
* Testerna ska utföras under kontorstid för Stillahavsområdets standardtidszon \(UTC-7\).
* Du kan behöva ta fram data och ange skälen för testet.

## Styrning {#section_mhs_bfz_vdb}

Livefyre förbehåller sig rätten att när som helst avsluta ett test om du utför ett test:

* I produktionsnätverket.
* Utan uttryckligt skriftligt godkännande från en teknisk konsult i Adobe tre veckor eller mer i förväg.
* Mot orealistiska scenarier.

Livefyre avbryter tester genom att blockera åtkomst till API:er, inaktivera Livefyre Networks och neka en begäran om load test om den inte uppfyller kraven.
