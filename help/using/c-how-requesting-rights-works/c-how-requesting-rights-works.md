---
description: Lär dig hur rättighetsförfrågningar fungerar. När du överför användargenererat innehåll (UGC) till en Livefyre-app innehåller innehållet tystlåten behörighet för återanvändning. Du måste ha författarens tillstånd att använda innehåll från Twitter eller Instagram.
seo-description: Lär dig hur rättighetsförfrågningar fungerar. När du överför användargenererat innehåll (UGC) till en Livefyre-app innehåller innehållet tystlåten behörighet för återanvändning. Du måste ha författarens tillstånd att använda innehåll från Twitter eller Instagram.
seo-title: Begär rättigheter
title: Begär rättigheter
uuid: d3194afa-f3c6-44ed-b03f-9b1ecb50c1d3
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# Begära rättigheter{#requesting-rights}

Lär dig hur rättighetsförfrågningar fungerar. När du överför användargenererat innehåll (UGC) till en Livefyre-app innehåller innehållet tystlåten behörighet för återanvändning. Du måste ha författarens tillstånd att använda innehåll från Twitter eller Instagram.

Följande rättighetsstatusar är tillgängliga från biblioteket, appinnehållet, ModQ och AEM Commerce:

* **[!UICONTROL Granted]**. När författaren ger dig rätt att återanvända innehållet ändras resursens status till **[!UICONTROL Granted]**.

* **[!UICONTROL Expired]**. Livefyre övervakar Instagram- och Twitter-strömmen för författarens svar i 14 dagar. Efter 14 dagar förfaller begäran och statusen för rättighetsbegäran ändras till **[!UICONTROL Expired]**. Du kan skicka ytterligare en begäran eller ta bort objektet från biblioteket.
* **[!UICONTROL Requested]**. Begär behörighet för innehåll från biblioteket. Du kan göra detta för en eller flera resurser i taget. När du har begärt behörighet anger Livefyre resursstatusen till **[!UICONTROL Requested]**.
* **[!UICONTROL Needs Review]**. Om författaren svarar med en anteckning som inte innehåller din #approvalHashtag, ändras resursens status till **[!UICONTROL Needs Review]**.

* **[!UICONTROL Request Failed]**. Det gick inte att skicka begäran (på grund av utgånen token osv.).
* **[!UICONTROL Request Pending]**. Köar rättighetsbegäran så att inte för många skickas samtidigt.

Du kan begära rättigheter för resurser som du har fått från Twitter och Instagram. Du måste spara resursen i biblioteket för att begära rättigheter.

Du måste konfigurera ett *Instagram-företagskonto* för att begära rättigheter för resurser från Instagram med ett delvis automatiserat arbetsflöde.

Du kan bara använda den här funktionen för innehåll som du får från en sökning eller direktsökning via ett företagskonto. Om du vill begära rättigheter för innehåll som du har fått från ett personligt Instagram-konto måste du skicka rättighetsförfrågningar manuellt.

>[!NOTE]
>
>Mer information om olika typer av Instagram-konton och hur du använder dem finns i [Om Instagram-konton](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts). Information om hur du begär rättigheter för Instagram-konton finns i [Skicka manuella rättighetsbegäranden](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md#c_send_instagram_manual_rights_request) och [Skicka delvis automatiserade rättighetsbegäranden](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md#c_send_an_instagram_rights_request_from_the_library).

