# Security Policy

## Supported Versions

Only the latest `main` branch is actively supported with security updates.

## Reporting a Vulnerability

AI Destroyer is a 100% local, client-side application. No data is ever transmitted to a server. 

However, if you discover a security vulnerability that could lead to local exploitation (e.g., malicious image parsing leading to XSS), please DO NOT open a public issue. 

Instead, please report it privately by contacting me through GitHub. I will do my best to address it promptly.

### Local Privacy Guarantee
Since this tool runs entirely within Web Workers and the browser's sandbox without external network requests, the attack surface is minimal by design. We are committed to keeping it this way.
