# Yash-Walhekar-Cyber-Task-8

# Elevate Labs Cybersecurity Internship - Task 8

## 🛡️ Task 8: VPN Setup and Analysis

This repository is a submission to the task 8 of the Elevate Labs Cybersecurity Internship. This task was aimed at knowing how Virtual Private Networks (VPNs) may be used to preserve privacy and ensure the safety of online communication.

### Tools Used
* **VPN Client:** ProtonVPN (Free Tier)
* **Verification:** `whatismyipaddress.com`

## Part 1: VPN Setup and Verification Process

The essence of the assignment was to install a VPN, connect to a server, and ensure that my public IP address has been masked.

### Step 1. Baseline IP Address (VPN Disconnected)

I obtained my baseline IP address before I had to activate the VPN. The ProtonVPN client was able to correctly identify my actual IP and location and this was verified by going to `whatismyipaddress.com`.

* **Original IP:** `My_IP_Address`
* **Location:** Mumbai, India

![My IP address before connecting to the VPN](Before%20VPN.png)
![ProtonVPN client showing my real IP before connection](ProtonVPN%20Disconnected.png)

### Step 2: VPN Connection (VPN Activated)

Next I used ProtonVPN, the result was that I was assigned to the **Fastest free server**, and my assigned server was the Netherlands. A successful and secure connection was proven by the client application.

* **New IP:** `185.132.132.203`
* **Location:** Netherlands

![ProtonVPN client showing a successful connection to a Netherlands server](ProtonVPN%20Connected.png)

### Step 3: IP Address Verification

Once the connection with VPN was made, I opened `whatismyipaddress.com` to check the change. The site verified that the new public IP address of my computer was that of the VPN server and the location was hidden as Naaldwijk, Netherlands.

![Verifying the new IP address after connecting to the VPN](After%20VPN.png)

## Part 2. VPN Benefits and Limitations

### Benefits of Using a VPN
* **Privacy:** Hides your IP address, so that sites and internet services will not be able to monitor your physical location.
* **Security:** Secures every internet traffic, and no one will be able to read it (including hackers on unsecured Wi-Fi or your internet provider).
* **Bypass Censorship:** Gives you the freedom to access websites and materials that could be blocked on your geographic region by directing your traffic to a server in another country.

### Limitations of a VPN
* **Speed Reduction:** Internet speed will be reduced nearly every time you crypt and route your traffic across a remote server.
* **Trust in the Provider:** VPN will guard you against your ISP, though you will have to put your trust into VPN provider. Even the VPN company that has a pathetic no-logs policy might track and reveal your browsing history.
* **Not Complete Anonymity:** VPN is not going to make you entirely anonymous. There is still the ability to trace you using browser cookies, device fingerprinting or even with the use of personal accounts (such as Google or Facebook)

---

## Part 3: VPN Encryption and Privacy Features Studies.

In this section, the main technologies that can make a VPN effective privacy and security tool will be described.

### 1. VPN Encryption

Encryption is the art of scrambling your data on the internet, it is a coded message that no one can read it, even somebody hacking in to intercept your data, like your ISP, or a hacker.

#### The Encryption Standard: AES-256

* The security standard used in the industry is the **Advanced Encryption Standard (AES)**.
* VPN typically virtually always relies on the **AES-256**, meaning the key size of 256.
* It is a symmetric-key algorithm, i.e. the key is the same one that is on which the data is encrypted and decrypted.
* The number of combinations of a key of 256 bits is $2^{256}$, a rather big number, which can hardly be broken by a modern computer. It is the same encryption standard that is relied on by governments and financial institutions to keep information classified.

#### The "Tunnel": VPN Protocols

To establish a secure and stable connection (the "tunnel" is what is needed here) between your device and the VPN server, encryption requires a **tunneling protocol**. The protocol is that code of rules which constructs this tunnel and executes the encryption.

| Protocol | Key Characteristics |
| :--- | :--- |
| **OpenVPN** | **Best All-Rounder:** Extremely secure, adaptable and open-source. It is a common industry standard and is very effective in beating firewalls since it can be set to operate on the typical ports (such as TCP port 443, which is used by typical traffic on the HTTPS). |
| **WireGuard** | **Fastest Speed:** A lightweight and modern protocol featuring simple codebase, therefore simpler to audit. It is very high in speed and therefore suited in streaming, playing games and downloading large files. |
| **IKEv2/IPsec** | **Best for Mobile:** Abbreviation of "Internet Key Exchange version 2. It has a reputation of being fast and most importantly stable. It also does a great job though in restoring connection in case you change network (say switching Wi-Fi on cellular or vice versa) which makes it one of the best options in mobile devices. |

### 2. Key Privacy Features

While encryption protects your *data*, these features protect your *identity*.

* **IP Address Masking:** This is the most basic characteristic. The VPN conceals your actual IP address and substitutes it with the IP address of the VPN server keeping your location and identity secret.
* **No-Logs Policy:** This is one of the critical assurances of the VPN provider that they **do not gather or maintain** any data on information concerning your online activity like websites accessed, files downloaded, or connection time-stamps. This implies that they can not provide any data to the authorities or that can be stolen by hackers. The most reliable VPNs already have such a policy checked by independent, third party audits.
* **VPN Kill Switch:** This is a very important safety item. Once your VPN connection suddenly goes dead, the kill switch will travel into effect barricading your equipment to the online environment. This will **not leave your true IP-address and un-ciphered information accidentally exposed**.
* **Split Tunneling:** There is an option to select which applications or websites go through the VPN tunnel and which go straight to the internet. This can be handy to trade security against speed on low risk applications (ex: allowing a streaming application to bypass your browser as your browser remains secure).
* **DNS Leak Protection:** When you enter a Web address, a DNS server requests your computer to locate the IP of the Web address. In the event this request is not met by VPN, it results in a DNS leak. The secure VPNs can stop this by redirecting all your DNS traffic through their encrypted tunnel so that your ISP will not be able to monitor your browsing history.
