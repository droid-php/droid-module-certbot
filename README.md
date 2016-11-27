# Droid Module: droid/certbot

Install SSL certificates using certbot.
For more information on Droid, please see [droidphp.com](http://droidphp.com).

The steps involved are:-

1. Install the certbot-auto package.
2. Run certbot-auto for all `module_certbot_domains`.
   `/etc/nginx/conf.d/`.

## Assumptions

1. The platform is Debian-based.
2. Each of the virtual hosts is running on each of the upstream servers.


## Limitations

1. As there are no apt packages for certbot, wget is used to download certbot-auto on each run.

## Information required by the module

* module_certbot_email: the email address used to run certbot --email
* module_certbot_domains: array with keys `name` (domain name itself) and `server` (apache or nginx) 
