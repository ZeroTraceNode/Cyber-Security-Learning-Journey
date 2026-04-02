## 📚 Source
PortSwigger Web Security Academy

## 🎯 Objective
Identify valid usernames and automate enumeration using Burp Suite Intruder.

## 🛠️ Tools Used
- Burp Suite (Proxy, Repeater, Intruder)

## 🔍 Key Concept
Applications may reveal valid usernames through differences in responses:
- Invalid username → one type of response
- Valid username + wrong password → different response

## ⚙️ Methodology

### Step 1: Interception
- Capture login request using Burp Suite Proxy

### Step 2: Manual Testing
- Send requests to Repeater
- Observe differences in responses

### Step 3: Intruder Automation (Sniper Attack)
- Send request to Intruder
- Use **Sniper mode** (single payload position)
- Insert username payload list
- Launch attack

### Step 4: Analysis
- Compare responses:
  - Length
  - Status codes
  - Error messages

### ✅ Result
- Successfully identified a valid username
- Successfully found the password with a brute-force attack
- Completed the lab

## 💡 Key Learning
- Response discrepancies can lead to user enumeration
- Intruder (Sniper) helps automate targeted payload testing
