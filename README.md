# -palo-alto-ha-active-passive
Palo Alto PA-01 and PA-02 High Availability configuration in PNETLab using Active-Passive HA.

# Palo Alto High Availability Project

## Project Overview

This project demonstrates the configuration of High Availability (HA) between two Palo Alto firewalls, PA-01 and PA-02, using an Active-Passive architecture in PNETLab.

The main objective is to configure PA-01 as the Active firewall and PA-02 as the Passive firewall so that the Passive firewall can provide redundancy if the Active firewall becomes unavailable.

---

## Project Objective

The objectives of this project are:

- Configure High Availability between PA-01 and PA-02.
- Configure PA-01 as the Active firewall.
- Configure PA-02 as the Passive firewall.
- Establish HA1 and HA2 communication.
- Configure and verify the Management Interface IP addresses.
- Verify the final HA topology in PNETLab.

---

## Lab Topology

The lab contains two Palo Alto firewalls connected through HA interfaces and a network switch.

### Components Used

- Palo Alto PA-01
- Palo Alto PA-02
- HA1 switch
- HA2 switch
- Network switch (SW)
- PNETLab
- Palo Alto CLI
- Palo Alto Web GUI

---

## Firewall Details

| Firewall | Role | Management IP |
|----------|------|---------------|
| PA-01 | ACTIVE | 192.168.2.1/24 |
| PA-02 | PASSIVE | 192.168.2.2/24 |

---

## Interface Connections

| Interface | Purpose |
|-----------|---------|
| eth1/1 | Network connection to SW |
| eth1/2 | HA1 connection |
| eth1/3 | HA2 connection |

---

## Final Topology

The completed PNETLab topology is shown below.

![Final Palo Alto HA Topology](Final-Topology.png)

---

## Management Interface Verification

### PA-01 Management Interface

The Management Interface of PA-01 is configured with:

**IP Address:** `192.168.2.1/24`

![PA-01 Management IP](PA01-Management-IP.png)

### PA-02 Management Interface

The Management Interface of PA-02 is configured with:

**IP Address:** `192.168.2.2/24`

![PA-02 Management IP](PA02-Management-IP.png)

---

## HA Architecture

The project uses an Active-Passive High Availability architecture.

### PA-01

**Role:** ACTIVE

PA-01 is the primary firewall handling network traffic during normal operation.

### PA-02

**Role:** PASSIVE

PA-02 remains ready to take over the Active role if required.

---

## Verification

The configuration was verified using the Palo Alto CLI and Web GUI.

The Management Interface IP addresses were verified using:

```text
show interface management
