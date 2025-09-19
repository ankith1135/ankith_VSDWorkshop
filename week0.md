# VLSI Physical Design Setup – Ubuntu Jammy Jellyfish

This repo documents my setup journey for VLSI tools and workflows.  
I followed a structured approach (Task-1, Task-2, …) and captured screenshots along the way.  
System used: **Ubuntu 22.04 (Jammy Jellyfish)** on **VirtualBox**.

---

## 📌 Table of Contents
- [Day 0 – Tools Installation](#day-0---tools-installatio

---

## 🔹 Task-1: Create GitHub Repo
- Created this repo to document the setup journey.  
- Added summary of the reference video in `README.md`.  
- Plan is to log each day’s progress here, with commands + snapshots.

---

## 🔹 Task-2: Install Tools

### 💻 Machine Configuration
- **OS**: Ubuntu 22.04 (Jammy Jellyfish) inside VirtualBox  
- **RAM**: 6 GB  
- **Storage**: 50 GB HDD  
- **CPU**: 4 vCPUs  

### 🛠 Tools Installed
1. **Yosys**
   ```bash
   sudo apt-get update
   git clone https://github.com/YosysHQ/yosys.git
   cd yosys
   sudo apt install make build-essential clang bison flex \
   libreadline-dev gawk tcl-dev libffi-dev git \
   graphviz xdot pkg-config python3 libboost-system-dev \
   libboost-python-dev libboost-filesystem-dev zlib1g-dev
   make config-gcc
   make
   sudo make install
  ``` ```

## 2. Icarus Verilog (iverilog)

Installation:
```bash
sudo apt-get update
sudo apt-get install iverilog
```
<img width="835" height="577" alt="Screenshot 2025-09-18 223349" src="https://github.com/user-attachments/assets/b6c15ae4-0a1a-48ea-bcdb-200d48eee145" />


## 3. GTKWave

Installation:
```bash
sudo apt-get update
sudo apt-get install gtkwave
gtkwave
```
<img width="1140" height="728" alt="Screenshot 2025-09-18 223858" src="https://github.com/user-attachments/assets/dbe3b3b8-ee5b-4ad0-94c0-7787946dd3bd" />



