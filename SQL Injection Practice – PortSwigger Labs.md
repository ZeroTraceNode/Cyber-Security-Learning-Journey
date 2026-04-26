### 1. SQL Injection – Data Retrieval (Administrator Access)

**Objective:** Extract sensitive data and access admin account.

**Steps Performed:**
- Detected SQL injection vulnerability using `'` input testing
- Identified column count using `ORDER BY` technique
- Tested payloads using `UNION SELECT`
- Determined injectable columns via reflected output
- Used `information_schema` to enumerate database structure
- Extracted credentials from user-related tables
- Logged in as administrator using obtained credentials

**Key Payloads:**
```sql
' ORDER BY 1--
' UNION SELECT NULL, NULL--
' UNION SELECT 'a','a'#
