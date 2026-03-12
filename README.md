# Foundations_Lab_Final

**Student Name:** Christopher Diaz  
**Course:** Cybersecurity Foundations Intensive: Night 4  
**Date:** February 26, 2026  
**Instructor:** George Robbins  

---

## Technical Overview
### Professional Introduction
Hello, my name is Christopher Diaz, and I am a Cybersecurity Fellow at The Knowledge House. I am currently building foundational skills in cybersecurity, including threat detection, incident response, and security operations. Through this project, I aim to apply what I’ve learned in a practical setting while continuing to strengthen my analytical and technical abilities. I am passionate about protecting systems and helping organizations improve their security posture.

### Cybersecurity Focus: 2026 Ecosystem
In the evolving 2026 cybersecurity ecosystem, organizations face increasingly sophisticated threats driven by artificial intelligence, cloud adoption, and expanding attack surfaces (World Economic Forum, 2024). The implementation of zero-trust architecture and continuous monitoring has become essential for reducing organizational risk and improving resilience (National Institute of Standards and Technology [NIST], 2023).

My focus is on integrating Security by Design principles within cloud-native environments while leveraging threat detection and governance frameworks to strengthen incident response readiness and minimize vulnerabilities.

---

## Security Foundations: Governance & Frameworks

### Governance Reflection: The Strategic Compass
While technical skill provides the "how" of cybersecurity, governance provides the "why" and "when," ensuring that security measures are not just functional but also legally and strategically sound. According to the **NIST CSF 2.0**, the **Govern (GV)** function serves as the baseline that informs all other technical activities, from **Identity Management (AAA)** to incident response (NIST, 2024). Without governance, technical configurations often lead to "security silos" where tools are deployed without addressing the organization's specific risk appetite or compliance obligations. Furthermore, governance establishes the framework for **Non-repudiation** through strict accounting and immutable logging, which is a legal necessity that technical skill alone cannot satisfy. Ultimately, technical skills are the tools in the belt, but governance is the architectural blueprint that ensures the entire structure is resilient against modern threats like ransomware.

### The CIA Triad Mapping
* **Confidentiality:** Ensuring data is only accessible to authorized parties.
    * *Real-world failure:* A misconfigured S3 bucket leaking PII.
* **Integrity:** Guarding against improper information modification or destruction.
    * *Real-world failure:* An attacker altering financial records or system logs.
* **Availability:** Ensuring timely and reliable access to information.
    * *Real-world failure:* A ransomware attack that encrypts a local VM, making it unusable.



### AAA Framework & Identity Management
* **Authentication:** Verifying who you are (e.g., Phishing-Resistant MFA).
* **Authorization:** Determining what you are allowed to do (e.g., Principle of Least Privilege).
* **Accounting:** Tracking user actions to establish **Non-repudiation**—the legal certainty that a specific user performed a specific action, backed by immutable logs.


# Lab Infrastructure & Virtualization Setup
* **Hypervisor:** The software layer (like VirtualBox) that creates and runs virtual machines by isolating the hardware from the operating system.
* **Virtual Machine (VM):** A digital version of a physical computer that runs on a hypervisor, using a portion of the host’s CPU, memory, and storage.
* **Isolation:** In cybersecurity, isolation ensures that if a VM is compromised or crashes, the "blast radius" is contained, and the Host OS (Windows) remains safe.

## Security Philosophy
In this lab, the deployment of a virtualized Linux environment serves as a practical application of the CIA Triad, bolstered by the principle of isolation. By using a Type-2 Hypervisor (VirtualBox), I have created a sandbox that separates the guest Ubuntu Server from my Windows host. This isolation is a fundamental security control that prevents "guest-to-host" escapes, ensuring that any testing or malicious activity within the VM does not compromise the primary system (National Institute of Standards and Technology [NIST], 2023).

I have mapped my lab environment to the CIA Triad as follows:

* **Confidentiality**: Through the use of VirtualBox's internal networking and Host-Only Adapters, data remains isolated within the virtual segment. This ensures that sensitive configuration files, like my `.env` or audit logs, are not exposed to the public internet or unauthorized users on the local network.
* **Integrity**: Virtualization provides the ability to use snapshots and immutable logging scripts. By running the `lab_verify.sh` script, I establish a baseline of system health. This aligns with governance frameworks that require non-repudiation and the detection of unauthorized changes to ensure the data remains accurate and trustworthy (NIST, 2024).
* **Availability**: By allocating specific CPU and RAM resources to the Ubuntu VM, I ensure that the infrastructure remains responsive. Virtualization allows for rapid recovery; if the server fails, it can be redeployed or restored from a backup without affecting the availability of the host machine.

Building this isolated environment is essential for secure experimentation, as it allows for the simulation of network attacks and defense strategies within a controlled "blast radius"

## Reflection
Isolation is critical when testing software or malware because it prevents malicious code from 'escaping' the test environment and infecting the host machine or the wider network. Virtualization supports secure experimentation by allowing us to create sandboxed environments where we can fail safely without permanent hardware damage. Today’s material aligns most closely with the Cloud Security and Network Security domains. Building virtualized infrastructure is the foundation of cloud computing, while configuring adapters and Packet Tracer topologies addresses network defense. Mastering these tools allows a professional to simulate complex attacks and defenses in a controlled space.

---

## References

Center for Internet Security. (2024). *CIS Controls version 8.1.*  
https://www.cisecurity.org/controls/v8-1

National Institute of Standards and Technology. (2023). *Zero trust architecture (SP 800-207).*  
https://doi.org/10.6028/NIST.SP.800-207

National Institute of Standards and Technology. (2024). *The NIST cybersecurity framework (CSF) 2.0.*  
https://doi.org/10.6028/NIST.ITL.2024.01

World Economic Forum. (2024). *Global cybersecurity outlook 2024.*  
https://www.weforum.org/reports/global-cybersecurity-outlook-2024
