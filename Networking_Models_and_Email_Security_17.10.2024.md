# OSI Model - Overview and Layers

The OSI (Open Systems Interconnection) model, created in 1984 by the ISO, is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven distinct layers. It helps in understanding how data is transmitted over a network.

## OSI Layers:
1. **Application Layer**
2. **Presentation Layer**
3. **Session Layer**
4. **Transport Layer**
5. **Network Layer**
6. **Data Link Layer**
7. **Physical Layer**

---

## 1. Physical Layer
- **Function**: Responsible for the physical connection between devices and transmitting raw bit streams (0s and 1s) over a physical medium.
- **Key Functions**:
  - Bit synchronization with a clock signal.
  - Bit rate control (bits per second transmission rate).
  - Defines physical topologies like bus, star, or mesh.
  - Transmission modes: Simplex, Half-duplex, Full-duplex.
  
- **Devices**: Hub, Repeater, Modem, Cables.
  
---

## 2. Data Link Layer
- **Function**: Manages node-to-node data transmission and error checking on the physical layer. Divided into two sub-layers: 
  1. **Logical Link Control (LLC)**
  2. **Media Access Control (MAC)**
  
- **Key Functions**:
  - Framing: Breaking data into frames for transmission.
  - Physical addressing (MAC): Sender and receiver's MAC addresses are added to frames.
  - Error control: Detects and retransmits damaged or lost frames.
  - Flow control: Ensures the sender and receiver have a constant data flow rate.
  - Access control: Determines which device controls a shared communication channel.

- **Devices**: Switch, Bridge.
  
---

## 3. Network Layer
- **Function**: Handles the transmission of data across different networks. It is responsible for routing data packets and placing the sender and receiver's IP addresses in packet headers.
  
- **Key Functions**:
  - Packet forwarding and routing.
  - Logical addressing (IP addresses).
  
---

## Additional Notes
- **Lower Layers**: Physical, Data Link, and Network layers are also called the "hardware layers."
- **Frames**: In the Data Link Layer, data is encapsulated in frames.

---

## TCP/IP Model and Packet Transmission

Whenever data is transmitted over the internet using the TCP/IP model, the data is divided into packets at the sender’s end. These packets are then recombined at the receiver’s end to recreate the original data, ensuring accuracy throughout the process. The TCP/IP model follows a 4-layer architecture, where data passes through each layer in sequence at the sender's end and in reverse order at the receiver's end.

### Layers of TCP/IP Model:
1. **Application Layer**
2. **Transport Layer**
3. **Network Layer**
4. **Data Link Layer**

### Key Differences between OSI and TCP/IP Models:
1. The **OSI model** consists of 7 layers, while the **TCP/IP model** has 4 layers. Layers 5, 6, and 7 of the OSI model are combined into the Application Layer of TCP/IP, and OSI Layers 1 and 2 are combined into the Network Access Layer in TCP/IP.
2. The **TCP/IP model** predates the OSI model and is the foundational protocol defining how data is transferred online.
3. The **TCP/IP model** has less strict layer boundaries, allowing more flexibility.
4. All layers in the **TCP/IP model** are required for data transmission, whereas certain applications can skip layers in the **OSI model**, with only layers 1, 2, and 3 being essential.

---

## Email Security

Email security ensures the availability, integrity, and authenticity of email communications by protecting them from unauthorized access and email-based threats. Email plays a vital role in how the internet functions, making it a frequent target for malicious attacks.

### Common Types of Email Attacks:
- **Phishing**
- **Spamming**
- **Malware Delivery**
- **Business Email Compromise (BEC)**
- **Ransomware**
- **Man-in-the-Middle Attack**
- **Data Exfiltration**

### Benefits of Email Security:
- Ensures availability and authenticity of communications.
- Prevents fraud, malware, and phishing attacks.
- Provides real-time defense against threats.

### Best Practices for Email Security:
- Enforce encrypted connections.
- Use encryption for sensitive emails.
- Create strong passwords.
- Implement two-factor or multi-factor authentication.
- Train employees on anti-phishing tactics.
- Use domain authentication and a secure email gateway.
- Employ secure Wi-Fi networks for communication.

### Features of Email Security Tools:
- Malware and antivirus protection.
- Spam and phishing detection.
- Email encryption.
- Data loss prevention (DLP).
- Anti-spoofing measures.
- Reporting and analytics for email traffic.
