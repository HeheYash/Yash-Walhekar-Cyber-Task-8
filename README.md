# Yash-Walhekar-Cyber-Task-8

# Elevate Labs Cybersecurity Internship - Task 8

## 🛡️ Task 8: VPN Setup and Analysis

This repository contains the submission for Task 8 of the Elevate Labs Cybersecurity Internship. The objective of this task was to understand the role of Virtual Private Networks (VPNs) in protecting privacy and securing online communication.

### Tools Used
* **VPN Client:** ProtonVPN (Free Tier)
* **Verification:** `whatismyipaddress.com`

## Part 1: VPN Setup and Verification Process

The core of the task was to install a VPN, connect to a server, and verify that my public IP address had been successfully masked.

### Step 1. Baseline IP Address (VPN Disconnected)

Before activating the VPN, I established my baseline IP address. The ProtonVPN client correctly identified my real IP and location, and this was confirmed by visiting `whatismyipaddress.com`.

* **Original IP:** `My_IP_Address`
* **Location:** Mumbai, India

![My IP address before connecting to the VPN](<./Before VPN.png>)
![ProtonVPN client showing my real IP before connection](<./ProtonVPN Disconnected.jpg>)

### Step 2: VPN Connection (VPN Activated)

I then connected to the "Fastest free server" on ProtonVPN, which assigned me a server in the Netherlands. The client application confirmed a successful and protected connection.

* **New IP:** `185.132.132.203`
* **Location:** Netherlands

![ProtonVPN client showing a successful connection to a Netherlands server](<./ProtonVPN Connected.jpg>)

### Step 3: IP Address Verification

After the VPN connection was established, I refreshed `whatismyipaddress.com` to verify the change. The website confirmed that my public IP address was now the one assigned by the VPN server, and my location was masked as Naaldwijk, Netherlands.

![Verifying the new IP address after connecting to the VPN](<./After VPN.png>)

## Part 2. VPN Benefits and Limitations

### Benefits of Using a VPN
* **Privacy:** Masks your real IP address, preventing websites and online services from tracking your physical location.
* **Security:** Encrypts all your internet traffic, making it unreadable to anyone trying to intercept it (like attackers on public Wi-Fi or your own ISP).
* **Bypass Censorship:** Allows access to websites and content that may be blocked in your geographic region by routing your traffic through a server in another country.

### Limitations of a VPN
* **Speed Reduction:** The process of encrypting and routing your traffic through a remote server almost always results in a loss of internet speed.
* **Trust in the Provider:** A VPN protects you from your ISP, but you must trust the VPN provider. A VPN with a poor "no-logs" policy could still record and expose your activity.
* **Not Complete Anonymity:** A VPN does not make you 100% anonymous. You can still be tracked by browser cookies, device fingerprinting, or by logging into personal accounts (like Google or Facebook).

---

## Part 3: Research on VPN Encryption & Privacy Features

This section details the core technologies that make a VPN a powerful tool for privacy and security.

### 1. VPN Encryption

Encryption is the process of scrambling your internet data, making it an unreadable code to anyone who might intercept it, such as your ISP or hackers.

#### The Encryption Standard: AES-256

* The industry-gold standard for security is the **Advanced Encryption Standard (AES)**.
* VPNs almost always use **AES-256**, which refers to the 256-bit key size.
* This is a symmetric-key algorithm, meaning the same key is used to encrypt and decrypt the data.
* A 256-bit key has $2^{256}$ possible combinations, a number so large that it is considered practically unbreakable by modern computers. It's the same encryption standard trusted by governments and financial institutions to protect classified information.

#### The "Tunnel": VPN Protocols

Encryption needs a **tunneling protocol** to create a secure and stable connection (the "tunnel") between your device and the VPN server. The protocol is the set of rules that builds this tunnel and applies the encryption.

| Protocol | Key Characteristics |
| :--- | :--- |
| **OpenVPN** | **Best All-Rounder:** Highly secure, flexible, and open-source. It's an industry standard and is excellent at bypassing firewalls because it can be configured to run on common ports (like TCP port 443, which regular HTTPS traffic uses). |
| **WireGuard** | **Fastest Speed:** A modern, lightweight protocol with a simple codebase, making it easier to audit. It is extremely fast, making it ideal for streaming, gaming, and large downloads. |
| **IKEv2/IPsec** | **Best for Mobile:** Stands for "Internet Key Exchange version 2". It is known for its speed and, most importantly, its stability. It is excellent at re-establishing a connection if you switch networks (e.g., moving from Wi-Fi to cellular data), making it a top choice for mobile devices. |

### 2. Key Privacy Features

While encryption protects your *data*, these features protect your *identity*.

* **IP Address Masking:** This is the most fundamental feature. The VPN hides your real IP address and replaces it with the IP address of the VPN server, protecting your location and identity.
* **No-Logs Policy:** This is a crucial promise from the VPN provider that they **do not collect or store** any information about your online activity, such as websites visited, files downloaded, or connection timestamps. This means they have no data to share with authorities or for hackers to steal. The most trustworthy VPNs have this policy verified by independent, third-party audits.
* **VPN Kill Switch:** This is a critical safety feature. If your VPN connection unexpectedly drops, the kill switch automatically **blocks your device from accessing the internet**. This prevents your real IP address and unencrypted data from being accidentally exposed.
* **Split Tunneling:** This feature allows you to choose which apps or websites use the VPN tunnel and which connect to the internet directly. This is useful for balancing security with speed for low-risk applications (e.g., letting a streaming app connect directly while your browser remains secured).
* **DNS Leak Protection:** When you type a website, your computer asks a DNS server to find its IP. A DNS leak happens when this request bypasses the VPN. Secure VPNs prevent this by forcing all DNS requests through their own encrypted tunnel, ensuring your ISP cannot see your browsing activity.
