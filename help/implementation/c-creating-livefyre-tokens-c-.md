---
description: Lär dig hur du skapar Livefyre-tokens med språket "C#".
seo-description: Lär dig hur du skapar Livefyre-tokens med språket "C#".
seo-title: Skapar Livefyre-token`C#`
solution: Experience Manager
title: Skapar Livefyre-token`C#`
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Skapar Livefyre-token C\# {#creating-livefyre-tokens-c}

Lär dig hur du skapar Livefyre-token med språket ``C#``.

Du kan använda äldre dokumentation och exempelkod för `C#.NET` att skriva metoder för att skapa tokens.

Om du vill referera till Livefyres officiella bibliotek använder du [Java-biblioteket](https://github.com/Livefyre/livefyre-java-utils) som utgångspunkt för `C#` utvecklare.

Du kan också överväga att använda [Node.js-biblioteket](https://github.com/Livefyre/livefyre-nodejs-utils) från kommandoraden för att generera referenstoken för dig själv och för att lära dig mer om metodstrukturen.

* [Hoppa till metatoken för samling](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [Hoppa till autentiseringstoken](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## Beroenden {#section_c15_fnh_xz}

* Du behöver [JWT-genereringspaketet](https://www.nuget.org/packages/JWT) i ditt projekt för att kunna generera token.
* Kodexempel på den här sidan använder [Newtonsoft JSON](https://www.nuget.org/packages/newtonsoft.json/) -paketet.

## CollectionMeta-token {#section_dzt_4mh_xz}

CollectionMeta Token skickas till Livefyre när du bäddar in kommentarer på en sida och ger vårt system de metadata som krävs för den nya samlingen. Dessutom skapar du en MD5 `checksum` av dessa data som Livefyre kontrollerar för att se om metadata har ändrats. (t.ex. om artikelns titel eller URL har redigerats).

Denna token har signerats med din `Site Key`som du fick av din tekniska kontoansvarige på Livefyre.

Se även:

* Officiell CollectionMeta Token Docs
* [Exempel på Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. Skapa en ordlista som innehåller metadata för samlingen. Vi kommer bara att lägga till några av de nödvändiga fälten i det här steget, eftersom vi vill skapa en kontrollsumma för det här objektet innan vi lägger till articleId.

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **titel** *krävs*:  Samlingens titel, vanligtvis artikelns titel. Maxlängden är 255 tecken. stöder inte html-entiteter. Koda specialtecken med UTF-8.
   * **URL** *krävs*:  Artikelns kanoniska URL. Detta används av kommentardelning och funktioner för social synkronisering samt länkar till artikeln från Admin Dashboard. Om du testar lokalt bör du tänka på att Livefyre inte accepterar localhost som domän.
   * **taggar** *valfria*:  En kommaseparerad lista med taggar som du vill lägga till i samlingen på Livefyre-kontrollpanelen. Taggar får inte innehålla blanksteg. Använd understreck om du vill att ett mellanslag ska visas på Admin Dashboard.
   * **type** *optional*:  En sträng som anger vilken typ av samling som ska skapas. Giltiga värden är:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      Om inget anges skapas en LiveComments-samling som standard.


1. JSON kodar den här ordlistan och genererar en md5-kontrollsumma av den.

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. Lägg till **articleId** i ordlistan. Kontrollsumman **** går inte in i token collectionMeta, utan ska skickas som en separat parameter i convConfig-js-objektet.

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **articleId** *required*:  En unik identifierare för din samling på Livefyre-webbplatsen. Vanligtvis är det unika artikel-ID som används i ditt CMS. (t.ex. ditt WordPress-ID) Det här värdet ska aldrig ändras. Livefyre identifierar unika samlingar med kombinationen siteId och articleId.

1. Generera en signerad JWT-token för ordlistan med hjälp av den platsnyckel som du får av Livefyre. Observera att du måste ange rätt hash-algoritm, eftersom JWT-paketet inte använder HS256 som standard.

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## Autentiseringstoken för användare {#section_g1d_43h_xz}

Auth-token för användare används för att signera en användare till Livefyre. När en användare loggar in på din webbplats genererar webbplatsen en användarautentiseringstoken som skickas till Livefyre-widgeten på sidan. (Mer information om autentiseringsprocessen finns i Fjärrprofiler.)

Denna token kräver ditt nätverksnamn (network.fyre.co) och signeras med din nätverksnyckel som du får av din tekniska kontohanterare på Livefyre.

Se även:

* Officiell autentiseringstoken-dokument
* [Exempel på Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. Skapa en ordlista som innehåller nödvändig information.

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **domän:** Namnet på ditt nätverk (tillhandahålls av Livefyre). t.ex. mynetwork.fyre.co
   * **user_id:** Det unika användar-ID:t för användaren i platsens profilsystem. Endast alfanumeriska tecken får användas (A-Z, a-z, 0-9). Om användar-ID:t för ditt system innehåller ogiltiga tecken kan du skicka Livefyre en md5-hash med användar-ID:t eller en base64-kodad version av det. (Meddela din kontoansvarige om du gör detta.)
   * **upphör:** Det datum (i Epoch-tid) som token förfaller. Detta bör matcha sessionstiden för inloggningar på webbplatsen så att Livefyres inloggningsläge förblir synkroniserat med webbplatsens inloggningsläge.
   * **display_name:** Användarens visningsnamn i ditt profilsystem, som det ska visas i kommentarströmmen.

1. Generera en signerad JWT-token för ordlistan med den nätverksnyckel som tillhandahålls av Livefyre. Observera att du måste ange rätt hash-algoritm, eftersom JWT-paketet inte använder HS256 som standard.

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
