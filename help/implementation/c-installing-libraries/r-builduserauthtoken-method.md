---
description: Returnerar en krypterad användarautentiserad token för det nätverk den anropas från.
title: buildUserAuthToken-nätverksmetod
exl-id: dcc61c4b-90d9-42a0-9f46-73a843a4ad78
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# buildUserAuthToken-nätverksmetod{#builduserauthtoken-network-method}

Returnerar en krypterad användarautentiserad token för det nätverk den anropas från.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| userId | Sträng | Användar-ID för användaren som denna token tillhör. |
| displayName | Sträng | Användarens visningsnamn. |
| förfaller | Dubbel | När token ska upphöra att gälla om några sekunder. |

## Java-exempel {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Python-exempel {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ruby-exempel {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
