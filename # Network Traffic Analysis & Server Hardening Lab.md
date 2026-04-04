## 📌 Overview
This repository documents a practical cybersecurity lab focused on network protocol analysis and web server hardening. Using **Wireshark** for packet interception and an **Apache** HTTP Server for configuration testing, this project demonstrates the vulnerabilities of unencrypted traffic and the importance of secure server deployments to prevent information disclosure.

## 🛠️ Tools & Technologies Used
* **Wireshark:** Deep-dive packet capture and protocol analysis.
* **Apache HTTP Server:** Local deployment for configuration and security hardening.
* **Target Environment:** Altoro Mutual (HTTP vulnerability testing site) and local loopback.

## 🎯 Lab Objectives & Practical Execution

### 1. Packet Interception & Credential Harvesting (Wireshark)
* Captured live network traffic navigating to the Altoro Mutual testing website over standard HTTP.
* Analyzed the TCP three-way handshake and subsequent HTTP requests.
* **Key Finding:** Successfully intercepted HTTP POST requests and extracted unencrypted login credentials transmitted in cleartext. This practically demonstrated the critical vulnerability of utilizing non-HTTPS communications for sensitive data.

### 2. Web Server Security Configuration (Apache)
* Deployed and configured a local Apache web server.
* Audited default configurations for potential information leakage.
* **Key Finding:** Implemented strict security settings (modifying directives like `ServerTokens` and `ServerSignature`) to limit the amount of server information—such as OS details and Apache version numbers—displayed to client requests. This step actively mitigates infrastructure footprinting by potential attackers.

## 🚀 Methodology Highlights
* **Traffic Filtering:** Utilized specific Wireshark display filters (e.g., `http.request.method == POST`) to isolate credential submission packets from background network noise quickly.
* **Information Control:** Hardened HTTP response headers and error pages to restrict unauthorized information disclosure to end-users.

## 💡 Learning Outcomes
This lab provided hands-on experience bridging the gap between offensive observation (sniffing unencrypted credentials) and defensive configuration (hardening a web server). Intercepting plaintext credentials in real-time heavily reinforced the absolute necessity of secure encryption protocols, while the Apache configuration highlighted how simple oversights can leak sensitive infrastructure details.
