### Cross-Site Request Forgery (CSRF) Overview

**Cross-Site Request Forgery (CSRF)** is a type of web security vulnerability that allows an attacker to trick a user into unknowingly submitting a request to a web application on which they are authenticated. This can lead to unauthorized actions being performed on behalf of the user without their consent, potentially compromising their account or sensitive data.

### Lab Task Explanation
In this lab, you exploited a CSRF vulnerability using Burp Suite. The steps you took included:

1. **Log in and Capture the Request**: You opened Burp's browser, logged into your account, and submitted the "Update email" form. You then found the resulting request in your Proxy history, which contained the details of the action you performed.

2. **Generate CSRF Proof of Concept (PoC)**: If using Burp Suite Professional, you generated a CSRF PoC directly from the captured request. This included an auto-submit script to automatically send the request when the HTML was loaded. For the Community Edition, you manually created an HTML template that replicated the request, ensuring to include the appropriate action URL and parameters.

   Example HTML Template:
   ```html
   <form method="POST" action="https://YOUR-LAB-ID.web-security-academy.net/my-account/change-email">
       <input type="hidden" name="email" value="anything%40web-security-academy.net">
   </form>
   <script>
           document.forms[0].submit();
   </script>
   ```

3. **Store the Exploit**: You navigated to the exploit server, pasted your crafted HTML into the "Body" section, and clicked "Store" to save your exploit.

4. **Verify the Exploit**: To ensure your exploit worked, you clicked "View exploit" to see the resulting HTTP request and response, confirming that the request was correctly formulated and would execute the desired action.

5. **Modify the Email Address**: You changed the email address in your exploit to ensure it didn't match your own, which is crucial for demonstrating the exploit on a victim's account.

6. **Deliver the Exploit**: Finally, you clicked "Deliver to victim" to complete the lab task, successfully executing the CSRF attack.

### Conclusion
This lab provided hands-on experience with CSRF vulnerabilities, highlighting how attackers can manipulate web requests to perform unauthorized actions. Understanding CSRF exploitation helps in recognizing the importance of implementing defenses such as anti-CSRF tokens in web applications to safeguard against such attacks.
