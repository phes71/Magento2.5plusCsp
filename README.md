# Magento2.5plusCsp
Magento 2 Csp - Content Security Policies
https://devdocs.magento.com/guides/v2.4/extension-dev-guide/security/content-security-policies.html

From Magento 2.3.5 onwards a new module as been added to mitigate against Cross Site Scripting (XSS) and related attacks, including card skimmers, session hijacking, clickjacking, and more. Web servers send CSPs in response HTTP headers (namely Content-Security-Policy and Content-Security-Policy-Report-Only) 

This module allows you to white list your external scripts, fonts, css and iframes to stop console warning such as :-
Report Only] Refused to load the script 'https://widget.trustpilot.com/bootstrap/v5/tp.widget.bootstrap.min.js' because it violates the following Content Security Policy

Install this module then edit the csp/etc/csp_whitelist.xml 

example to allow the Trustpilot iframe widget for reviews use the following

<policy id="frame-src">
           <values>
                <value id="widget.twitter.com" type="host">*.trustpilot.com</value>
            </values>
        </policy>
