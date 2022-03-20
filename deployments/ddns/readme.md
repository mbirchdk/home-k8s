# Guide
## step 1) 
Create cloudflare account

## step 2) 
If you haven’t already done so, add an A record to Cloudflare that points to your home network. For now, this can point to any IP, such as 1.1.1.1 because ddclient will update the IP to the correct address when we deploy it later.

## step 3)
Go to templates/ddclient-secret.yaml and change:

zone — your domain name like example.com (not subdomain!) \
login — your Cloudflare account email address \
password — your global API key from under API Tokens on your Cloudflare profile \
the line beneath password — full domain name to keep updated, including subdomain like home.example.com

# FYI
Here’s some other interesting details in the ddclient.conf.

daemon: ddclient will run this process every 300 seconds (five minutes) \
web: dclient will check if the IP address has changed, using this web service: https://domains.google.com/checkip

# source    
https://codeburst.io/ddclient-c9a6ac1d8f81

