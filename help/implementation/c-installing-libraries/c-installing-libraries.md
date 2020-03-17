---
description: Installera bibliotek för uppgifter på serversidan för Livefyre
seo-description: Installera bibliotek för uppgifter på serversidan för Livefyre
seo-title: Installation
solution: Experience Manager
title: Installation
uuid: f60b4cc7-178f-4a16-ba75-f1d0d171c52f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Installation{#installation}


## Java {#section_yd3_3zk_rz}

Om du vill installera Java-biblioteket lägger du till det här beroendet i projektets POM:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Java-biblioteket är beroende av följande moduler:

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

Mer information finns i Java-dokumenten eller i källan på [GitHub](https://github.com/Livefyre/livefyre-java-utils).

## NodeJS {#section_swj_pwq_rz}

Kör följande rad för att installera NodeJS-biblioteket:

`$ npm install livefyre`

NodeJS-biblioteket är beroende av följande moduler:

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

Mer information finns i NodeJs-dokumenten eller i källan på [GitHub](https://github.com/Livefyre/livefyre-nodejs-utils).

Länkar: [Restler](https://github.com/danwrong/restler), [Validator](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

Om du vill installera PHP-biblioteket med Composer lägger du till det i din Composer.json:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

Installera sedan med:

```
composer.phar install 
```

Om du **inte** använder Composer hämtar du den senaste versionen av biblioteket med:

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

Om du vill använda biblioteket lägger du till följande i PHP-skriptet:

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP-biblioteket är beroende av följande moduler:

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

Mer information finns i PHP-dokumenten eller i källan på [GitHub](https://github.com/Livefyre/livefyre-php-utils).

Länkar: [ext-json](https://php.net/manual/en/book.json.php), [förfrågningar](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

Kör den här raden för att installera Python-biblioteket:

`$ pip install livefyre`

Python-biblioteket är beroende av följande moduler:

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

Mer information finns i Python-dokumenten eller i källan på [GitHub](https://github.com/Livefyre/livefyre-python-utils).

Länkar: [PyJWT](https://github.com/progrium/pyjwt), [Requests](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

Om du vill installera Ruby-biblioteket lägger du till den här raden i programmets Gemfile:

```
gem 'livefyre' 
```

Eller installera själv:

`$ gem install livefyre`

Ruby-biblioteket är beroende av följande moduler:

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

Mer information finns i Ruby-dokumenten eller i källan på [GitHub](https://github.com/Livefyre/livefyre-ruby-utils).

Länkar: [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST Client](https://github.com/rest-client/rest-client/), [adresserbar](https://github.com/sporkmonger/addressable)
