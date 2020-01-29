# LandingNet
Azure Web App (IIS) rules to filter out noise traffic from scriptkiddies and their tools. This is essentially a "poor man's WAF" for your dev server if you (like myself) are annoyed by the weird people who are skewing your usage stats or testing by relentlessly trying to retrieve /bitcoin/wallet.dat from your server. If you'd like to hang up on these requests instead of rewriting to stub, use:

```xml
<action type="AbortRequest" />
```

**WARNING** If you're running Wordpress, Magento, Joomla, Drupal or phpMyAdmin, this config may break them as we're blocking access to things like /wp-login, PMA-specific CSS and other stuff that is publicly served and security researches are probing for. 

# License
Since this is a set of configuration settings and not software (code), I'm not even sure if I should say this specifically - but this is distributed under the most permissive license known to me - MIT license. Feel free to do whatever you want with these rules.

