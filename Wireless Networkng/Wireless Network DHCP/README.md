# 📡Wireless Network with DHCP

> **Dynamic IP Addressing & Wireless Connectivity**

This lab demonstrates the configuration of a **wireless network with DHCP** using **Cisco Packet Tracer**.

The objective was to configure a network where wired and wireless devices could communicate while receiving their IP addresses **automatically through DHCP**.

---

## 🎯 Objectives

* Configure a **DHCP Server**
* Configure a **Wireless Access Point**
* Configure a wireless **SSID**
* Connect wired and wireless clients
* Verify **dynamic IP addressing**
* Test communication between devices

---

## 🖥️ Network Topology

The lab uses the following devices:

| Device                   | Role                                |
| ------------------------ | ----------------------------------- |
| 🖥️ DHCP Server          | Provides IP addresses automatically |
| 🔀 Switch                | Connects wired devices              |
| 📡 Wireless Access Point | Provides wireless connectivity      |
| 💻 PC                    | Wired client                        |
| 💻 Laptop                | Wireless client                     |

---

## ⚙️ Configuration

### 1. DHCP Server

The DHCP Server was configured to automatically assign IP addresses to devices joining the network.

### 2. Wireless Access Point

The Access Point was configured with an **SSID** to provide wireless network access.

### 3. Client Configuration

The wired PC and wireless Laptop were configured to obtain their network settings dynamically.

### 4. Connectivity Testing

The assigned IP addresses were verified and connectivity was tested using **ping**.

---

## 🧪 Verification & Results

| Test                      | Result       |
| ------------------------- | ------------ |
| DHCP IP Assignment        | ✅ Successful |
| Wireless Connection       | ✅ Successful |
| Wired Connection          | ✅ Successful |
| Dynamic IP Verification   | ✅ Successful |
| Ping Test                 | ✅ Successful |
| PC ↔ Laptop Communication | ✅ Successful |

---

## 🌐 Network Flow

```text
                    ┌─────────────────┐
                    │   DHCP Server   │
                    └────────┬────────┘
                             │
                             │
                       ┌─────▼─────┐
                       │   Switch  │
                       └─────┬─────┘
                             │
                ┌────────────┴────────────┐
                │                         │
          ┌─────▼─────┐           ┌─────▼─────────┐
          │    PC     │           │ Wireless AP   │
          │  Wired    │           │    📡         │
          └───────────┘           └──────┬─────────┘
                                         │
                                      📶 Wi-Fi
                                         │
                                  ┌──────▼──────┐
                                  │   Laptop    │
                                  │  Wireless   │
                                  └─────────────┘
```

---

## 📚 Key Learning

This lab strengthened my practical understanding of how **DHCP and wireless networking** work together.

I learned how a DHCP Server can automatically provide IP configuration to clients while a Wireless Access Point allows wireless devices to connect to the same network.

The lab also provided hands-on practice with:

* **DHCP**
* **IPv4 addressing**
* **Wireless networking**
* **Access Point configuration**
* **Dynamic IP addressing**
* **Basic connectivity testing**

---

## 📂 Lab Files

### 🔹 Cisco Packet Tracer File

* [01-Wireless Network with DHCP.pkt](https://github.com/muhammadmustf564-cyber/CCNA-Lab-Portfolio/blob/main/Wireless%20Networkng/Wireless%20Network%20DHCP/01-Wireless%20Netwrok%20with%20DHCP.pkt)

### 🔹 Network Topology

![Network Topology](https://github.com/muhammadmustf564-cyber/CCNA-Lab-Portfolio/blob/main/Wireless%20Networkng/Wireless%20Network%20DHCP/02-Newtork%20topology.png)

### 🔹 DHCP Server Configuration

![DHCP Server Configuration](https://github.com/muhammadmustf564-cyber/CCNA-Lab-Portfolio/blob/main/Wireless%20Networkng/Wireless%20Network%20DHCP/03-DHCP%20server%20configuration.png)

### 🔹 Access Point Configuration

![Access Point Configuration](https://github.com/muhammadmustf564-cyber/CCNA-Lab-Portfolio/blob/main/Wireless%20Networkng/Wireless%20Network%20DHCP/04-Access%20point%20configuration.png)

### 🔹 Dynamic IP Configuration

![Dynamic IP Configuration](https://github.com/muhammadmustf564-cyber/CCNA-Lab-Portfolio/blob/main/Wireless%20Networkng/Wireless%20Network%20DHCP/05-Dynamic%20ip%20configuration.png)

---

## 🛠️ Tools & Technologies

* **Cisco Packet Tracer**
* **DHCP**
* **Wireless Access Point**
* **IPv4**
* **Dynamic IP Addressing**
* **Ping**

---

## 🚀 CCNA Lab Journey

Continuing my hands-on **CCNA Lab Journey** to strengthen practical networking, configuration, and troubleshooting skills.

---

