# HTTP vs HTTPS Analysis

**Veda Technology Cyber Security Internship, Task 16 (Day 16)**
Author: Ritu Raj

## Objective
Compare HTTP and HTTPS and explain the security benefits of TLS (encryption, authentication, integrity).

## Tools Used
- Web browser (Chrome / Firefox)
- Browser Developer Tools (Network and Security tabs)

## Approach
1. Opened an HTTP-only site (neverssl.com) and an HTTPS site (example.com).
2. Compared the address bar indicators ("Not secure" vs padlock).
3. Inspected the TLS certificate (issuer, validity, domain).
4. Used DevTools → Network to compare ports (80 vs 443) and protocols.
5. Used the Security tab to check the TLS version and cipher suite.

## HTTP vs HTTPS Analysis
| Feature | HTTP | HTTPS |
|---|---|---|
| Full form | HyperText Transfer Protocol | HyperText Transfer Protocol Secure |
| Default port | 80 | 443 |
| Encryption | None (plain text) | TLS encrypted |
| Authentication | No server verification | Certificate-based |
| Integrity | Data can be altered | Tampering detected |
| Browser indicator | "Not secure" | Padlock |

## Security Benefits of TLS
- **Encryption:** data is unreadable to anyone sniffing the network.
- **Authentication:** the certificate proves the server's identity and stops fake sites and MITM attacks.
- **Integrity:** any change to data in transit is detected.

## Interview Questions and Answers

### 1. What is HTTPS?
HTTPS (HyperText Transfer Protocol Secure) is HTTP running over TLS. It encrypts the data exchanged between browser and server, verifies the server's identity with a digital certificate, and protects data from being modified in transit. It uses port 443 by default.

### 2. What is TLS?
TLS (Transport Layer Security) is a cryptographic protocol that secures communication over a network. It starts with a handshake where the server is authenticated and both sides agree on a session key. After that, all data is encrypted and integrity-protected. TLS replaced the older SSL, and the current version is TLS 1.3.

### 3. Why is HTTP insecure for sensitive data?
HTTP sends everything in plain text with no encryption, authentication or integrity checks. Anyone on the network path (public Wi-Fi, rogue router, attacker) can read passwords, cookies and card details, impersonate the server, or modify the content. This makes sniffing, man-in-the-middle attacks and session hijacking easy.

## Outcome
HTTP exposes data to sniffing and MITM attacks. HTTPS protects the same traffic with TLS and should be used on every site, together with HSTS and TLS 1.2/1.3.

## Files
- `Task16_HTTP_vs_HTTPS_Report.docx`: full report
