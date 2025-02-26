  # Updated Evilginx3 Phishlets
  
I've dedicated substantial time and effort to create and update new phishlets for Evilginx3. 
In this repository, you'll find many custom Evilginx phishlets, finely crafted and updated to suit real-world applications.

## Want to Learn How to Create Advanced Phishlets from Scratch in 2025?

## Our New Training Course [Evilginx Phishlet Developer Masterclass (2025)](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass) has been released!

![PRO - Evilginx Phishlet Developer Masterclass Main Cover Art - min](https://github.com/user-attachments/assets/865f4bb4-648a-43a6-bb04-5da479e80710)


After months of dedicated work and relentless refinement, our team proud to announce that our **Evilginx Phishlet Developer Masterclass (2025)** has finally been completed. This course is the culmination of years of advanced research and practical red team experience—designed for developers, security professionals, red teamers and anyone who wants to learn how to build custom phishlets from scratch.

Join us now and unlock the most complete, up-to-date resource for mastering phishlet creation in 2025. Elevate your offensive security skills with hands-on labs, expert insights, and innovative techniques that will redefine your approach to reverse-proxy phishing.

[Click Here to View the Course](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass)

![SimplerHacking Student Poll Updated - Phishlet Mastery](https://github.com/user-attachments/assets/10c14fc5-5fbf-4543-9451-5210556b004f)

![Github - Evilginx Workflow Test](https://github.com/user-attachments/assets/7b7e467d-9d48-4ead-9319-13fa2d05c26f)

Are you a programmer, cybersecurity enthusiast, or a red/blue team member ready to move beyond basic Evilginx setup? This course is built for those who want to get hands-on with advanced phishlet development—from the ground up. Whether you're an entry-level developer eager to learn the ins and outs of reverse-proxy phishing or an experienced security professional looking to refine your skills, this masterclass will take you step-by-step through building and customizing phishlets that work in real-world engagements.

![Simpler Hacking Phishlet Mastery (2025)-min](https://github.com/user-attachments/assets/191866aa-d15b-48f1-b18e-f374f99cf625)

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

Evilginx Phishlet Developer Masterclass (2025) isn’t just another security course—it’s the ultimate resource for anyone serious about advanced phishlet development. Elevate your skills, learn to build custom, resilient phishlets.

# Curriculum Previews:
![MITM Phishing Nexus Mods with Evilginx by Simpler Hacking](https://github.com/user-attachments/assets/d3e67abf-50d5-47d4-bb4e-6cd9c73a5254)

![Evilginx vs CAPTCHAS + Real Puppeteer aka EvilPuppet Integration for Evilginx Pro](https://github.com/user-attachments/assets/d5ff3bd9-430c-4a29-9ed0-aec96480bbfa)

![MFA Attacks Preview - Snapshot 2](https://github.com/user-attachments/assets/f74fc110-9ac6-4d4c-9275-383e14ac1077)

![IG Phishlet Lab - DevTooling Instagram With Hussain (Edited, Cropped, Cleaned) - frame at 13m36s](https://github.com/user-attachments/assets/b5d7ba6b-0312-431c-9350-0257bb341bd9)

![EVILGOPHISH MASTERY COURSE CURRICULUM PREVIEW PT 1](https://github.com/user-attachments/assets/cb0d1c33-5b5b-4b4f-9a08-40091aba55d3)


## Click [HERE](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass) to enroll in Evilginx Phishlet Developer Masterclass (2025)

Our **Evilginx Phishlet Developer Masterclass (2025)** is for advanced practitioners, penetration testers, red teamers, and cybersecurity professionals who demand a deeper, more technical understanding of phishlet creation in 2025.

In this masterclass, you will:
- **Dissect Phishlet Architecture:** Gain an intimate understanding of Evilginx phishlets—from proxy host configuration and dynamic sub-filters to capturing critical session cookies and authentication tokens.
- **Tackle Real-World Challenges:** Learn to overcome, diagnose, and troubleshoot complex authentication flows and hurdles with cutting-edge techniques, ensuring your phishlets work seamlessly in real environments and applications.
- **Build Custom Solutions:** Transition from using off-the-shelf phishlets to engineering bespoke tools that are robust, adaptable, and tailored for your red team engagements.
- **Engage with Practical Labs:** Work through hands-on exercises and interactive labs that mirror actual offensive operations, equipping you with skills you can deploy immediately.

![Phishlet Developer Course Preview - Course Components   Disciplines - frame at 0m1s](https://github.com/user-attachments/assets/06a65370-8c9b-48bc-ab34-cfe1422b17b1)

Click [HERE](https://www.simplerhacking.com/pages/evilginx-phishlet-creation-masterclass) to explore the full curriculum and enroll in our extensive course.

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

### Enroll in our free training lessons & webinars: www.simplerhacking.com/courses

## Community Discord Server

![Discord Members](https://img.shields.io/badge/Discord%20Members-1134-blue)


[![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/Wxjpp2EPMF)

## Disclaimer
The tools here are intended solely for legal and ethical use by cybersecurity professionals in controlled environments. 
Any illegal or malicious use is strictly prohibited.
I disclaim all responsibility for any harm, loss, or damage that may arise from improper use.
