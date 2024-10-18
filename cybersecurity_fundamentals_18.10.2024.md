# Cybersecurity Fundamentals

## 1. General Cybersecurity Knowledge

### What is the CIA Triad?
**Answer**: CIA stands for **Confidentiality, Integrity, and Availability**. Confidentiality ensures data is only accessible to authorized users, Integrity ensures that data is accurate and unaltered, and Availability ensures that data is accessible when needed.

### What is the difference between a vulnerability, a threat, and a risk?
**Answer**: 
- **Vulnerability**: A weakness in a system.
- **Threat**: A potential cause of an unwanted event.
- **Risk**: The likelihood of a threat exploiting a vulnerability.

### Definitions:

1. **Vulnerability**:
   - A weakness or flaw in a system, application, or network that can be exploited by attackers.
   - **Examples**: Unpatched software, misconfigured systems, weak passwords.

2. **Threat**:
   - Any potential event or actor that could exploit a vulnerability and cause damage.
   - **Examples**: Malware, phishing attacks, insider threats.

3. **Risk**:
   - The potential for loss or damage when a threat exploits a vulnerability.
   - **Formula**: Risk = Threat x Vulnerability x Impact
   - **Example**: A vulnerability in a web application targeted by hackers increases the risk of compromise.

### Summary:
- **Vulnerability**: A weakness.
- **Threat**: What can exploit the weakness.
- **Risk**: Potential harm from a successful exploitation.

---

## 2. Encryption vs. Hashing

- **Encryption**:
  - A two-way process that transforms plaintext into ciphertext using an algorithm and key, allowing for decryption.
  - **Common Algorithms**: AES (Advanced Encryption Standard), RSA (Rivest–Shamir–Adleman), DES (Data Encryption Standard).
  - **Use Cases**: Securing emails, files, network communications.

- **Hashing**:
  - A one-way process that converts data into a fixed-length hash, ensuring data integrity.
  - **Common Algorithms**: SHA-256 (Secure Hash Algorithm 256-bit), MD5 (Message Digest Algorithm 5), SHA-1 (Secure Hash Algorithm 1).
  - **Use Cases**: Verifying file integrity, storing passwords securely.

### Summary:
- **Encryption**: Reversible with a key (confidentiality).
- **Hashing**: Irreversible, used for integrity checking.

---

## 3. Common Types of Cyberattacks
- **Phishing**: Fraudulent attempts to steal sensitive information.
- **Malware**: Malicious software designed to harm systems.
- **Ransomware**: Malware that encrypts data and demands a ransom.
- **DDoS**: Overwhelming a system with traffic to make it unavailable.
- **MITM**: Intercepting communications between two parties.
- **SQL Injection**: Exploiting application vulnerabilities to execute malicious SQL queries.

---

## Example of SQL Injection Attack:
1. **Initial Query**:
   ```sql
   SELECT * FROM users WHERE username = 'user_input' AND password = 'user_input';

2. **Attacker Input**:
   ```sql
   ' OR '1'='1
   ```
3. **Modified Query**:
   ```sql
   SELECT * FROM users WHERE username = '' OR '1'='1' AND password = '';
   ```

