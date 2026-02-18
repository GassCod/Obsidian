---
tags:
  - Cyber
  - OffSec
  - pentest_tools
  - пентест
  - "#web"
---
---

created: "{{date}}"  
tags:

- burp-suite
    
- pentest
    
- how-to
    

---

# Burp Suite — Quick Usage Guide

> **Goal:** use Burp effectively during labs and pentesting.

---

## Setup (once)

- Start Burp
    
- Browser proxy: `127.0.0.1:8080`
    
- Install Burp CA certificate
    

---

## 1. Proxy → HTTP History (START HERE)

**Do:**

- Browse the website normally
    
- Watch requests appear
    

**Look for:**

- Endpoints
    
- Parameters
    
- Cookies
    



---

## 2. Proxy → Intercept (ONLY WHEN NEEDED)

**Use for:**

- Login
    
- Sensitive actions
    

**Steps:**

1. Intercept ON
    
2. Perform action
    
3. Modify request
    
4. Forward
    

---

## 3. Repeater (MAIN TOOL)

**Do here:**

- Change parameters
    
- Remove headers
    
- Resend requests
    

> Most vulnerabilities are confirmed in Repeater.


---

## 4. Intruder (OPTIONAL)

**Use for:** brute-force, fuzzing, enumeration

---

## 5. Decoder (HELPER)

**Use for:** decoding cookies, tokens, payloads

---

## Typical Workflow

1. Browse → HTTP History
    
2. Send request → Repeater
    
3. Modify → observe response
    
4. Automate only if needed
    

---

## Rules

- Manual first
    
- One request at a time
    
- Watch response differences