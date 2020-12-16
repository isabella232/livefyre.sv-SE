---
description: 'null'
seo-description: 'null'
seo-title: Smarta taggar
title: Smarta taggar
uuid: f978fa83-e79b-46ae-bb3e-0f9449bd0440
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Smarta taggar{#smart-tags}

Livefyre använder Adobe Sensei dataveteknik för att automatiskt tagga bilder och videor som du sparar eller överför i biblioteket.

Med smarta taggar kan du spara mycket tid genom att hantera, söka efter och strukturera innehåll. Med smarta taggar kan du:

* Söka i sparade och överförda bilder och videoklipp efter exakt innehåll baserat på bild- och videoinnehåll, i stället för enbart text
* Samla innehåll i strömmar baserat på exakta söktermer som analyserar bilden eller videon, i stället för bara text

När du sparar eller överför en bild eller video granskar Adobe Sensei automatiskt innehållet och taggar det med 135 000 klassificerare i tre kategorier:

* Funktioner (t.ex. katter, hundar, pyramider, landmärken)
* Kategorier (t.ex. resor, turism, skönhet)
* Estetiska egenskaper (till exempel bildkvalitet, tredjedelsregler)
* SFW/NSFW (på så sätt kan du automatiskt filtrera NSFW-bilder, vilket förbättrar säkerheten för strömmar och UGC-biblioteket

Rankningsalgoritmen för smarta taggar filtrerar innehåll med hjälp av ett smart kodkonfidensresultat, hur nytt innehållet är och hur många stjärnor en användare gav innehållet.

**Smarta taggar för video**

Funktioner:

* Smarta taggar används i MP4-, AVI- och MOV-videoformat
* Maximala längden för videor som stöds är 60 sekunder eller 50 MB
* Smarta taggar är tillgängliga i filer för social sökning, strömmar och överförd video i biblioteket

Märkordstyper:

* Funktionstaggar: Funktionen är densamma som funktionstaggarna för bilder (t.ex. katter, hundar, pyramider, landmärken).
* Åtgärdstaggar: Identifiera funktioner som finns i flera ramar i stället för bara en. Dessa är effektivare när det gäller att sammanfatta videoinnehåll.

Mer information om smarta taggar finns i [Direktuppspelningsregelalternativ för alla direktuppspelningsregler](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
