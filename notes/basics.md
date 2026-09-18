# Cybersecurity Foundation Notes

## 1. Cybersecurity Fundamentals

Cybersecurity is the practice of protecting computers, networks, applications, and data from unauthorized access, attacks, damage, or disruption.

### CIA Triad

The CIA Triad represents three important goals of cybersecurity:

* **Confidentiality** – Ensures that information is accessible only to authorized users.
* **Integrity** – Ensures that information remains accurate and is not modified without authorization.
* **Availability** – Ensures that systems and information are available when required.

### Common Cybersecurity Threats

* **Phishing** – A social engineering technique used to trick users into revealing sensitive information.
* **Malware** – Malicious software designed to damage, disrupt, or gain unauthorized access to systems.
* **DDoS** – An attack that sends a large amount of traffic to a service to make it unavailable.
* **SQL Injection** – An attack that attempts to insert malicious SQL commands into an application's database queries.
* **Brute Force** – Repeatedly trying different passwords or credentials to gain access.
* **Ransomware** – Malware that can encrypt or restrict access to data and demand payment.

### Attack Vectors

An attack vector is a method or path that can be used to gain unauthorized access to a system or network.

Examples include:

* Phishing emails
* Weak passwords
* Vulnerable software
* Malicious files
* Unsecured networks
* Exploitable web applications

---

## 2. Lab Environment

A cybersecurity lab provides an isolated environment where security concepts and tools can be practiced safely.

### Lab Components

* **Kali Linux** – Used as the security testing machine.
* **Metasploitable** – Used as a vulnerable target machine.
* **VirtualBox/VMware** – Used to run the virtual machines.
* **Host-Only Network** – Allows communication between virtual machines in an isolated network.

The lab was used only for educational and authorized security testing.

---

## 3. Linux Fundamentals

Linux is widely used in cybersecurity because of its command-line tools and flexibility.

### Basic Commands

| Command      | Purpose                                 |
| ------------ | --------------------------------------- |
| `pwd`        | Shows the current directory             |
| `ls`         | Lists files and directories             |
| `cd`         | Changes the current directory           |
| `chmod`      | Changes file permissions                |
| `chown`      | Changes file ownership                  |
| `apt`        | Manages software packages               |
| `dpkg`       | Manages Debian packages                 |
| `ifconfig`   | Displays network interface information  |
| `ping`       | Tests network connectivity              |
| `netstat`    | Displays network connections            |
| `traceroute` | Shows the path taken by network packets |

---

## 4. Networking Basics

Networking allows computers and devices to communicate with each other.

### OSI Model

The OSI model consists of seven layers:

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

### TCP/IP Model

The TCP/IP model commonly consists of:

1. Network Access
2. Internet
3. Transport
4. Application

### Important Protocols

* **DNS** – Converts domain names into IP addresses.
* **HTTP** – Protocol used for communication between web browsers and web servers.
* **HTTPS** – Secure version of HTTP that uses encryption.
* **TCP** – Provides reliable communication between devices.
* **IP** – Provides addressing and routing of packets.

### IP Addressing

An IP address identifies a device on a network.

Example:

```text
192.168.128.3
```

In the lab, private IP addresses were used for communication between the virtual machines.

### NAT

Network Address Translation (NAT) allows private IP addresses to communicate with external networks by translating between private and public addresses.

---

## 5. Cryptography Basics

Cryptography is used to protect information by transforming data into a form that unauthorized users cannot easily understand.

### Symmetric Encryption

Symmetric encryption uses the same key for encryption and decryption.

Example:

```text
Plaintext → Encryption → Ciphertext
Ciphertext → Decryption → Plaintext
```

### Asymmetric Encryption

Asymmetric encryption uses a pair of keys:

* Public key
* Private key

The public key can be shared, while the private key should be kept secret.

### Hashing

Hashing converts data into a fixed-length value.

Common hashing algorithms include:

* MD5
* SHA-256

Hashing is generally used for integrity verification and password-related applications rather than reversible encryption.

### Digital Certificates

Digital certificates help verify the identity of websites or other entities and are commonly used with HTTPS.

### SSL/TLS

TLS provides encrypted communication between systems. HTTPS uses TLS to help protect web traffic.

### OpenSSL

OpenSSL is a widely used toolkit that provides functionality related to cryptography and TLS.

---

## 6. Security Tools

### Nmap

Nmap is a network scanning tool used to discover hosts, services, and open ports.

Example:

```bash
nmap 192.168.128.3
```

In the lab, Nmap was used to perform a basic scan of the vulnerable target machine.

### Wireshark

Wireshark is a network protocol analyzer used to capture and examine network packets.

For example, ICMP traffic generated using `ping` can be captured and analyzed in Wireshark.

Example:

```bash
ping -c 4 192.168.128.3
```

The Wireshark display filter:

```text
icmp
```

can be used to view ICMP packets.

### Burp Suite

Burp Suite is a web application security testing platform. It can be used to inspect and analyze HTTP/HTTPS requests and responses.

In the lab, Burp Suite was explored as part of learning basic web security testing.

### Netcat

Netcat is a networking utility that can be used for TCP/UDP communication, connection testing, and other networking tasks.

---

## 7. Practical Learning

During the practical exercises, I:

* Set up a basic cybersecurity lab environment.
* Practiced Linux commands.
* Checked network connectivity using `ping`.
* Performed a basic network scan using Nmap.
* Captured ICMP traffic using Wireshark.
* Explored Burp Suite for web security testing.
* Studied basic networking and cryptography concepts.

All practical testing was performed in a controlled lab environment for educational purposes.
