# Phishing Incident Investigation Report

## Incident Overview

A phishing email impersonating PayPal support services was investigated in a controlled lab environment to identify malicious indicators, spoofed infrastructure, and email authentication weaknesses.

The investigation focused on identifying:

* Suspicious sender behavior
* Domain spoofing techniques
* Email authentication failures
* Potential Indicators of Compromise (IOCs)
* Social engineering tactics

---

# Investigation Summary

The phishing email attempted to impersonate a legitimate PayPal communication using a deceptive sender domain designed to appear trustworthy to recipients.

During analysis, the following suspicious indicators were identified:

* Spoofed sender domain
* Missing DMARC policy
* Invalid MX records
* Weak SPF configuration
* Suspicious DNS behavior
* Social engineering language

The email encouraged users to take urgent action, a common phishing tactic used to pressure victims into clicking malicious links or revealing credentials.

---

# Threat Indicators Identified

| Indicator Type       | Value               |
| -------------------- | ------------------- |
| Suspicious Domain    | paypal-accounts.com |
| Attack Type          | Phishing            |
| Technique            | Domain Spoofing     |
| Email Authentication | SPF Failure         |
| Email Authentication | Missing DMARC       |
| Risk Level           | High                |

---

# Technical Findings

## Domain Analysis

The suspicious domain was analyzed using DNS and email security validation tools.

### Findings

* No valid DMARC policy configured
* Missing or invalid MX records
* SPF configuration weaknesses detected
* Suspicious domain infrastructure behavior

These findings suggest the domain may have been configured for phishing or malicious email delivery purposes.

---

## Email Authentication Analysis

The investigation identified multiple authentication failures.

### Authentication Issues

* SPF validation failed
* DMARC policy missing
* Potential sender spoofing detected

Improper email authentication significantly increases the risk of phishing attacks and email impersonation.

---

## Social Engineering Indicators

The phishing message used common psychological manipulation tactics:

* Urgency
* Fear-based language
* Brand impersonation
* Credential harvesting attempts

These tactics are commonly used to deceive users into interacting with malicious content.

---

# Indicators of Compromise (IOCs)

| Type              | Indicator           |
| ----------------- | ------------------- |
| Domain            | paypal-accounts.com |
| Threat Category   | Phishing            |
| Technique         | Social Engineering  |
| Security Weakness | Missing DMARC       |
| Security Weakness | Invalid MX Records  |

---

# MITRE ATT&CK Mapping

| Technique ID | Technique                 |
| ------------ | ------------------------- |
| T1566.001    | Spearphishing Attachment  |
| T1583        | Acquire Infrastructure    |
| T1584        | Compromise Infrastructure |
| T1598        | Phishing for Information  |

---

# Security Recommendations

* Implement SPF, DKIM, and DMARC policies
* Deploy secure email gateway protections
* Block suspicious domains and indicators
* Conduct phishing awareness training
* Monitor email authentication failures
* Integrate phishing indicators into SIEM platforms

---

# Key Learnings

* Email authentication mechanisms are critical for phishing prevention
* Domain spoofing remains a common phishing technique
* IOC extraction supports incident response workflows
* Threat intelligence improves phishing detection capabilities
* Social engineering remains a major attack vector

---

# Conclusion

This phishing investigation demonstrated how attackers exploit weak email authentication and user trust to conduct phishing campaigns. The analysis highlighted the importance of domain validation, email security controls, and defensive monitoring practices within SOC environments.

The project also reinforced practical skills in phishing investigation, IOC extraction, threat analysis, and security documentation relevant to entry-level SOC and Blue Team roles.
