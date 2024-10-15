**Task**
1.	Open TCP port
2.	OS/VERSIONS
3.	SERVICES
4.	FIREWALL YESOR NO
5.	PERFORM SCRIPT SCAN ON SANE TARGET

**COMMAND**
```
sudo nmap -sS -O -sV --script firewall-bypass scanme.nmap.org --top-ports 100 --reason -T4
```

Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-10-15 12:53 EDT

Nmap scan report for scanme.nmap.org (45.33.32.156)

Host is up, received reset ttl 128 (0.067s latency).

Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f

Not shown: 86 filtered tcp ports (no-response)

PORT     STATE  SERVICE         REASON          VERSION

22/tcp   open   tcpwrapped      syn-ack ttl 128

80/tcp   open   tcpwrapped      syn-ack ttl 128

|_http-server-header: Apache/2.4.7 (Ubuntu)

110/tcp  closed pop3            reset ttl 128

119/tcp  closed nntp            reset ttl 128

144/tcp  closed news            reset ttl 128

515/tcp  closed printer         reset ttl 128

544/tcp  closed kshell          reset ttl 128

990/tcp  closed ftps            reset ttl 128

1026/tcp closedLSA-or-nterm    reset ttl 128

2121/tcp closed ccproxy-ftp     reset ttl 128

3389/tcp closed ms-wbt-server   reset ttl 128

5432/tcp closed postgresql      reset ttl 128

8081/tcp closed blackice-icecap reset ttl 128

8888/tcp closed sun-answerbook  reset ttl 128

OS fingerprint not ideal because: Didn't receive UDP response. Please try again with -sSU

No OS matches for host


OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .

Nmap done: 1 IP address (1 host up) scanned in 33.99 seconds



**Command Breakdown**

**sudo:**

This command runs Nmap with superuser privileges, which is often required for certain types of scans (like SYN scans). Without sudo, you might receive permission errors or limited scan results.

**nmap:**

This is the command-line tool you are using for network exploration and security auditing.

**-sS:**

This flag initiates a SYN scan, which is a stealthy method of port scanning. It sends SYN packets to the target ports and waits for responses (SYN-ACK for open ports or RST for closed ports). It does not complete the TCP handshake, making it less detectable by firewalls and intrusion detection systems.

**-O:**

This option enables OS detection. Nmap tries to determine the operating system of the target by analyzing the responses from the scanned ports.

**-sV:**

This option enables service version detection. Nmap will probe open ports to determine the version of the services running on them, providing more detailed information about the software in use.

**--script firewall-bypass:**

This instructs Nmap to run a specific script from its extensive scripting engine (NSE). The firewall-bypass script attempts to determine if there are any weaknesses in the firewall configuration that could be exploited. This can help in assessing the security posture of the target.

**scanme.nmap.org:**

This is the target hostname you are scanning. It’s a public server maintained by the Nmap project, designed for users to practice scanning without legal repercussions.

**--top-ports 100:**

This option tells Nmap to scan the top 100 most common TCP ports instead of all 65,535. This speeds up the scan while still providing a good overview of the most commonly used services.

**--reason:**

This flag adds additional output to the results, explaining why each port is in its given state (open, closed, filtered). This helps in understanding the scan results better.

**-T4:***

This sets the timing template for the scan. -T4 is a faster timing option that makes Nmap perform scans more aggressively (e.g., increasing the number of parallel probes), which can speed up the scan but might increase the chances of being detected by intrusion detection systems.

**Summary**

Overall, this command is designed to efficiently and stealthily gather information about a target, including open ports, services, OS information, and firewall status, while minimizing the impact of detection. It combines different techniques and options to provide a comprehensive overview of the network security posture of the specified target.







 


