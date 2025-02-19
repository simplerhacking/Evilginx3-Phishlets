  # Updated Evilginx3 Phishlets
  
I've dedicated substantial time and effort to create and update new phishlets for Evilginx3. 
In this repository, you'll find many custom Evilginx phishlets, finely crafted and updated to suit real-world applications.

## Want to Learn More About Creating Advanced Phishlets from Scratch in 2025?

## [Evilginx Phishlet Developer Masterclass (2025)](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass) has been released!

After months of dedicated work and relentless refinement, we're proud to announce that our **Evilginx Phishlet Developer Masterclass (2025)** has finally been completed. This course is the culmination of years of advanced research and practical red team experience—designed for developers, security professionals, red teamers and anyone who wants to learn how to build custom phishlets from scratch.

Join us now and unlock the most complete, up-to-date resource for mastering phishlet creation in 2025. Elevate your offensive security skills with hands-on labs, expert insights, and innovative techniques that will redefine your approach to reverse-proxy phishing.

[Click Herer to View the Course](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass)

![evilginx phishlet developer mastery class by simpler hacking (2025)](https://github.com/user-attachments/assets/aaa0823d-4ebe-4f3c-b78d-974380d373fb)

![SimplerHacking Student Poll Updated - Phishlet Mastery](https://github.com/user-attachments/assets/10c14fc5-5fbf-4543-9451-5210556b004f)

Are you a programmer, cybersecurity enthusiast, or a red/blue team member ready to move beyond basic Evilginx setup? This course is built for those who want to get hands-on with advanced phishlet development—from the ground up. Whether you're an entry-level developer eager to learn the ins and outs of reverse-proxy phishing or an experienced security professional looking to refine your skills, this masterclass will take you step-by-step through building and customizing phishlets that work in real-world engagements.

![Evilginx Mention Landing Page Fade in Out + Logo Github](https://github.com/user-attachments/assets/32ac299b-c2d4-4499-8623-e51bff39744c)


**What You’ll Master in Evilginx Phishlet Developer Masterclass (2025):**

- **Phishlet Architecture Fundamentals:**  
  Learn how Evilginx phishlets are structured, and understand how each section—from proxy_hosts and sub_filters to javascript injection and force_post—works together to capture session data and user credentials.

- **Over 10 Hours of In-Depth Content:**  
  This masterclass features more than 10 hours of content that covers every facet of phishlet development—from foundational principles to advanced customization techniques—ensuring you have all the knowledge and tools you need to create, deploy, and manage custom phishlets from scratch.

- **Token and Cookie Capture Techniques:**  
  Discover the methods used to intercept session cookies and authentication tokens. You’ll learn how to extract critical data using regular expressions and how to set up auth_urls to trigger successful session capture.

- **Real-World Challenges & Phishing Popular Websites:**  
  Work through practical exercises that address modern challenges, including handling multi-factor authentication and CAPTCHA flows. Learn to integrate and manage these hurdles without compromising data capture.

- **Step-by-Step Labs & Interactive Exercises:**  
  Follow detailed, hands-on labs that cover every aspect of phishlet development. By the end of the course, you’ll have built your own advanced phishlets, ready for use in simulated red team engagements.

- **Tailored for Aspiring Phishlet Developers of All Skill Levels:**  
  This course speaks directly to programmers who are ready to master Evilginx phishlet creation—from understanding basic concepts to implementing sophisticated customizations. You'll get clear, code-driven examples and nuanced insights.

Evilginx Phishlet Developer Masterclass (2025) isn’t just another security course—it’s the ultimate resource for anyone serious about advanced phishlet development. Elevate your skills, learn to build custom, resilient phishlets from scratch.

# Curriculum Previews:

## Click [HERE](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass) to enroll in Evilginx Phishlet Developer Masterclass (2025)

## Elevate Your Offensive Security Skillset with Our Latest Advanced Phishing Course!

Are you ready to push your Evilginx expertise to new heights? If you’re already comfortable with deploying basic phishlets, it’s time to master the craft of building them from scratch. Our **Evilginx Phishlet Developer Masterclass (2025)** is engineered for advanced practitioners—penetration testers, red teamers, and cybersecurity professionals—who demand a deeper, more technical understanding of phishlet creation.

In this masterclass, you will:
- **Dissect Phishlet Architecture:** Gain an intimate understanding of Evilginx phishlets—from proxy host configuration and dynamic sub-filters to capturing critical session cookies and authentication tokens.
- **Tackle Real-World Challenges:** Learn to overcome, diagnose, and troubleshoot complex authentication flows and hurdles with cutting-edge techniques, ensuring your phishlets work seamlessly in real environments and applications.
- **Build Custom Solutions:** Transition from using off-the-shelf phishlets to engineering bespoke tools that are robust, adaptable, and tailored for your red team engagements.
- **Engage with Practical Labs:** Work through hands-on exercises and interactive labs that mirror actual offensive operations, equipping you with skills you can deploy immediately.

Join the ranks of industry professionals who have already transformed their approach to reverse-proxy phishing.  
Click [HERE](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass) to explore the full curriculum and enroll in the **Evilginx Phishlet Developer Masterclass 2025** today—and redefine what’s possible in offensive security.

## Need Custom Phishlets? 
Check our constantly updating our free Evilginx3 Phishlet Repository for Red Teams

You can find it here: https://github.com/simplerhacking/Evilginx3-Phishlets

## Questions?
Send us an email to info@simplerhacking.com or message directly on our website www.simplerhacking.com

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

## Follow our academic blog for more insights on security: https://medium.com/@simplerhacking

![Subscribe](https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/05768590-0ad4-47d8-bee0-5e940b71a00b)

## Want more Evilginx Phishlets not available on Github? 
Gain access to more private Phishlets not available to the public on our Patreon.


[![Get Exclusive Access on Patreon](https://img.shields.io/badge/Exclusive_Access-Patreon-orange.svg)](https://www.patreon.com/SimplerHacking)

<img width="264" alt="Patreon" src="https://github.com/simplerhacking/Evilginx3-Phishlets/assets/141525149/3e9d587d-0792-4dad-a6d2-aaa004197508">

## Patreon: www.patreon.com/SimplerHacking


### Enroll in our free training lessons & webinars: www.simplerhacking.com/courses

## Community Discord Server

![Discord Members](https://img.shields.io/badge/Discord%20Members-1036-blue)


[![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/yqfVskRa)

## Disclaimer
The tools here are intended solely for legal and ethical use by cybersecurity professionals in controlled environments. 
Any illegal or malicious use is strictly prohibited.
I disclaim all responsibility for any harm, loss, or damage that may arise from improper use.
