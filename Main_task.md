# 🛡️ Phishing Email Analysis Report

## 🎯 Objective

Identify **phishing characteristics** in a suspicious email sample using both manual inspection and free online tools.

---

## 🧰 Tools Used

- 📧 **Email client** or **saved email file** (in plain text)
- 🔍 **Online header analyzer**  
  [MXToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)

---

## 📬 Email Sample Source

![Email_Security](https://github.com/user-attachments/assets/6426e093-241e-4487-b714-3314d567a9d0)


---

## 🔍 Analysis Steps & Findings

### 1. 🕵️ Sender Email Address

- **Observed:** `973c_bciu.82iu@bain.com`
- **Issue:** Spoofed domain trying to copy `timhortons`  
- In many cases the email would actually look like the orignal email domain but would exchange numbers in place of letters or vice-versa to make it look like legit but not. Like Uses number "1" instead of letter "l"

---

### 2. 🧾 Email Header Inspection

- **Tool Used:** MXToolbox Header Analyzer
- ![header](https://github.com/user-attachments/assets/9b9172e6-bc77-4a88-826e-4b83e729e63e)

- **Findings:**
  - SPF Alignment: ✅ **Pass**
  - SPF Authenticated: ✅ **Pass**    
  - DKIM Alignment: ✅ **Pass**
  - DKIM Authenticated: ❌ **Fail**
  - Ok Icon DMARC Compliant
  - Received from: Suspicious IP in a different country
  - Return-Path: Mismatched with "From" address

---

### 3. 🔗 Suspicious Links or Attachments

- **Link text:** `Click here to claim prize`
- **Actual URL:** `http://timcoffeservice.org/`
- **Issue:** Mismatched domain; non-HTTPS, suspicious TLD


---

### 4. ⚠️ Language & Tone

- **Phrases found:**
  - _"Claim your Prize immidiately"_
 

- **Trait:** Uses fear and urgency to provoke reaction

---

### 5. 🔡 Spelling & Grammar
(Not in this message but usually are present)
- Multiple grammatical mistakes:
  - "Your account has been compromise."
  - "We needing you update now."

---

## ✅ Summary of Phishing Indicators

| Indicator                        | Found? | Notes                                                  |
|----------------------------------|--------|--------------------------------------------------------|
| Spoofed sender address           | ✅     | `paypa1.com` instead of `paypal.com`                   |
| Header anomalies (SPF, DKIM)     | ✅     | One failed                                             |
| Suspicious/malicious link        | ✅     | Hover shows different, sketchy URL                     |
| Urgent/threatening language      | ✅     | Fear-based trigger phrases                             |
| Spelling/grammar errors          | ✅     | Multiple grammar issues found                          |

---

## 📌 Conclusion

This email displays **multiple classic phishing characteristics** and should be treated as malicious. Users are advised **not to click on any links or download attachments**, and report it to their security team immediately.

---

> 🧠 **Tip:** Always double-check email domains, hover over links before clicking, and verify suspicious messages with official support channels.
