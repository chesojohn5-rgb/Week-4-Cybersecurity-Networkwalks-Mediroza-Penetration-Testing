# Week-4-Cybersecurity-Networkwalks-Mediroza-Penetration-Testing

# 🔐 Mediroza General Hospital – Penetration Testing Project
**Week 4 Cybersecurity Practical | Batch B084**

Black-box penetration testing, web security assessment and information exposure investigation.

---

## 📌 Project Overview

This project focuses on conducting an authorized penetration test against **Mediroza General Hospital (`medirozahospital.com`)** as part of the Week 4 cybersecurity practical.

The purpose of this assessment was to investigate potential security weaknesses in the hospital's web infrastructure, identify exposed resources, examine possible information disclosure risks and understand how attackers could exploit weaknesses in web applications.

The assessment involved reconnaissance, web directory discovery, login security testing, SQL injection concepts and investigation of publicly accessible files and historical information.

All activities were conducted within the scope of the authorized educational exercise.

## 🎯 Objectives

The main objectives of this project were to:

- Conduct reconnaissance against the target website.
- Identify accessible directories and web resources.
- Discover potentially exposed PDF documents.
- Investigate the exposure of historical database information.
- Examine web application login security.
- Understand SQL injection vulnerabilities and their potential impact.
- Explore password-testing tools and authentication weaknesses.
- Document findings, challenges and possible security improvements.

## 🛡️ Scope of Testing

**Target:** `medirozahospital.com`

**Assessment type:** Black-box penetration testing.

The assessment focused on:

- Website reconnaissance.
- Directory and file discovery.
- Identification of exposed PDF documents.
- Investigation of historical staff and stakeholder information.
- Authentication security testing.
- SQL injection concepts.
- Information disclosure risks.

**Restrictions:** Denial-of-service attacks and activities outside the authorized testing scope were excluded.

## 🧰 Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration-testing operating system |
| VirtualBox | Virtual testing environment |
| Nmap | Network scanning and service discovery |
| Gobuster | Directory and resource discovery |
| Hydra | Authentication security testing |
| SecLists | Username and password wordlists |
| John the Ripper | Password hash auditing |
| Browser Developer Tools | Inspecting web application elements |
| Windows CMD | Initial DNS and network reconnaissance |

## 🔎 Methodology & Activities

### Step 1. Initial Reconnaissance

The assessment began with basic reconnaissance to gather information about the target domain.

The following command was used during initial investigation:

```bash
nslookup medirozahospital.com
```

The purpose was to examine DNS resolution and identify the IP address associated with the target domain.

### Step 2. Web Resource Discovery

Gobuster was explored as a directory and file discovery tool.

The objective was to identify potentially accessible resources and directories that were not immediately visible through normal website navigation.

This stage helped develop an understanding of how exposed directories and files can create information disclosure risks.

### Step 3. PDF Document Discovery

During the assessment, **three PDF files were identified** on the target website.

These documents were recorded as potential information exposure findings because publicly accessible documents may contain information that should not be available to unauthorized visitors.

The documents were treated as evidence requiring further review.

### Step 4. Historical Database Discovery

An old database containing historical staff and stakeholder information was identified during the investigation.

The information of interest included:

- Staff names.
- Email addresses.
- Salary-related information.
- Stakeholder details.

This raised concerns about historical data retention, access controls and the potential exposure of sensitive organizational information.

.

### Step 5. Authentication Security Testing

Authentication security was investigated using Hydra and prepared username and password wordlists from SecLists.

The purpose was to understand how weak authentication mechanisms and predictable credentials can expose user accounts to password-guessing attacks.

The investigation also involved examining login form parameters, identifying the correct submission method and understanding how applications respond to unsuccessful authentication attempts.

### Step 6. SQL Injection Investigation

SQL injection was studied as part of the web application security assessment.

The investigation focused on understanding how improperly handled user input can interfere with database queries.

Particular attention was given to:

- SQL comments.
- Authentication query conditions.
- The use of logical operators.
- How login forms interact with backend databases.

This helped demonstrate why input validation and parameterized database queries are important security controls.

---

## 🐞 Problems Encountered & Solutions

Several technical and conceptual challenges were encountered during the practical.

### Problem 1. Gobuster Installation and Updates

During the installation of Gobuster on Kali Linux, additional updates and dependencies were required.

This initially made it difficult to determine whether the installation had completed successfully.

**Solution:**

The installation and update process was allowed to complete before checking the tool's availability.

### Problem 2. Copying Text from the Kali Terminal

Copying terminal output was initially difficult, making it challenging to share commands and error messages for troubleshooting.

**Solution:**

The terminal output was selected carefully and alternative copying methods were explored.

### Problem 3. Understanding Hydra Login Parameters

While working with Hydra, identifying the correct login form parameters proved challenging.

The investigation involved understanding:

- HTTP POST requests.
- Username and password fields.
- Form submission methods.
- Failure messages returned by the application.

An important lesson was that an incorrect-password response does not automatically prove that a username is valid.

### Problem 4. Identifying the Correct Failure Condition

Hydra requires an appropriate failure condition to distinguish unsuccessful login attempts from potentially successful ones.

