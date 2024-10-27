
# Basic Firewall Setup with pfSense on VMware

This project involves setting up **pfSense** as a basic firewall using **VMware** and configuring it through the pfSense web interface. The goal is to gain foundational skills in network security and traffic control by managing simple firewall rules.

## Project Overview

- **Objective**: Use pfSense as a firewall to secure and control network traffic in a virtual environment.
- **Tools Used**: pfSense, VMware, Web GUI
- **Description**: Installed and configured pfSense in a VMware virtual machine, setting up basic firewall rules to control access and protect network traffic.

## Skills Developed

- **Firewall Configuration**: Set up rules to control network traffic, allowing or blocking as per security requirements.
- **Network Security Basics**: Configured rules to control and secure access to network resources.
- **GUI Management**: Managed the firewall through the pfSense web interface for easy navigation and setup.

## Firewall Rules Configured

Below are the specific firewall rules configured on each interface:

### **WAN Interface Rules**
1. **Allow TCP from Trusted Source**:
   - **Source**: 192.168.xxx.xxx (trusted IP)
   - **Protocol**: TCP
   - **Purpose**: Allows specific inbound TCP traffic from a trusted external IP.
2. **Default Block Rule**:
   - No other WAN traffic is permitted unless specifically allowed.

### **LAN Interface Rules**
1. **Allow All Outbound (Default)**:
   - **Source**: LAN network
   - **Destination**: Any
   - **Protocol**: Any
   - **Purpose**: Allows all outbound traffic from LAN devices, including web and DNS access.
2. **Allow All IPv6 Outbound (Default)**:
   - **Source**: LAN network (IPv6)
   - **Destination**: Any
   - **Protocol**: IPv6
   - **Purpose**: Allows all outbound IPv6 traffic from LAN devices.

### **OPT1 (LapTop) Interface Rules**
1. **Allow All Traffic**:
   - **Source**: OPT1 (LapTop) network
   - **Destination**: Any
   - **Protocol**: Any
   - **Purpose**: Allows unrestricted access to and from the OPT1 interface.

## Setup Overview

1. **Install pfSense on VMware**:
   - Download the pfSense ISO and set up a new virtual machine in VMware.
   - Complete the pfSense installation steps, configuring LAN and WAN interfaces as needed.

2. **Access the pfSense Web GUI**:
   - Once installed, log into the pfSense interface through the web browser using the LAN IP.
   - Configure the firewall rules listed above using the pfSense GUI.

3. **Test Configurations**:
   - Verify that LAN devices can access the internet and that unwanted inbound traffic is blocked.
   - Check the effect of each rule by testing network access to/from LAN and WAN.


