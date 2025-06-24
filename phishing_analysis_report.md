# Phishing Email Analysis Report – for ICICI BANK

This report presents a comparative analysis between a **spoofed phishing email** and a **legitimate email** sample claiming to be from ICICI Bank. The goal is to understand key traits that help detect phishing attempts using **email content inspection** and **header analysis**.

---

## 1. Spoofed Email Summary

**Subject:** Immediate Action Required – ICICI Account Suspension Alert  
**From:** ICICI Bank <secure@icicibank-security.com>  
**Link:** https://icicibank.verify-nowlogin.net  

### What I Observed as Threat Indicators

| Feature | Value | Analysis |
|--------|-------|----------|
| **Sender Domain** | icicibank-security.com | Fake domain trying to mimic real one |
| **Reply-To** | support-verification.info | Different and untrustworthy domain |
| **Urgency** | “Account will be deactivated in 24 hours” | Common social engineering trick |
| **Greeting** | “Dear Customer” | No personalization (generic) |
| **Hyperlink** | verify-nowlogin.net | Mismatched domain, not ICICI |
| **Return-Path** | spoofed domain | Does not match real ICICI servers |
| **SPF/DKIM/DMARC** | Not included | Indicates no authentication |
| **Sending IP** | 192.0.2.24 | Unknown mail server |

### Conclusion for the fake one:
This is a **phishing email**. The sender impersonates ICICI Bank using a fake domain, manipulates the recipient with urgency, and tries to redirect them to a fraudulent website. The email header further confirms it was **not sent by ICICI's infrastructure**.

---

## 2. Legitimate Email Summary

**Subject:** Your ICICI Bank Account Statement is Ready  
**From:** ICICI Bank <noreply@icicibank.com>  
**Link:** https://www.icicibank.com  

### Safe Indicators

| Feature | Value | Analysis |
|--------|-------|----------|
| **Sender Domain** | icicibank.com | Official and verified domain |
| **Reply-To** | Same as sender | No redirection |
| **Greeting** | “Dear Aditya Pilania” | Personalized |
| **Hyperlink** | icicibank.com | Trusted, secure link |
| **Return-Path** | noreply@icicibank.com | Matches sending domain |
| **SPF/DKIM/DMARC** | All passed | Verified as legitimate |
| **Sending IP** | 203.27.235.120 | ICICI’s genuine mail server |
| **Tone** | Informational | No threats, no urgency |

### Conclusion for originial email:
This email is **legitimate**. It comes from ICICI’s real domain, contains a secure link, passes all email authentication checks, and uses personalized, professional language.

---

## Comparative Summary of a Real and Spoof Email

| Factor | Spoofed Email | Legitimate Email |
|--------|---------------|------------------|
| Sender Domain | `icicibank-security.com` | `icicibank.com` |
| Link Domain | `verify-nowlogin.net` | `icicibank.com` |
| Urgency / Threat | Yes | No |
| Personalized? | No | Yes |
| SPF/DKIM/DMARC | Fail / Absent | Pass |
| Header Source | Unknown IP | Known ICICI IP |
| Social Engineering? | Yes | No |

---

By comparing both email types, I learned:
- **Spoofed emails often use similar-looking domains** to trick users.
- **Legit emails are properly authenticated** via SPF/DKIM/DMARC.
- **Urgency and fear** are signs of social engineering.
- **Header analysis** is critical for backend verification.

Always inspect:
- The sender’s domain and reply-to fields.
- Embedded links (hover before clicking).
- Email headers using tools like [Google Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/)

This exercise strengthens our **threat detection** and **email forensics** skills in real-world scenarios.

