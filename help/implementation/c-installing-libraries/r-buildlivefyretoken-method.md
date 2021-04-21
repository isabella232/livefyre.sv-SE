---
description: Returnerar en krypterad, giltig Livefyre-token som kan användas för att interagera med andra Livefyre-API:er för det nätverk som anropas från.
title: buildLivefyreToken - nätverksmetod
exl-id: 2b303606-e8de-41e5-9c01-b41cc7bd8437
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# buildLivefyreToken-nätverksmetod{#buildlivefyretoken-network-method}

Returnerar en krypterad, giltig Livefyre-token som kan användas för att interagera med andra Livefyre-API:er för det nätverk som anropas från.

Returnerar en krypterad, giltig Livefyre-token som kan användas för att interagera med andra Livefyre-API:er för det nätverk som anropas från.

Som standard upphör denna token att gälla om 24 timmar efter att den skapades.

## Java-exempel {#section_nyl_ycs_rz}

```
network.buildLivefyreToken(); 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
network.buildLivefyreToken(); 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## PHP-exempel {#section_ghf_gds_rz}

```
network.buildLivefyreToken(); 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Python-exempel {#section_dwg_gds_rz}

```
network.build_livefyre_token() 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## Ruby-exempel {#section_enh_gds_rz}

```
network.build_livefyre_token() 
```

Exempelutdata:

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```
