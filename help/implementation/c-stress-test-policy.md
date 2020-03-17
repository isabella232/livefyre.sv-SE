---
description: Kör stresstester mot Livefyre-plattformen.
seo-description: Kör stresstester mot Livefyre-plattformen.
seo-title: Princip för stresstest
solution: Experience Manager
title: Princip för stresstest
uuid: f2d49b55-f4fc-485f-9aea-a17ce64813ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Princip för stresstest{#stress-test-policy}

Kör stresstester mot Livefyre-plattformen.

Detta dokument ger vägledning om hur man kör stresstester mot Livefyre-plattformen. Ad hoc-tester av kunder utan meddelanden är strängt förbjudna. Mer om [förbjudna och tillåtna aktiviteter](#c_stress_test_policy/section_mhs_bfz_vdb).

>[!NOTE]
>
>Stresstester är valfria. Du behöver inte eller förväntas utföra ett stresstest. Adobe Livefyre genomför regelbundna stresstester och valideringar som en del av releaseprocessen. Om du väljer att köra tester beskrivs kraven och begränsningarna för att utföra stresstester i det här dokumentet.

## Meddelande {#section_ihs_bfz_vdb}

Du måste meddela din vinnande kundspecialist och Adobes tekniska konsult om dina planerade tester tre eller fler veckor innan du planerar att börja.

Om du vill meddela Livefyre skickar du följande information till en av Livefyres nöjda kunder och Adobes tekniska konsulter:

* Syfte och beskrivning av testet
* Det användningsfall du testar mot
* Lista över alla Livefyre-API:er som du planerar att använda i testet
* Datum, tid och varaktighet för testet
* IP-adresser som du kommer att starta testerna från

## Krav {#section_khs_bfz_vdb}

Du får endast utföra tester om de uppfyller följande krav:

* Du måste få ett uttryckligt, skriftligt godkännande från en Adobe Technical Consultant i minst tre veckor innan du påbörjar testet.
* **Du får endast utföra tester på UAT-nätverket.**
* Du måste testa mot realistiska scenarier. Du kan till exempel inte anta att din egendom kommer att betjäna *miljontals* efterfrågningar varje dag, eftersom detta inte är ett realistiskt scenario. Om du behöver hjälp med att avgöra om ditt scenario är realistiskt eller inte kan du fråga din livefyre Customer Success Specialist eller Adobes tekniska konsult.
* Testerna ska utföras under kontorstid för Stillahavsområdets standardtidszon \(UTC-7\).
* Du kan behöva ta fram data och ange skälen för testet.

## Styrning {#section_mhs_bfz_vdb}

Livefyre förbehåller sig rätten att när som helst avsluta ett test om du utför ett test:

* I produktionsnätverket.
* Utan uttryckligt skriftligt godkännande från en Adobe Technical Consultant tre veckor eller mer i förväg.
* Mot orealistiska scenarier.

Livefyre avbryter tester genom att blockera åtkomst till API:er, inaktivera Livefyre Networks och neka en begäran om load test om den inte uppfyller kraven.
