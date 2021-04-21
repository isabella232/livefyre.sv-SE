---
description: Ta reda på antalet inlägg och kommentarer för vissa samlingar som ska visas på indexsidorna.
title: Visa antal kommentarer
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Visa antal kommentarer{#display-comment-count}

Ta reda på antalet inlägg och kommentarer för vissa samlingar som ska visas på indexsidorna.

Med Livefyres `CommentCount.js` kan du hämta innehållsantal för samlingar på din webbplats. Även om appar visar antalet kommentarer för den aktuella samlingen kan det vara bra att ha dessa antal syndikerade över hela webbplatsen. Den här funktionen är särskilt användbar om du inte vill behålla innehållet i databasen (eller om CMS-databasen inte synkroniseras med Livefyre).

1. Läs in JavaScript.

   Om du vill använda `CommentCount.js` måste du först bädda in JavaScript-filen i `<head>`-avsnittet på sidan eller mallen där du vill använda den.

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. Bind HTML-elementet.

   När skriptet har lästs in försöker det hitta andra element på sidan med klassnamnet `livefyre-commentcount`. För vart och ett av dessa element söker skriptet efter HTML-attributen `data-lf-site-id` och `data-lf-article-id` och använder dem för att hämta innehåll från Livefyre och uppdatera varje element med det senaste värdet.

   Följande element skulle till exempel uppdateras:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >Koden `CommentCount.js` söker efter ett numeriskt värde som ska uppdateras med det faktiska antalet. Var noga med att ta med ett numeriskt värde mellan taggarna.

   **Exempel 1** (Använda URL:en som artikel-ID):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **Exempel 2** (Använda ett numrerat system som artikel-ID):

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. Konfigurera alternativ.

   Om du vill ha mer kontroll över hur innehållsantalet ersätts anropar du `LF.CommentCount()` och skickar ett objekt som innehåller konfigurationsalternativen. Se till att anropa funktionen efter att alla element som behöver ersättas finns i DOM. Det bästa stället att anropa den här metoden är i sidfoten, så det händer när DOM läses in, men före händelserna document och window ready.

   Vi tillåter följande konfigurationsalternativ:

* **replacer:** Function eller Regex som används för att ersätta texten för varje innehållsantal.

* **function:** Används för att ersätta varje element. Funktionens argument är:

   **element:** Det HTML-element som uppdateras.
   **count:** The content count for this element.

* **regex:** Används för att avgöra vilken del av elementets text som ska ersättas av antalet.

   **Exempel**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >Använd replacer för att anpassa eller internationalisera kommentarräkningsmeddelandet.
