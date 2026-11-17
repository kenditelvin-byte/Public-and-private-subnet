## Architecture Overview

AWS Two-Tier Architecture

This project sets up a secure, two-tier web application network inside an **AWS Virtual Private Cloud (VPC)** (`10.10.0.0/16`)[cite: 1]. 

### How It Works

* **Public Subnet (`10.10.0.0/24`):** Hosts the **Web Server** (EC2). Users on the internet reach it through an **Internet Gateway** and **Router**, with a security group allowing HTTP traffic on **port 80**.
* **Private Subnet (`10.10.2.0/24`):** Hosts the **Database (DB) Server** (EC2). It is isolated from direct internet access for security and only accepts traffic from the Web Server on **port 3306** (MySQL)[cite: 1].

### Traffic Flow
`Internet` ➔ `Internet Gateway` ➔ `Router` ➔ `Web Server (Port 80)` ➔ `DB Server (Port 3306)`[cite: 1]
