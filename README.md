# FUTURE_CS_01

# Vulnerability Assessment Report 

**Task:** Future Interns — Cyber Security Task 1 (2026)
**Type:** Read-only, passive vulnerability assessment

## Website Tested
- URL: `http://testphp.vulnweb.com/` *(replace with your actual target — see note below)*
- Nature of target: [e.g. "Acunetix's public intentionally-vulnerable demo site, provided for security testing practice" / "my own personal portfolio site"]

## Scope
**In scope (performed):**
- Public-facing pages only
- Passive scanning (OWASP ZAP passive mode)
- HTTP response header analysis
- Basic Nmap port/service enumeration
- Browser DevTools inspection (headers, cookies, mixed content)

**Out of scope (NOT performed):**
- Login bypass
- Exploitation of any vulnerability
- Brute-force attacks
- Denial-of-Service (DoS) testing
- Any action that could disrupt or damage the site

## Tools Used
| Tool | Purpose |
|---|---|
| Nmap | Port and exposed-service enumeration |
| OWASP ZAP (Passive Scan) | Header/config vulnerability identification without attack traffic |
| Browser DevTools | Header, cookie, and mixed-content inspection |
| curl -I | Raw HTTP header capture |
| Canva | Report layout/design (source: `Vulnerability_Assessment_Report.docx` / `.pdf` in this repo) |



## Summary of Findings
| # | Finding | Risk |
|---|---|---|
| 1 | Missing security response headers (CSP, X-Frame-Options, HSTS) | Medium |
| 2 | Outdated/version-disclosing server banner | Medium |
| 3 | Verbose error messages / information disclosure | High |
| 4 | Directory listing enabled | Low |
| 5 | Cookies missing Secure/HttpOnly flags | Medium |


## Disclaimer
This assessment was conducted for educational purposes under a strictly passive, read-only scope. No exploitation or intrusive testing was performed. If testing a site you do not own, confirm it is explicitly designated for security-testing practice (e.g. Acunetix's `vulnweb.com` demo sites) or that you have written authorization.

## Author

THOTA JANAKI RAMA KRISHNAMA NAIDU — Cyber Security Track, Future Interns
