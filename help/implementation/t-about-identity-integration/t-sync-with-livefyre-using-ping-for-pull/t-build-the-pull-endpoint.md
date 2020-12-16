---
description: Bygg pull-slutpunkten för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
seo-description: Bygg pull-slutpunkten för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.
seo-title: Bygg pull-slutpunkten
solution: Experience Manager
title: Bygg pull-slutpunkten
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Bygg pull-slutpunkten{#build-the-pull-endpoint}

Bygg pull-slutpunkten för att ta emot och besvara förfrågningar om åtkomst till ditt användaridentitetssystem.

1. Skapa en HTTPS-slutpunkt som tar emot Livefyre-begäranden och svarar med ett JSON-objekt som innehåller de senaste användaruppgifterna.

   >[!NOTE]
   >
   >Den här slutpunkten måste vara tillgänglig. Vi rekommenderar också starkt att både begäranden och svar skickas via HTTPS-protokollet.

1. Registrera slutpunkten med Studio.
