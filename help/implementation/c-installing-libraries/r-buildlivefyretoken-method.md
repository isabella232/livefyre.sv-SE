---
description: Returnerar en krypterad, giltig Livefyre-token som kan användas för att interagera med andra Livefyre-API:er för det nätverk som anropas från.
seo-description: Returnerar en krypterad, giltig Livefyre-token som kan användas för att interagera med andra Livefyre-API:er för det nätverk som anropas från.
seo-title: buildLivefyreToken - nätverksmetod
solution: Experience Manager
title: buildLivefyreToken - nätverksmetod
uuid: 7c72a05f-669b-4df3-8117-aa4af2f7a179
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildLivefyreToken - nätverksmetod{#buildlivefyretoken-network-method}

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

