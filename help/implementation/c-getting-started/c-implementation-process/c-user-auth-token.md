---
description: I det här avsnittet beskrivs hur du skapar det JSON-objekt för UserAuth som skapar den token för användarautentisering som krävs för att logga in användare i dina appar.
title: Autentiseringstoken för användare
exl-id: 564144dd-6db4-447b-80ac-b743ecac833d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Autentiseringstoken för användare{#user-auth-token}

I det här avsnittet beskrivs hur du skapar det JSON-objekt för UserAuth som skapar den token för användarautentisering som krävs för att logga in användare i dina appar.

I det här avsnittet beskrivs hur du skapar det JSON-objekt för UserAuth som skapar den token för användarautentisering som krävs för att logga in användare i dina appar.

Om du vill skapa en variabel använder du det önskade språkbiblioteket och skickar följande parametrar:

| Parameter | Typ | Beskrivning |
|---|---|---|
| networkName | Sträng *krävs* | Namnet på Livefyre-nätverket (tillhandahålls av Livefyre). |
| networkKey | Sträng *krävs* | Den hemliga nyckeln för det här specifika nätverket (tillhandahålls av Livefyre). |
| userId | Sträng *krävs* | ID:t för användaren som loggar in som det är lagrat i ditt användarhanteringssystem (endast alfanumeriska tecken, bindestreck, understreck och punkttecken tillåts: [a-zA-Z0-9_-.]). **Obs!** UserId måste vara unikt. |
| förfaller | Heltal *krävs* | När token ska upphöra att gälla från och med nu (i sekunder). **Obs!** Det här värdet kan också skickas som ett flyttal. JSON-webbtoken som skapas lagrar det här värdet i UNIX-epok. |
| displayName | Sträng *krävs* | Text som identifierar den här användaren i användargränssnittet och i kommentarer. (Maximalt antal tecken: 50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>Nätverksnycklar delas inte för demosite-konton för Livefyre. Du får en nätverksnyckel när Livefyre har etablerat en miljö åt dig. Den här nyckeln bör hållas privat.
