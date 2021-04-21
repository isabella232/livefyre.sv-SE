---
description: Bygg pull-slutpunkten för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
title: Bygg pull-slutpunkten
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# Bygg pull-slutpunkten{#build-the-pull-endpoint}

Bygg pull-slutpunkten för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.

1. Skapa en HTTPS-slutpunkt som tar emot Livefyre-begäranden och svarar med ett JSON-objekt som innehåller de senaste användaruppgifterna.

   >[!NOTE]
   >
   >Den här slutpunkten måste vara tillgänglig. Vi rekommenderar också starkt att både begäranden och svar skickas via HTTPS-protokollet.

1. Registrera slutpunkten med Studio.
