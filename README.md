# Home Network Setup with Unifi Dream Machine

This project demonstrates the setup and configuration of a home network using a **Unifi Dream Machine (UDM)**, a **switch**, and **Unifi access points** to create a secure and reliable home network environment. The goal was to set up and secure the network, including basic configurations and network monitoring to optimize performance.

**Note**<br>
This configuration can also be used in small business environments depending on use case/needs.


## Table of Contents

- [Project Overview](#project-overview)
- [Hardware and Software Requirements](#hardware-and-software-requirements)
- [Network Configuration](#network-configuration)
  - [Unifi Dream Machine Setup](#unifi-dream-machine-setup)
  - [Switch Configuration](#switch-configuration)
  - [Access Points Setup](#access-points-setup)
- [Security Configuration](#security-configuration)
  - [Firewall Settings](#firewall-settings)
  - [Wi-Fi Security](#wi-fi-security)
  - [Network Monitoring](#network-monitoring)
- [Testing and Verification](#testing-and-verification)
- [Conclusion](#conclusion)

---

## Project Overview

This project covers the configuration of a home network environment designed for optimal performance and security. The network includes a **Unifi Dream Machine (UDM)** as the firewall/router, a **managed switch** for connecting multiple devices, and **Unifi access points** to extend Wi-Fi coverage throughout the home. The setup focuses on security through proper configuration of firewalls, Wi-Fi encryption, and monitoring tools.

---

## Hardware and Software Requirements

### Hardware:
- **Unifi Dream Machine (UDM)**: All-in-one router, security gateway, and access point management.
- **Managed Switch (USW)**: To connect multiple wired devices and provide network management features.
- **Unifi Access Points**: To extend Wi-Fi coverage across the house.
- **Ethernet Cables**: To connect devices to the switch and router.
- **Laptop/PC**: For accessing the UDM's management interface and setting up configurations.

### Software:
- **Unifi Network Controller**: Used for managing the UDM and all connected devices.
- **Web Browser**: For accessing the UDM and Network Controller interface (accessible via `http://192.168.1.1` or through the Unifi app).

---

## Network Configuration

### Unifi Dream Machine Setup

1. **Connect the Unifi Dream Machine** to the modem (provided by your ISP) via the WAN port. This will serve as the router and security gateway for the network.
2. **Log in** to the Unifi Network Controller using a browser:
   - Navigate to `http://192.168.1.1` (or use the Unifi app).
   - Set up a new network, selecting options like **DHCP** for automatic IP addressing.
   - Create a strong **admin password** and secure the device.

3. **Configure the UDM**:
   - Set up **LAN settings** (subnet, DHCP range, DNS settings).
   - Enable **remote access** via the cloud controller if needed (for managing the network from anywhere).

---

### Switch Configuration

1. **Connect the Managed Switch** to one of the LAN ports on the UDM.
2. Use the **Unifi Network Controller** to configure the switch:
   - Set up **VLANs** if necessary for network segmentation (e.g., separate networks for guest Wi-Fi and internal devices).
   - Define specific **port profiles** to control the type of devices connected to the switch (e.g., Ethernet ports for IP cameras, printers, etc.).

---

### Access Points Setup

1. **Install the Unifi Access Points** in various locations (such as near the center of rooms or in high-traffic areas for maximum coverage).
2. **Connect each Access Point** to the switch using Ethernet cable and adopt them to the network. 
3. In the **Unifi Network Controller**, adopt the access points and assign them to the desired network.
   - **Create Wi-Fi networks** with appropriate security settings:
     - **WPA3 encryption** (recommended for higher security).
     - Set up **SSID** names for your networks (e.g., `HomeNetwork` for the internal network and `GuestNetwork` for a guest Wi-Fi).
   
4. **Optimize the Access Point Settings**:
   - Adjust **channels** and **transmit power** to minimize interference and ensure strong coverage.

---

## Security Configuration

### Firewall Settings

1. Log into the **Unifi Network Controller** and navigate to the **Firewall** settings.
2. Enable the **built-in firewall** on the UDM and configure rules:
   - Block unnecessary ports and services.
   - Allow only essential ports such as **HTTP/HTTPS** for web access and **SSH** for remote management.

### Wi-Fi Security

1. Enable **WPA3 encryption** on all Wi-Fi networks (if supported by your devices).
2. Set a **strong passphrase** for your Wi-Fi networks.
3. **Disable WPS** to prevent potential vulnerabilities from brute-force attacks.
4. Create a **Guest Wi-Fi** network with a separate VLAN and limited access to internal resources.

### Network Monitoring

1. Enable **traffic monitoring** in the Unifi Network Controller to track bandwidth usage and device activity.
2. Set up **alerts** for unusual traffic patterns or unauthorized access attempts.
3. Optionally, use tools like **PRTG Network Monitor** or **Wireshark** to analyze traffic and identify potential issues.

---

## Testing and Verification

1. **Test Device Connectivity**: Ensure that all devices (wired and wireless) can connect to the network.
2. **Ping Test**: From a connected device, run `ping` commands to verify connectivity with the router and other devices.
3. **Speed Test**: Use an online tool like **Speedtest.net** to check the speed of your internet connection and internal network.
4. **Wi-Fi Coverage Test**: Walk around your home with a mobile device to test the Wi-Fi signal strength and ensure the access points are properly placed.

---


## Conclusion

This project demonstrates the process of setting up a home or business network using a **Unifi Dream Machine**, a **managed switch**, and **Unifi access points**. It highlights best practices for network security and optimization, including configuring firewalls, Wi-Fi encryption, and monitoring tools to ensure a reliable and secure home network environment.

---

Feel free to clone or adapt this setup for your own home network or similar environments. This can also be used to adopt a Unifi Network Video Recorder to add multiple cameras using the protect app in the UDM. 
