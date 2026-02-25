# Foundations_Lab_Final

**Student Name:** Christopher Diaz  
**Course:** Cybersecurity Foundations Intensive: Night 2  
**Date:** February 24, 2026  
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



---

## References

Center for Internet Security. (2024). *CIS Controls Version 8.1*. https://www.cisecurity.org/controls/v8-1

National Institute of Standards and Technology. (2023). *Zero trust architecture* (SP 800-207). https://doi.org/10.6028/NIST.SP.800-207

National Institute of Standards and Technology. (2024). *The NIST Cybersecurity Framework (CSF) 2.0*. https://doi.org/10.6028/NIST.ITL.2024.01

World Economic Forum. (2024). *Global cybersecurity outlook 2024*. https://www.weforum.org/reports/global-cybersecurity-outlook-2024