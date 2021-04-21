---
description: Anpassa datum- och tidsstämplar med Livefyre.js.
title: Anpassa datum- och tidsstämpeln
exl-id: 77130793-00ba-4a5c-8318-4221d971da6c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# Anpassa datum- och tidsstämpeln{#customize-the-date-and-time-stamp}

Anpassa datum- och tidsstämplar med Livefyre.js.

Livefyre Apps innehåller parametern option, datetimeFormat, som anger datumformatet enligt beskrivningen nedan.

* [Terminologi](#c_date_time_stamp/section_xsk_jn4_xz)
* [Formatering](#c_date_time_stamp/section_ynx_gn4_xz)
* [Symbolbeteckning](#c_date_time_stamp/section_inq_2n4_xz)

## Terminologi {#section_xsk_jn4_xz}

* **Absoluta** tidsstämplar definieras som exakta och specifika tider (t.ex. 1 januari 2012 12:00 pm)
* **Relativa** tidsstämplar definieras som allmänna och mindre exakta tider (t.ex. för 25 sekunder sedan, för 14 minuter sedan, för 1 dag sedan, för 1 år sedan osv.)

## Formaterar {#section_ynx_gn4_xz}

Parametern datetimeFormat har följande standardbeteende när inget argument anges:

* Datumtidsformat för: MMMM d yyyy (för 8 januari 2012)
* 20160 minuter (14 dagar) till absolut tid (14 dagar tills relativa tidsstämplar blir absoluta tidsstämplar)

Parametern datetimeFormat accepterar tre möjliga argumenttyper: datetime, format och sträng.

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

Ett objekt som anger absoluteFormat och/eller minutesuntilAbsoluteTime. Ett minutesWhenAbsoluteTime med värdet -1 gör att tiden är absolut.

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

En funktion som tar ett Date-objekt som argument och returnerar en datetime-sträng som ska visas

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## Symbolbeteckning {#section_inq_2n4_xz}

Formateringsfunktioner för datumtid enligt mönsterspecifikationen som definierats i JDK, ICU och CLDR, med mindre ändringar för vanlig användning i JS. Mer information finns i [dokumentationen för Google Closure Library](https://developers.google.com/closure/library/docs/overview).

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

Objekt som är markerade med * stöds inte ännu.

Objekt som är markerade med # fungerar annorlunda än Java.

Antalet mönsterbokstäver bestämmer formatet.

* **Text:** 4 eller fler, använd fullständigt format. Använd kort eller förkortad form om den finns, om den är kortare än 4. (Exempel: &quot;EEEE&quot; skapar &quot;Monday&quot;, &quot;EEE&quot; producerar &quot;Mon&quot;.)
* **tal:** minsta antalet siffror. Kortare siffror läggs till med noll (till exempel: Om &quot;m&quot; skapar &quot;6&quot;, &quot;mm&quot; skapar &quot;06&quot;.) År hanteras särskilt. om antalet&quot;y&quot; är 2 kommer år att trunkeras till två siffror. (Exempel: om &quot;yyyy&quot; skapar &quot;1997&quot;, &quot;yy&quot; skapar &quot;97&quot;.) Till skillnad från andra fält läggs bråksekunder till till höger med noll.
* **Text och nummer:** 3 eller högre, använd text. Färre än 3, använd nummer. (Exempel: &quot;M&quot; skapar &quot;1&quot;, &quot;MM&quot; skapar &quot;01&quot;, &quot;MMM&quot; skapar &quot;Jan&quot; och &quot;MMMM&quot; skapar &quot;January&quot;.)

Alla tecken i mönstret som inte ligger inom intervallet [&quot;a&quot;..&quot;.z&quot;] och [&quot;A&quot;..&quot;Z&#39;] behandlas som citattext. Tecken som&quot;:&quot;,&quot;.&quot;,&quot;#&quot; och&quot;@&quot; visas i den resulterande tidstexten även om de inte omsluts av enkla citattecken.
