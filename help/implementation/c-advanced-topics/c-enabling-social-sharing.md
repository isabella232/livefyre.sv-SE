---
description: Konfigurera autentiseringsuppgifter som gör att dina användare kan dela innehåll till olika sociala nätverk.
title: Aktivera delning via sociala medier
exl-id: 08ac9766-52ea-432f-8b4f-bf68cb8b62bc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Aktiverar delning via sociala medier {#enabling-social-sharing}

Konfigurera autentiseringsuppgifter som gör att dina användare kan dela innehåll till olika sociala nätverk.

Om du vill att användare ska kunna dela innehåll på webbplatser för sociala medier ska du implementera funktionen för delning via sociala medier i Livefyre och skapa ett OAuth-system för att kunna autentisera webbplatserna på rätt sätt. Med det här systemet agerar Livefyre å användarens vägnar när de väljer att dela innehåll via sociala medier.

>[!NOTE]
>
>Olika leverantörer har olika OAuth-krav. Kontakta leverantörerna för att få information om hur de implementerar OAuth.

## Nödvändiga sociala autentiseringsuppgifter {#section_gff_cjm_b1b}

Om du använder ett anpassat användaridentitetssystem måste du ange dina sociala autentiseringsuppgifter för att användare ska kunna dela till Twitter, Facebook eller LinkedIn från en Livefyre-app.

>[!NOTE]
>
>Kunder som använder Janrain Engage behöver bara ange sin Engage Domain- och Engage API Key.

Använd panelen Integrationsinställningar i Admin Console för att ange eller uppdatera följande inloggningsuppgifter för sociala medier.

### Nödvändiga autentiseringsuppgifter:

* **Omdirigering av** klienthemlighet för OAuth-proxy för klient-ID
* **API-hemlighet** för LinkedInAPI-nyckel
* **API-hemlighet för** token för tokenåtkomsttoken för API-nyckel för TwitterAccess

## Twitter {#section_qp5_1yl_b1b}

Twitter-autentiseringsuppgifter är tillgängliga från Twitter App Dashboard. Så här hittar du dessa autentiseringsuppgifter:

* Öppna [Twitter App Dev Page](https://dev.twitter.com/apps) som appägare, hitta ditt program och klicka på titeln.
* Bläddra ned till &quot;Din åtkomsttoken&quot; och hämta värdena från &quot;Åtkomsttoken&quot; och &quot;Åtkomsttokenhemlighet&quot;.

Du måste:

* Ange ett värde för fältet Återanrops-URL i Twitter App. Det här fältet kan vara en enkel platshållare, men kan inte lämnas tomt.
* Ange att programtypen ska ha tillgång till både **read** och **write**.
* Bekräfta att webbadressen till Twitter App-webbplatsen finns på samma värddomän som kärnappen Livefyre.

>[!NOTE]
>
>Alla program som visar Twitter-innehåll måste uppfylla kraven för visning. Mer information finns i [Twitter Display Guidelines](https://dev.twitter.com/terms/display-requirements).

## linkedIn {#section_lfz_zxl_b1b}

linkedIn-autentiseringsuppgifter finns tillgängliga i avsnittet OAuth-nycklar i API-nycklarna för ditt LinkedIn-program.

* Logga in på ditt konto från LinkedIn utvecklarsida [https://developer.linkedin.com/](https://developer.linkedin.com/).
* Hovra över ditt namn i det övre högra hörnet och välj API-nycklar i listrutan.
* Klicka på programtiteln.
* Hämta API-nyckelvärden och hemlig nyckel från avsnittet OAuth-nycklar

## Facebook {#section_zyb_gpl_b1b}

Facebook-inloggningsuppgifter finns på din Developer Apps-sida.

* Öppna [Facebook Developer Apps Page](https://developers.facebook.com/apps) som appägare, hitta ditt program och klicka på titeln.
* Hämta in värdena för App ID och App Secret. För programhemligheten kan du behöva klicka på knappen Visa för att visa den.

När du delar till Facebook måste du konfigurera en omdirigeringssida så att du kan ta Facebook-förfrågningar och följa de domänrutiner som krävs av [Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/). Sidan måste finnas på din domän så att Facebook kan verifiera att begäran kommer från en giltig källa.

### Facebook Redirect

Värdsidan ska innehålla följande kod:

### Ruby

Detta är ett exempel där Ruby och Rails används för att utföra Facebook OAuth-omdirigeringen.

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

Detta är ett exempel på hur Python och Django använder omdirigeringen Facebook OAuth.

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

Detta är ett exempel där NodeJS och Sail/Express används för att utföra Facebook OAuth-omdirigeringen.

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

Detta är ett exempel på hur du använder Java- och Spring-kontroller för att utföra Facebook OAuth-omdirigeringen.

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## Konfigurerar &quot;Skicka till&quot;-providers {#section_rdk_dpl_b1b}

Som standard visas Facebook-, LinkedIn- och Twitter-knapparna &quot;Post to&quot; i Livefyre Core-program. Använd parametern postToButtons för att konfigurera vilka providers som ska visas när du bäddar in Livefyre-appen.

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` är en array med en delmängd av följande alternativ:

* tw: Twitter
* fb: Facebook
* li: linkedIn