Initially, there was confusion about which response message should be used.

**Solution:**

The login response and HTML form behavior were examined to understand how the application communicates unsuccessful authentication attempts.

### Problem 5. Understanding SQL Injection Syntax

There was initial confusion about SQL comment syntax, particularly the difference between `--` and `#`.

**Solution:**

The SQL comment syntax and how comments affect the interpretation of database queries were studied.

This improved understanding of how SQL injection vulnerabilities can arise when applications construct database queries unsafely.

### Problem 6. Kali Linux Virtual Machine Configuration

During preparation for the practical, difficulties were encountered with virtual machine storage, network configuration and snapshot management.

**Solution:**

The Kali Linux environment was investigated and its configuration checked to maintain a usable testing environment.

---

## 💡 What I Learned

Through this project, I developed practical knowledge of penetration testing and web application security.

The most important concepts I learned include:

### 1. Reconnaissance

I learned that penetration testing begins with information gathering.

Reconnaissance helps identify the target's infrastructure and provides useful information for subsequent security assessments.

### 2. Directory and File Discovery

I learned how tools such as Gobuster can help identify directories and files that may not be visible through normal website navigation.

I also understood that improperly protected directories can expose sensitive information.

### 3. Information Disclosure

Discovering three PDF files and historical database information helped me understand the risks associated with exposing organizational documents and outdated records.

Even historical information can create security and privacy risks.

### 4. Authentication Security

I learned how login forms process authentication requests and how tools such as Hydra can be used to assess password security in authorized testing environments.

I also learned why understanding HTTP methods and application response messages is important.

### 5. SQL Injection

I developed a better understanding of how SQL injection works, particularly how SQL comments and logical conditions can affect database queries.

I learned that applications should use parameterized queries rather than directly combining user input with SQL statements.

### 6. Password Security

I learned about password wordlists, password-guessing techniques and the importance of strong passwords.

I also explored the role of John the Ripper in password hash auditing.

### 7. Troubleshooting

I learned that penetration testing involves more than executing commands.

Understanding errors, identifying incorrect parameters and investigating unexpected results are important skills when working with cybersecurity tools.

### 8. Professional Documentation

I learned the importance of documenting testing procedures, evidence, findings, encountered problems and recommended solutions.

A penetration test is not complete without a clear report explaining the results.

---

## 🔐 Security Recommendations

Based on the areas investigated, the following security improvements are recommended:

1. **Access control:** Restrict access to confidential documents and internal resources.
2. **Database protection:** Ensure historical databases are securely stored and inaccessible to unauthorized users.
3. **Data retention:** Review and securely dispose of outdated records that are no longer required.
4. **Authentication:** Implement strong password policies and multi-factor authentication.
5. **SQL injection prevention:** Use parameterized queries and proper input validation.
6. **Directory protection:** Disable unnecessary directory listings and restrict access to sensitive files.
7. **Monitoring:** Monitor authentication attempts and suspicious activity.
8. **Regular security assessments:** Conduct periodic vulnerability assessments and penetration tests.

## 📊 Project Findings Summary

| Finding | Observation | Security Concern |
|---|---|---|
| PDF documents | Three PDF files identified | Potential information disclosure |
| Historical database | Old staff and stakeholder information identified | Sensitive data exposure |
| Authentication | Login security investigated | Potential authentication weaknesses |
| SQL injection | SQL injection concepts investigated | Potential database manipulation |
| Directory discovery | Gobuster explored | Potentially exposed web resources |

**Note:** The observations above should not be interpreted as confirmation that every suspected vulnerability was successfully exploited. Final vulnerability classifications require supporting evidence.

## 📝 Conclusion

The Week 4 penetration-testing project provided practical exposure to web application security assessment and ethical hacking methodologies.

Through the investigation of Mediroza General Hospital's website, I gained experience with reconnaissance, directory discovery, authentication testing, SQL injection concepts and information exposure risks.

The identification of three PDF files and historical database information demonstrated the importance of protecting organizational documents and maintaining appropriate access controls.

I also developed troubleshooting skills while working with Kali Linux and penetration-testing tools.

Overall, this project improved my understanding of how penetration testers identify security weaknesses, investigate potential vulnerabilities and communicate findings through professional documentation.

## ⚠️ Ethical Considerations

This project was conducted as part of an authorized educational cybersecurity exercise.

All testing must remain within the approved scope.

Confidential information must be protected, and sensitive personal records must not be unnecessarily copied, distributed or published.

Denial-of-service testing was excluded from the project.

## 🔗 Tools & Resources

- Kali Linux: https://www.kali.org/get-kali/
- VirtualBox: https://www.virtualbox.org/wiki/Downloads
- Gobuster: https://github.com/OJ/gobuster
- Hydra: https://github.com/vanhauser-thc/thc-hydra
- SecLists: https://github.com/danielmiessler/SecLists
- John the Ripper: https://www.openwall.com/john/

## 👤 Author

**John Cheso**  
Cybersecurity Student  
Batch B084

**Project:** Week 4 – Mediroza General Hospital Penetration Testing
