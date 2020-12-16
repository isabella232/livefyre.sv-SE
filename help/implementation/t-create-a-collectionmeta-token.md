---
description: Skapa en ny samling genom att skapa en collectionMeta-token som skickas till Livefyre.
seo-description: Skapa en ny samling genom att skapa en collectionMeta-token som skickas till Livefyre.
seo-title: Skapa en samling med CollectionMeta-token
solution: Experience Manager
title: Skapa en samling med CollectionMeta-token
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Skapa en samling med CollectionMeta Token{#create-a-collection-using-the-collectionmeta-token}

Skapa en ny samling genom att skapa en collectionMeta-token som skickas till Livefyre.

1. Skapa collectionMeta-token.
1. Skapa kontrollsumman.

   Kontrollsumman krävs om du vill meddela Livefyre om ändringar du har gjort i din samling. Livefyre uppdaterar din samling endast om den angivna kontrollsumman skiljer sig från den tidigare skickade kontrollsumman. Att skapa en kontrollsumma påminner om att skapa en `collectionMeta`-token, men i stället för att anropa `buildCollectionMetaToken` anropar du `buildChecksum`.

Skapa användartokens för autentisering i Livefyre.