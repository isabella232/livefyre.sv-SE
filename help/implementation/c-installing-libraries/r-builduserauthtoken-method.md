---
description: Returnerar en krypterad användarautentiserad token för det nätverk den anropas från.
seo-description: Returnerar en krypterad användarautentiserad token för det nätverk den anropas från.
seo-title: buildUserAuthToken-nätverksmetod
solution: Experience Manager
title: buildUserAuthToken-nätverksmetod
uuid: 8828d356-c3c6-46a6-91bf-83bd59e35050
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

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
