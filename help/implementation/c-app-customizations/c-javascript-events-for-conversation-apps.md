---
description: Tillgängliga händelser som du kan binda JavaScript till för konversationsappar (till exempel kommentarer, chatt, live-blogg, granskningar och sidobjekt).
seo-description: Tillgängliga händelser som du kan binda JavaScript till för konversationsappar (till exempel kommentarer, chatt, live-blogg, granskningar och sidobjekt).
seo-title: JavaScript-händelser för konversationsappar
solution: Experience Manager
title: JavaScript-händelser för konversationsappar
uuid: cce112b5-7c3a-4721-9854-fc8471f3d5d0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 11%

---


# JavaScript-händelser för konversationsappar{#javascript-events-for-conversation-apps}

Tillgängliga händelser som du kan binda JavaScript till för konversationsappar (till exempel kommentarer, chatt, live-blogg, granskningar och sidobjekt).

## Matris för konversationsappar och händelser {#section_y4j_x4m_ybb}

Här följer en matris med de händelser som är tillgängliga för konversationsappar. Ett X anger att händelsen är tillgänglig för appen, N/A anger att händelsen inte gäller för appen och ingen markering betyder att händelsen inte är tillgänglig för appen:

### Apphändelser för konversationer

| Händelser | Kommentarer | Chatt | Liveblog | Recensioner | Sidenotes | Omröstningar | Trender |
|---|---|---|---|---|---|---|---|
| Init | X | X | X | X | X |  |  |
| Läs in | X | X | X | X |  |  |  |
| Visa | X | X | X | X |  |  |  |
| Bokför | X | X | X | X |  | Ej tillämpligt | Ej tillämpligt |
| Bokfört | X | X | X | X | X | Ej tillämpligt | Ej tillämpligt |
| Twitter-svar | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Twitter gillar | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| LF gillar | X | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| LF ogilla | X | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Dela efter | X | X |  | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Knappen Dela | X | X | X | X |  | Ej tillämpligt | Ej tillämpligt |
| Dela Twitter | X | X | X | X | X | Ej tillämpligt | Ej tillämpligt |
| Dela Facebook | X | X | X | X | X | Ej tillämpligt | Ej tillämpligt |
| Dela URL | X | X | X | X |  | Ej tillämpligt | Ej tillämpligt |
| ExpanderaSvar | X | Ej tillämpligt | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Komprimera svar | X | Ej tillämpligt | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Flaggknapp | X | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Flagga | X | X | X | X | X | Ej tillämpligt | Ej tillämpligt |
| Avbryt flagga | X | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Följ | X | Ej tillämpligt | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Unfollow | X | Ej tillämpligt | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| RequestMore | X | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| ModalView |  | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Twitter Retweet | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Knappen Posta | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Antal kommentarer har uppdaterats | X | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Användaren är inloggad |  |  |  |  |  | Ej tillämpligt | Ej tillämpligt |
| Användaren är utloggad |  |  |  |  |  | Ej tillämpligt | Ej tillämpligt |
| Kommentar |  | Ej tillämpligt |  |  | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Kommentaren är inte tillgänglig |  | Ej tillämpligt |  |  | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Omröstad kommentar | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | X | X | Ej tillämpligt | Ej tillämpligt |
| Val av omröstning | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |  | Ej tillämpligt |
| Trendartikel markerad | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |  |
| Nätverks-ID |  |  |  |  |  |  |  |
| Program-ID | X | X | X | X |  |  |  |
| Kontext-ID | X | X | X | X |  |  |  |
| Apptyp | X | X | X | X |  |  |  |
| Innehållstyp | X | X | X | X |  |  |  |
| Publicerat datum till app |  |  |  |  |  |  |  |
| Inloggad i slutanvändarappen |  |  |  |  |  |  |  |

