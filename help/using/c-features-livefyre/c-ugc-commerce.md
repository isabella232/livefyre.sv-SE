---
description: Leverera produktspecifik användargenererat innehåll vid specifika punkter av kundresan för att öka inköpsengagemanget och konverteringsgraden med hjälp av funktionen för UGC-handel.
seo-description: Leverera produktspecifik användargenererat innehåll vid specifika punkter av kundresan för att öka inköpsengagemanget och konverteringsgraden med hjälp av funktionen för UGC-handel.
seo-title: UGC Commerce
solution: Experience Manager
title: UGC Commerce
uuid: 71e64901-a2b6-4957-ba88-058e4eaca537
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---


# UGC Commerce{#ugc-commerce}

Leverera produktspecifik användargenererat innehåll vid specifika punkter av kundresan för att öka inköpsengagemanget och konverteringsgraden med hjälp av funktionen för UGC-handel.

Använd funktionen för UGC-handel för att påverka inköpsavsikt och konvertering på UGC- och produktinformationssidor. Snabba upp time to market genom att smidigt koppla UGC till produktlager. Bygg varumärkeslojalitet genom att skapa en community med hjälp av UGC för att lyfta fram autentiska kundberättelser.

I AEM Livefyre finns flera sätt att importera produktkataloginformation, bland annat SKU, miniatyrbilder, pris och produktnamn. Hantera enkelt kopplingen mellan produkter och UGC med AEM Livefyres begäran om rättigheter, automatisk regeltaggning och modereringsarbetsflöden.

Förutom att påverka köpet kan AEM Livefyres UGC-handelserbjudande utnyttjas för att driva konverteringar på andra sätt, bland annat:

* Blygenerering inom B2B: placera åtgärdsknappar under UGC för att fånga leads
* Hämtning av B2C-appar: uppmana användare att hämta ett program
* Artikelhänvisningar: länka användare till artiklar som rör delar av användargenererat innehåll

Lägg produktanrop till åtgärder tillsammans med UGC för att öka konverteringsgraden. Du kan:

* Lägg till produktspecifik UGC i stor skala på tusentals produktinformationssidor.
* Bädda in AEM Livefyres visualiseringsappar som stöder UGC-handelsfunktioner som Media Wall och Mosaic på produktinformationssidor.
* Använd konfigurerbara hänvisningsspårningskoder med en analyslösning för att mäta konverteringarna från produktCTA som placerats på UGC och UGC på produktinformationssidor.

AEM Commerce-användare kan smidigt integrera sin befintliga produktkatalog i Livefyre för att öka användarengagemanget i Livefyres visualiseringsappar. Livefyre-användare som inte använder AEM Commerce kan importera produktkataloger manuellt till Livefyre. Mer information finns i [Överför produkter till Livefyre med filöverföring](/help/using/c-features-livefyre/c-ugc-commerce.md).

Program som använder den här funktionen:

* [Funktionskort](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app). Mer information om hur du använder UGC Commerce i ett funktionskort finns i [Anpassningar av funktionskort](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y).

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). Mer information om hur du använder UGC Commerce på en bildband finns i [Anpassningar av bildband](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations).

* [Medievägg](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app). Mer information om hur du använder UGC-handel i en medievägg finns i [Anpassningar av medievägg](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations).

* [Mosaik](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app). Mer information om hur du använder UGC-handel i Mosaik finns i [Mosaic Customizations](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations).

## Översikt: Så här använder du UGC Commerce Call-to-action-knappen {#section_s2d_tln_n1b}

1. Skapa en app med en Call-to-action-knapp. Se [Lägg till en Call-to-action-knapp i en app](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155).
1. Lägg till produktkatalogen i Livefyre. Du kan importera innehåll på ett av två sätt:

   * [Importera produkter till Livefyre med AEM ](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) Commerceiom du använder AEM Commerce.
   * [Överför produkter till ](/help/using/c-features-livefyre/c-ugc-commerce.md) Livefyreom du inte använder AEM Commerce.

1. Associera produkter med innehåll. Du kan göra detta på ett av fyra sätt:

   * Från biblioteket. Se [Associera produkter med innehåll med hjälp av biblioteket](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * Från ModQ. Se [Moderera innehåll med ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * Från appinnehåll. Se [Lägg till en Call-to-action-knapp i en app](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * Från en ström. Se [Alternativ för direktuppspelningsregel för alla direktuppspelningsregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).

## Överför produkter till Livefyre med filöverföring {#section_n1s_4hz_m1b}

Ladda upp produkter som ska användas med knappen Call-to-Action för att lägga till produkter som ska kopplas till innehåll eller redigera och ta bort befintliga filer.

>[!NOTE]
>
>Om du överför en fil till en mapp med befintliga filer tas alla filer i mappen bort och ersätts med den nya filen.

1. Navigera till **[!UICONTROL Network Settings > Products.]**
1. Skapa en **[!UICONTROL Product Folder]** eller använd en befintlig **[!UICONTROL Product Folder]**.

1. Klicka på **[!UICONTROL Product Folder]** för att markera den.
1. Klicka på knappen **[!UICONTROL Upload Products]**.
1. Överför en produktfil i något av följande format:

   * Google Products, filformat
   * Livefyre-format (se nedan)

   Överför en JSON-fil i standardformat. Du kan hämta en mall för att se ett exempel på standardformatet. Följande är ett exempel på en produktlinje i en mall. Den följer sekvensen `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   Tabellen förklarar de nyckel- och värdepar du behöver för att överföra produkter:

## Nyckel-/värdepar för standardformat för överföring av produktkatalog

| Nyckel | Typ | Beskrivning |
|--- |--- |--- |
| id | Sträng | Unikt ID för produkten. |
| oembed | Objekt | Bifogad bild `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | Sträng | Produkttitel. |
| isFolder | Boolean | Om true behandlas produkten som en mapp (till exempel &quot;meningar&quot;, &quot;kvinnor&quot; osv.). |
| parentId | Sträng | Definierar vilken mapp produkten finns under. |
| description | Sträng | Beskrivning av produkten. |
| pris | Sträng | Produktens värde i dollar. Exempel: 23.36. |
| sku | Sträng | Produktens lagerenhet (SKU). |
| url | Sträng | Länk till produktsidan. |
| aktiverad | Boolean | Värdet True innebär att produkten är aktiv. |
| attributes | Array | Typer och värden som definierar produkten (till exempel färg, storlek). Detta är en array med objekt.</br>**egenskaper:** </br>typ  </br>Typ: </br>StringDescription: Färg,  </br>värde  </br>Typ: Strängbeskrivning  </br>: Grön, XS |
| taggar | Array | Taggar som definierar innehållskategorier (t.ex. bilar, skor). Detta är en array med strängar. |

## ModQ {#section_os1_v4t_n1b}

Du kan associera innehåll med produkter från produktkatalogen i ModQ i enlighet med dina befintliga modereringsarbetsflöden. Mer information om hur du använder UGC Commerce med ModQ finns i [Moderate Content Using ModQ](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md).

## Strömmar {#section_qtj_v4t_n1b}

Du kan automatiskt koppla produkter till innehåll med hjälp av strömregler och sedan publicera innehållet automatiskt till en app, spara det i biblioteket eller moderera det med hjälp av ModQ. Mer information om hur du använder UGC-handel med strömregler finns i [Alternativ för strömregel för alla strömregler](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules).
