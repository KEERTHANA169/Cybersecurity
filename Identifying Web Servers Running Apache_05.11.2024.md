### Report: Identifying Web Servers Running Apache

---

#### **Objective**

To determine the number of web servers running Apache by analyzing HTTP response headers using a network analysis tool.

---

#### **Methodology**

**Step 1: Filter HTTP Responses**  
- Apply the filter `http.response` in the network analysis tool to isolate all HTTP response packets. This filter ensures only HTTP responses are displayed for further analysis.

**Step 2: Extract Server Information**  
- To view the server type, configure the tool to display the "Server" header from HTTP responses as a column:
  - Select any HTTP response packet.
  - Right-click and choose "Apply as Column" for the "Server" header.
- This allows for an immediate visual display of the server types in the packet list.

**Step 3: Filter for Apache Servers**  
- Apply a secondary filter `http.server contains "Apache"` to narrow down the packets to those originating from Apache servers. This ensures only relevant packets are considered.

**Step 4: Analyze Connection Statistics**  
- Navigate to `Statistics > Endpoints` to display a summary of all connections.
- This section provides an overview of all endpoints and the number of connections each has made.

---

#### **Output**

**Step 5: Identify Apache Connections**  
- After applying the filters, the tool initially shows **22 connections** from servers running Apache.
- Exclude connections from the IP address `192.168.1.71`, identified as a client rather than a server.
- The adjusted count of Apache server connections will be the final result.

---

#### **Conclusion**

Using the HTTP response headers and applying relevant filters, the total number of Apache server connections was determined. By excluding the client IP, the actual count of Apache web server connections is clarified. This approach allows for accurate identification without manual counting.
