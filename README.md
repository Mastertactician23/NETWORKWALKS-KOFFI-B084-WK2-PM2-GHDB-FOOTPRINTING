# Week 2 - Project Module 2: Footprinting & Reconnaissance with GHDB

## Overview
In this module, I utilized the **Google Hacking Database (GHDB)** hosted on Exploit-DB to perform passive reconnaissance. GHDB is a collection of advanced Google search queries (Dorks) designed to uncover sensitive information, misconfigured servers, and exposed devices that website owners never intended to make public. 

Because this technique relies entirely on Google's search index, it is 100% passive—meaning the target is never directly contacted, making it extremely difficult to detect.

## Lab Tasks

### Task 1: Exposed Security Cameras
* **Objective:** Find 10 live, vulnerable security camera links exposed to the internet.
* **Methodology:** I used the Exploit-DB GHDB to find relevant dorks, searched them on Google, and manually verified each link to ensure the camera feed was actually live and accessible without authentication.
* **Dork Used:** `intitle: "webcamXP" inurl:8080`

### Task 2: Open Directory Listings (Math PDFs)
* **Objective:** Find 10 open directory listings containing downloadable mathematics ebooks in PDF format.
* **Methodology:** Utilized Google's `index.of` operator to find misconfigured web servers hosting parent directories, then filtered for math-related PDF documents.
* **Dork Used:** `intitle:index.of "parent directory" mathematics pdf`

## Attackers' Perspective & Defense (Key Takeaways)
* **The Risk of Indexing:** If a web server has directory listing enabled by default, Google will index every file inside it. Attackers use GHDB to find these "low-hanging fruit" targets instantly.
* **IoT Vulnerabilities:** The exposed cameras found (like the webcamXP feeds) often lack default password changes, giving attackers direct visual access to physical locations.
* **Defensive Mitigation:** As a defender, it is critical to disable directory browsing on web servers, ensure IoT devices are not exposed to the public internet, and regularly run self-audits using GHDB to see what your organization is leaking.

## Full Report & Evidence
All specific links, exact dorks used, and verified findings are documented in the attached PDF report.

📄 **[Click here to view the full Footprinting Report](NETWORKWALKS-KOFFI-B084-WK2-PM2-GHDB-FOOTPRINTING.docx.pdf)**
