# Cloudflare DynDns Updater

## Description
This tool transforms a traditional DNS record into a Dynamic DNS record. Once started, the tool checks if the value of the specified record matches the current external IP of the network. If the IP address does not match the tool will update it.

## Installation

To install on Raspberry PI

```
git clone https://github.com/mdl2021/cloudflare_dyndns/
```

1. Create API Key - Log into Cloudflare
2. Click top right My Profile
3. Click API Tokens in left menu
4. Click Create Token
5. Click Edit Zone DNS (Tempalte)
6. Click On Zone resources select base domain
7. Click Continue to Summary
8. Copy the API Token
9. Open CloudeFlare.py and Create and API token
10. Copy and paste the Curl text into ssh and confirm its working.
11. Goto Websites and click on domain
12. Click on DNS
13. Create a subdomain A record that you will use to access the PI remotely and set the IP to 0.0.0.0 and select DNS only
14. ON the PI run the command.
```
python3 main.py -e <EMAIL> -ak <API_KEY> -d <DOMAIN> -r <DNS_RECORD> -rt <RECORD_TYPE> -i <INTERVAL>
```


## Usage

```
Usage: python3 main.py -e <EMAIL> -ak <API_KEY> -d <DOMAIN> -r <DNS_RECORD> -rt <RECORD_TYPE> -i <INTERVAL>

      -e  cloudflare email address
      -ak cloudFlare apikey
      -d  domain name to be updated eg. test.com
      -r  record to be updated eg. myrecord.test.com
      -rt record type eg. A
      -i  check interval in seconds (minimum is 10s)
```

## Donations

Donate: <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=QF3RUSYRD5XBE&source=url">PayPal</a>
