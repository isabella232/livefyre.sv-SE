---
description: Ge kunderna möjlighet att betygsätta och granska era produkterbjudanden.
seo-description: Ge kunderna möjlighet att betygsätta och granska era produkterbjudanden.
seo-title: Recensioner
solution: Experience Manager
title: Recensioner
uuid: b740ee28-f6f9-4ae7-9fe7-61a5cde97bbb
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 0%

---


# Recensioner {#reviews}

Ge kunderna möjlighet att betygsätta och granska era produkterbjudanden.

Med granskningar kan medlemmar i communityn lägga in stjärngraderingar och kvalitativa granskningar för alla produkter och tjänster.

## Integrering {#section_kk5_15b_c1b}

Om du vill integrera en granskningsapp följer du proceduren för att integrera en konversationsapp. Se [Bädda in en app](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md). Följande är ett exempel på en inbäddad granskningsapp.

### Exempel

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

Som du kan se i avsnittet Building `CollectionMeta` är `CollectionMeta` ett kodat JSON-objekt. I ovanstående exempel har JSON-objektet följande format innan det är JWT-kodat:

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig-objekt {#section_pzv_ytb_c1b}

Om du redan har slutfört avsnittet Komma igång bör du känna till convConfig-objektet. Om du vill aktivera granskningar uppdaterar du convConfig med följande fält:

* **** ** alwaysShowEditoroptionalboolean: Som standard visas granskningsredigeraren först när användaren trycker på knappen&quot;Skriv granskning&quot;. Ställ in den här parametern på true om du alltid vill visa redigeraren.

* **** ** apprequiredString: Programnamnet som ska användas för granskningar. Måste vara &quot;recensioner&quot;.

* **** ** defaultSortoptionalstring: Gör att du kan välja standardsorteringsalternativet för granskningar. Möjliga värden är: MostHelpful, highestRated, bottomRated, newest och old.

* **disable** ** Titleoptionalboolean: Inaktiverar och döljer titelfältet i granskningsredigeraren, som är obligatoriskt och synligt som standard. Standardvärdet är true.

* **enableHalfRatingoptionalboolean:** **  Används för att aktivera halv klassificering i standardstjärnans markeringsmodul. Standardvärdet är true.

* **** ** hideShowReviewButtonOptionBoolesk: Anger om  [!UICONTROL Show My Review] knappen ska visas. Ange som true om du vill att användarna ska kunna välja om de vill visa eller visa sina egna granskningar.

* **** ** maxRatingoptionalinteger Används för att ange antalet stjärnor som visas i standardstjärnans markeringsmodul. Standardvärdet är 5. Detta kan konfigureras upp till 100.

* **** ** ratingSummaryEnabledoptionalboolean: Används för att visa klassificeringssammanfattningen ovanför granskningsappen. Detta måste aktiveras för att du ska kunna använda ratingSummaryDelegate. Standardvärdet är true.

## Granska samlingsmetadata {#section_k1s_sqb_c1b}

* **typ:** ** obligatorisk sträng: Definierar samlingstypen. Måste vara `reviews`.

* **** ** ratingDimensionsOptionsArray: En array med strängar för varje typ av dimension som den här samlingen ska använda. Om detta inte anges tillåts bara 1 dimension.

   Om du till exempel vill att användarna ska kunna klassificera produkten som&quot;design&quot;,&quot;funktioner&quot; och&quot;prestanda&quot;, ställer du in matrisen på: `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **** ** ratingSubparts, valfritt heltal: Antal partitioner som ska visas i textrutan för granskningen. Underdelsetiketterna skickas in med parametern enligt nedan.

   >[!NOTE]
   >Du måste definiera etiketter för varje underdel.

* **** ** ratingSubpartsIdsoptionalarray: Gör att du kan definiera ett ID för varje underdel i din Ratings Collection, som kan användas för att ange deldeldelelementen i din CSS och JavaScript som mål. När användare publicerar granskningar kommer varje `ratingSubpart` att ha attributet `data-lf-subpart-id` ifyllt med detta ID.

>[!NOTE]
>
>Om du vill använda `ratingSubpartsIds` måste även parametern `ratingSubparts` definieras och längden på de två arrayerna måste matcha.

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>Om du använder `ratingDimensions` MÅSTE du använda `ratingSelectionDelegate`, `ratingDisplayDelegate` och `ratingSummaryDelegate` (om du vill visa klassificeringssammanfattningen).

## Anpassning av granskningar {#section_khz_xmb_c1b}

### Konfigurera stjärnbilder

Om du vill ändra bilden för fullständiga stjärnor är klassen `goog-ratings-star`. Ändra bakgrundsbilden till vilken bild du vill. Som standard är stjärnorna 28 x 28 pixlar.

### Konfigurera stjärnbilder med halva stjärnor

Med halv stjärna finns det två klasser, en för varje sida av stjärnan. Den vänstra sidan av halvstjärnan är `fyre-rating-half-odd` och den högra sidan är `fyre-rating-half-even`. Som standard är halva stjärnor 28 x 14 pixlar.

### Konfigurera verktygstipsvärden för stjärnor

Om du vill konfigurera verktygstipsvärden för stjärnorna följer du den anpassade text som beskrivs i String Customizations. När du har ställt in den använder du nyckeln `ratingValues` och värdet på en array som innehåller verktygstipssträngarna. Om du har inaktiverat halva stjärnor bör antalet element i arrayen vara samma som `maxRating` (ovan). Om du har aktiverat halva stjärnor ska antalet element vara 2x `maxRating`. Det första elementet i arrayen motsvarar det element som är längst till vänster (eller en halv stjärna) och fortsätter från vänster till höger.

### Växla alternativet Visa min granskning

Om du vill aktivera eller inaktivera alternativet [!UICONTROL Show My Review] anger du parametern `hideShowReviewButton` som mål i appkonfigurationen.

### Visa textredigeraren som standard

Granskningsredigeraren visas bara när användaren trycker på knappen [!UICONTROL write review]. Om du vill visa det här formuläret som standard anger du parametern `alwaysShowEditor` som mål i appkonfigurationen.
