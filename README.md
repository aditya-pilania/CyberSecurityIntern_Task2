# Phishing Email Analysis – Cybersecurity Internship Task2

This repositorycontains a practical analysis of **phishing email samples**, including:
- A **spoofed email** that imitates ICICI Bank.
- A **legitimate-looking email** with no malicious traits.

The purpose of this task is to understand how phishing emails are structured and how we can analyze their **content and headers** to detect threats.

0---

## Key Concepts That Is Important To Know

### What is Phishing?
Phishing is a type of cyberattack in which an attacker poses as a trustworthy entity to trick individuals into revealing sensitive information like passwords, credit card numbers, or OTPs. It usually comes via emails, SMS, or fake websites.

### What is Email Spoofing?
Email spoofing is a technique used by attackers to forge the sender's address in an email, making it look like it’s coming from a trusted source when it’s not. This tricks the recipient into trusting the message.

### What is an Email Header?
An email header is a hidden metadata section of an email that contains technical details such as:
- Sender and receiver addresses
- Sending server info (IP, domain)
- Authentication results (SPF, DKIM, DMARC)
- Routing information (Received lines)

## Tools Used

- Handcrafted phishing and legit email samples
- Google Admin Toolbox – [Google Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/)
- Markdown editor for documentation

## Steps Followed

1. Copied two email samples:
   - One **spoofed** (phishing)
   - One **legit** (safe)
3. Analyzed header fields to detect spoofing, suspicious IPs, reply-to mismatches, etc.

### How I Analyzed an Email Header?
With the help of Phishing Email Samples I was able to get two emails with a email header and its content. Copied and Pasted it into a email head analyzer tool like [Google Header Analyzer](https://toolbox.googleapps.com/apps/messageheader/). 
Then I Checked for:
   - Return-Path mismatches
   - Unauthorized sending IPs
   - Failed SPF/DKIM checks
   - Suspicious `Reply-To` addresses

4. Summarized findings in the analysis report.

## Files Included

| File Name | Description |
|-----------|-------------|
| `phishing_email.txt` | Fake phishing email pretending to be ICICI Bank |
| `phishing_header.txt` | Header of spoofed email |
| `same_email.txt` | Clean, legitimate-looking email |
| `safe_header.txt` | Header of legit email |
| `phishing_analysis_report.md` | Detailed report on spoofed email analysis |
| `README.md` | This file – full documentation of the project |

---

## What I Learned?

This task helped build a practical skills in:
- Spotting phishing and spoofed emails
- Analyzing email headers
- Understanding how attackers try to manipulate user trust

