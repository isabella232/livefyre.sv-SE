---
description: Skapa en ny samling genom att skapa en collectionMeta-token som skickas till Livefyre.
title: Skapa en samling med CollectionMeta-token
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Skapa en samling med CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}

Skapa en ny samling genom att skapa en collectionMeta-token som skickas till Livefyre.

1. Skapa collectionMeta-token.
1. Skapa kontrollsumman.

   Kontrollsumman krävs om du vill meddela Livefyre om ändringar du har gjort i din samling. Livefyre uppdaterar din samling endast om den angivna kontrollsumman skiljer sig från den tidigare skickade kontrollsumman. Att skapa en kontrollsumma påminner om att skapa en `collectionMeta`-token, men i stället för att anropa `buildCollectionMetaToken` anropar du `buildChecksum`.

Skapa användartokens för autentisering i Livefyre.
