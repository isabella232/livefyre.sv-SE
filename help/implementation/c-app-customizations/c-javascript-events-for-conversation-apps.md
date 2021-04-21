---
description: Tillgängliga händelser som du kan binda JavaScript till för konversationsappar (till exempel kommentarer, chatt, live-blogg, granskningar och sidobjekt).
title: JavaScript-händelser för konversationsappar
exl-id: 2497346e-b2cc-44b2-bcd9-906dd443fe38
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 8%

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
| Twitter Reply | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
| Twitter Gilla | X | X | X | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt | Ej tillämpligt |
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
