# VAPT Authentication Lab Exercise

## Lab Scenario:
Every web application has a login page where you can enter your username and password that gets validated by the backend. What if there are misconfigurations in this login page script and the attacker is able to bypass the login easily?

## Lab Objective:
Username enumeration via different responses.

## Lab Environment:
- OS/Tools to be used: PortSwigger – Lab 1.

## Lab Tasks:
This lab is vulnerable to username enumeration and password brute-force attacks. It has an account with a predictable username and password, which can be found in the following wordlists:
- Candidate usernames list – [Download here]
- Candidate passwords list – [Download here]

To solve the lab:
1. Enumerate a valid username.
2. Brute-force the user's password.
3. Access their account page.

## Steps to Achieve the Task:
1. With Burp running, investigate the login page and submit an invalid username and password.
2. In Burp, go to **Proxy > HTTP history** and find the **POST /login** request.
3. Highlight the value of the **username** parameter in the request and send it to **Burp Intruder**.
4. In **Burp Intruder**, go to the **Positions** tab. The **username** parameter should be set as a payload position automatically, indicated by § symbols (e.g., `username=§invalid-username§`).
5. Leave the password as any static value for now and make sure the **Sniper** attack type is selected.
6. In the **Payloads** tab, ensure the **Simple list** payload type is selected.
7. Under **Payload settings**, paste the list of candidate usernames. Click **Start attack**. The attack will run in a new window.
8. When the attack finishes, examine the **Length** column in the **Results** tab. One entry will be longer than the others and may have a message like "Incorrect password" instead of "Invalid username." Note the username from the **Payload** column.
9. Close the attack and return to the **Positions** tab. Click **Clear**, then change the username parameter to the valid username you just found.
10. Add a payload position to the password parameter so that it looks like this:
    ```
    username=identified-user&password=§invalid-password§
    ```
11. In the **Payloads** tab, clear the list of usernames and replace it with the candidate password list. Click **Start attack**.
12. Once the attack finishes, check the **Status** column for a 302 response, indicating a successful login. Note the corresponding password.
13. Log in with the identified username and password to access the user account page.

## Output:
Once logged in as Administrator, the lab should display as solved.

