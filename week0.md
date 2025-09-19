This repo documents my setup journey for VLSI tools and workflows.  
I followed a structured approach (Task-1, Task-2, …) and captured screenshots along the way.  
System used: **Ubuntu 22.04 (Jammy Jellyfish)** on **VirtualBox**.

---

## 📌 Table of Contents
- [Day 0 – Tools Installation](#day-0---tools-installations)

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
<img width="1104" height="754" alt="image" src="https://github.com/user-attachments/assets/1acb972d-9191-4d71-9918-aeea7e26364e" />

2. **Icarus Verilog (iverilog)**

Installation:
```bash
sudo apt-get update
sudo apt-get install iverilog
```
<img width="835" height="577" alt="Screenshot 2025-09-18 223349" src="https://github.com/user-attachments/assets/b6c15ae4-0a1a-48ea-bcdb-200d48eee145" />

3.**GTKWave**

Installation:
```bash
sudo apt-get update
sudo apt-get install gtkwave
gtkwave
```
<img width="1140" height="728" alt="Screenshot 2025-09-18 223858" src="https://github.com/user-attachments/assets/dbe3b3b8-ee5b-4ad0-94c0-7787946dd3bd" />

4. **OpenSTA**

Installation:
```bash
https://github.com/The-OpenROAD-Project/OpenSTA.git
cd OpenSTA
mkdir build
cd build
cmake ..
make -j$(nproc)
make install
```
<img width="1227" height="495" alt="image" src="https://github.com/user-attachments/assets/850b365e-cbfc-471a-b065-7cee5f84525a" />

5. **ngspice**

Installation:
```bash
After downloading the tarball from https://sourceforge.net/projects/ngspice/files/ to a local
directory, unpack it using:
tar -zxvf ngspice-37.tar.gz
cd ngspice-37
mkdir release
cd release
../configure --with-x --with-readline=yes --disable-debug
make
sudo make install 

```
<img width="871" height="624" alt="Screenshot 2025-09-19 064112" src="https://github.com/user-attachments/assets/5c3d0bad-c43d-4962-95f4-d854cbd241ee" />

6. **magic**

Installation:
```bash
sudo apt-get install tcsh
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install tcl-dev tk-dev
sudo apt-get install libcairo2-dev
sudo apt-get install mesa-common-dev libglu1-mesa-dev
sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
make install 

```
<img width="1201" height="753" alt="Screenshot 2025-09-19 073047" src="https://github.com/user-attachments/assets/6c838f32-3a58-426d-9073-ffdd70cb2ce7" />


7. **Openlane**
<img width="1248" height="782" alt="image" src="https://github.com/user-attachments/assets/7a920f38-a285-424e-a223-f26dc1334330" />

