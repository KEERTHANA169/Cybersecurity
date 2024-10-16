### Cross-Site Scripting (XSS) Overview

**Cross-Site Scripting (XSS)** is a common web security vulnerability that allows attackers to inject malicious scripts into webpages viewed by other users. XSS exploits the trust a user has in a website, enabling attackers to execute scripts in the victim's browser, potentially leading to session hijacking, defacement, or redirection to malicious sites.

### Types of XSS
1. **Stored XSS**: The malicious script is stored on the server (e.g., in a database) and executed whenever a user accesses the affected page.
2. **Reflected XSS**: The script is reflected off a web server, often via a URL or query string, and executed immediately without being stored.
3. **DOM-based XSS**: The attack occurs in the Document Object Model (DOM) rather than being reflected from the server.

### Lab Task Explanation
In your lab task, you likely tested various methods to identify and exploit XSS vulnerabilities on a web application. This would have involved:

- **Input Validation Testing**: Checking how the application handles user inputs and whether it sanitizes or escapes potentially dangerous characters (e.g., `<`, `>`, `&`).
- **Payload Delivery**: Crafting and injecting payloads to test the application’s response. Common payloads include JavaScript alerts or cookies theft scripts.
- **Assessing Vulnerability**: Observing the application's behavior when the payloads were executed, which helps determine if XSS is possible and assess the impact on users.

### Conclusion
Understanding XSS is crucial for web application security. By recognizing how these vulnerabilities arise and learning to exploit them in a controlled environment, you can better protect applications from potential attacks. Your lab task not only enhances your technical skills but also contributes to a deeper understanding of web security principles.
