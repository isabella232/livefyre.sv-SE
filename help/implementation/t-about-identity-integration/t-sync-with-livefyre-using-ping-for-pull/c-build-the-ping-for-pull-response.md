---
description: Bygg Ping for Pull-svaret för att skicka uppdaterad användarinformation till Livefyre.
seo-description: Bygg Ping for Pull-svaret för att skicka uppdaterad användarinformation till Livefyre.
seo-title: Bygg Ping for Pull Response
solution: Experience Manager
title: Bygg Ping for Pull Response
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Bygg Ping for Pull Response{#build-the-ping-for-pull-response}

Bygg Ping for Pull-svaret för att skicka uppdaterad användarinformation till Livefyre.

| Typ | Egenskap | Beskrivning |
|--- |--- |--- |
| Sträng *krävs* | id | Användar-ID för användaren i profilsystemet. Detta måste vara unikt för alla användare i ditt nätverk och får aldrig ändras. |
| Sträng *krävs* | display_name | Användarens visningsnamn. Detta återges med Livefyre-innehåll som publiceras av användaren. |
| Objektet är *valfritt, men rekommenderas* | name | Strängar som definierar användarens formaterade, första, mellersta och efternamn. |
| Sträng *valfri, men rekommenderas* | e-post | Användarens e-postadress. Används för att skicka e-postmeddelanden. |
| Sträng *valfri, men rekommenderas* | image_url | URL till en avatar som ska visas för användaren. Livefyre skalar upp överförda bilder till 100 × 100, 75 × 75 eller 50 × 50 pixlar, beroende på vad som är lämpligt. För bästa resultat bör användarna ladda upp en fyrkantig bild med 100 × 100 pixlar. Om du vill vara säker på att avatarbilden uppdateras i Livefyre ändrar du image_url för varje bilduppdatering så Ping for Pull identifierar att bilden har ändrats. Bifoga t.ex. en tidsstämpel till filnamnet eller stega upp bildändringarna. Obs!  Alla URL-adresser måste vara fullständigt kvalificerade och tillgängliga. |
| Sträng *valfri, men rekommenderas* | profile_url | URL till användarens profilsida på webbplatsen. |
| Sträng *valfri, men rekommenderas* | settings_url | URL till en sida där användarna kan konfigurera användarens profilinställningar för platsen. |
| Matris *är valfritt, men rekommenderas* | taggar | Används för att tilldela användare till användargrupper. Taggar kan innehålla 1-63 alfanumeriska tecken och understreck. |
| Booleskt *valfritt, men rekommenderas* | autofollow_conversations | Definierar om en användare automatiskt vill följa en samling efter publicering. När användare följer en samling får de e-postmeddelanden när andra användare deltar. Kan vara sant eller falskt. Standardvärdet är true. |
| Objektet är *valfritt, men rekommenderas* | email_notifications | Definierar frekvensen för tillgängliga Livefyre-e-postmeddelanden. Olika frekvenser kan anges för varje meddelandetyp. Som standard skickas inga meddelanden. <br><ul><li> skickar meddelanden omedelbart efter den angivna händelsen. </li><li>skickar ofta meddelanden gruppvis. </li><li> skickar aldrig e-postmeddelanden för aktiviteten. </li><li>*kommentarer*: Definierar när meddelanden skickas när andra användare publicerar innehåll i samlingar som den här användaren följer. </li><li>*svar*: Definierar när meddelanden skickas när en annan användare svarar på den här användarens innehåll.</li><li>*Gilla*: Definierar när meddelanden skickas när en annan användare gillar den här användarens innehåll.</li><li>*moderator_comments*: Definierar när meddelanden skickas till moderatorer när användare publicerar innehåll i en samling i nätverket.</li><li>*moderator_flags*: Definierar när meddelanden skickas till moderatorer när andra användare flaggar innehåll i en samling i nätverket.</li></ul> |
| Sträng *valfri* | plats | En plats som har skickats av användaren. |
| Sträng *valfri* | bio | En självbiografi som användaren har skickat in. |
| Array ( *tillval)* | webbplatser | En array med användarskickade webbplatser. Max = 2. |
| Objekt *valfritt* | display_rules | Definierar vilka profilegenskaper som är offentligt synliga för andra användare. Varje tillgänglig parameter tar boolesk inmatning som true eller false. Tillgängliga parametrar:  <br><ul><li>bio </li><li> plats</li><li>  kön </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| Boolean *valfritt* | moderator | Definierar om användaren har moderatorbehörighet i nätverket. |
| Boolean *valfritt* | gravatar_disabled | Definierar om Livefyres användning av en gravatar ska inaktiveras om inget image_url anges. |

## Exempel på svar {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
