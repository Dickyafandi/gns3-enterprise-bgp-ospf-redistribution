# Enterprise Multi-Site BGP & OSPF Redistribution (GNS3 Simulation)

[ 🇮🇩 Bahasa Indonesia ] | [ 🇬🇧 English Version ]

---

## 🇮🇩 Bahasa Indonesia

### 📌 Deskripsi Proyek
Proyek jaringan tingkat lanjut (*Advanced Network Project*) ini mensimulasikan arsitektur jaringan skala *enterprise* multi-site yang menghubungkan dua *Autonomous System* (AS) yang berbeda menggunakan protokol routing eksternal **BGP (Border Gateway Protocol)**, sementara di dalam masing-masing wilayah korporat menggunakan protokol routing internal **OSPF (Open Shortest Path First)**. 

Proyek ini mendemonstrasikan keahlian *hands-on* dalam hal desain topologi, pengalamatan subnetting, manajemen *border routing*, serta teknik *route redistribution* agar komunikasi *end-to-end* antar cabang perusahaan berjalan mulus tanpa hambatan.

### 🌐 Topologi Jaringan
* **AS 100 (Cabang Utama):** Router R1 (Border Router) & Router R2 (Internal OSPF)
* **AS 200 (Cabang Sekunder / Eksternal):** Router R3 (Border Router) & Router R4 (Internal OSPF)
* **eBGP Link:** Jalur WAN langsung antara R1 dan R3 (`12.12.12.0/30`)

### 🛠️ Fitur & Implementasi Teknis
* Konfigurasi IPv4 Subnetting & Point-to-Point Interfaces.
* Implementasi **OSPF Area 0** untuk routing dinamis di dalam area internal AS 100 dan AS 200.
* Implementasi **eBGP Peering** lintas Autonomous System (AS 100 ↔ AS 200).
* Konfigurasi **Route Redistribution** (Mutual Redistribution antara OSPF dan BGP) di perangkat Border Router (R1 & R3).
* Verifikasi jalur *Routing Table* dan pengujian *End-to-End Connectivity* (100% Success Rate).

---

## 🇬🇧 English Version

### 📌 Project Overview
This advanced network project simulates an enterprise multi-site corporate network architecture connecting two distinct Autonomous Systems (AS) using **BGP (Border Gateway Protocol)** for external routing, while utilizing **OSPF (Open Shortest Path First)** for internal routing within each corporate domain.

This project demonstrates hands-on expertise in topology design, subnet planning, border routing management, and mutual route redistribution to ensure seamless end-to-end communication across different corporate branches.

### 🌐 Network Topology
* **AS 100 (Primary Site):** Router R1 (Border Router) & Router R2 (Internal OSPF)
* **AS 200 (Secondary / External Site):** Router R3 (Border Router) & Router R4 (Internal OSPF)
* **eBGP Link:** Direct WAN link between R1 and R3 (`12.12.12.0/30`)

### 🛠️ Features & Technical Implementation
* IPv4 Subnetting & Point-to-Point Interface configuration.
* **OSPF Area 0** implementation for dynamic internal routing across AS 100 and AS 200.
* **eBGP Peering** setup across separate Autonomous Systems (AS 100 ↔ AS 200).
* **Route Redistribution** configuration (Mutual OSPF and BGP redistribution) on Border Routers (R1 & R3).
* Routing table verification and successful End-to-End Ping test (100% Success Rate).

---

### 🚀 Verification & Results / Hasil Pengujian
* **BGP Status:** `State/PfxRcd` Established and routes successfully exchanged.
* **Routing Table:** External subnets correctly learned via OSPF External Type 2 (`O E2`) and BGP (`B`).
* **Connectivity:** 100% packet delivery confirmed via cross-AS ICMP echo tests.

---

### 🖼️ Lab Screenshots / Dokumentasi Lab

**1. Topologi Jaringan GNS3**
![Topologi Jaringan]
<img width="1162" height="563" alt="Topology" src="https://github.com/user-attachments/assets/ed2cfa1e-21ea-4ae1-83c2-30fdff13c921" />

**2. Status BGP Established**
![BGP Summary]

<img width="661" height="407" alt="bgp-summary" src="https://github.com/user-attachments/assets/c14cc7d3-44c9-4a7a-b2a8-aa4e8f541ae0" />


**3. Tabel Routing R2 (OSPF External O E2)**
![Routing Table R2]
<img width="631" height="409" alt="r2-routing-table" src="https://github.com/user-attachments/assets/0188146b-c46a-4063-867e-16ea4fe70967" />

**4. Tes Ping End-to-End Lintas AS (100% Success)**
![Ping Test]
<img width="622" height="408" alt="ping-test" src="https://github.com/user-attachments/assets/f8417cda-a60a-4b2b-bc77-0245331a5329" />


---
*Built with ❤️ & GNS3 for Network Engineering Portfolio.*
