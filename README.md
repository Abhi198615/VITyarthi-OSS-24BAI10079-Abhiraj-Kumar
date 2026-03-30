 #  Open Source Audit — Capstone Project

> Course: Open Source Software (OSS NGMC)
> Student: Abhiraj Kumar
> Registration No.: 24BAI10079
> Chosen Software: Python 

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

##  Project Overview

This project is a hands-on exploration of open-source principles through a series of Bash shell scripts. Each script investigates a different aspect of a Linux system — from system identity and package inspection to disk auditing, log analysis, and even generating a personal open-source manifesto.

The goal isn't just to write scripts — it's to **think like an open-source developer**: understand the tools you use, respect the philosophy behind them, and document your work so others can learn from it too.

All scripts are written for Debian/Ubuntu-based Linux systems and are designed to be readable, modifiable, and educational.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


##  Features

-  **System Identity Report** — Captures kernel version, current user, and system uptime in a clean audit format
-  **FOSS Package Inspector** — Checks if a package is installed, displays its version and license, and shares a fun philosophy note
-  **Disk & Permission Auditor** — Loops through key system directories and reports their permissions and sizes
-  **Log File Analyzer** — Parses any log file for a keyword and counts occurrences — useful for quick diagnostics
-  **Open Source Manifesto Generator** — An interactive script that takes your answers and writes a personal manifesto to a text file

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


##  Folder / Script Overview
```
open-source-audit/
│
├── script1.sh       # System Identity Report
├── script2.sh       # FOSS Package Inspector
├── script3.sh       # Disk and Permission Auditor
├── script4.sh       # Log File Analyzer
├── script5.sh       # Open Source Manifesto Generator
└── README.md        # You're reading it!
```

| Script | Name | What It Does |
|--------|------|--------------|
| `script1.sh` | System Identity Report | Displays kernel, username, and uptime in a formatted banner |
| `script2.sh` | FOSS Package Inspector | Checks if `python3` is installed, shows its version/license, and prints a philosophy note |
| `script3.sh` | Disk & Permission Auditor | Iterates over `/etc`, `/var/log`, `/home`, `/usr/bin`, `/tmp` and reports permissions + size |
| `script4.sh` | Log File Analyzer | Accepts a log file path and keyword as arguments; counts matching lines |
| `script5.sh` | Manifesto Generator | Prompts 3 questions interactively and saves a manifesto to a `.txt` file |

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Getting Started

Follow these steps to get all scripts up and running on your Linux system.

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/open-source-audit.git
cd open-source-audit
```

### 2. Make Scripts Executable

Before running any script, give it execute permission:
```bash
chmod +x script1.sh script2.sh script3.sh script4.sh script5.sh
```

Or all at once:
```bash
chmod +x *.sh
```

### 3. Run a Script
```bash
./script1.sh
```

That's it! Each script is self-contained and requires no installation.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


##  Usage

###  Script 1 — System Identity Report
```bash
./script1.sh
```

**Sample Output:**
```
================================
 Open Source Audit — Abhiraj Kumar
================================
Kernel : 6.5.0-21-generic
User   : abhiraj
Uptime : up 2 hours, 14 minutes
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


###  Script 2 — FOSS Package Inspector
```bash
./script2.sh
```

Checks if `python3` is installed on your system and prints its version, status, and a short note on its open-source philosophy.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Script 3 — Disk & Permission Auditor
```bash
./script3.sh
```

**Sample Output:**
```
Directory Audit Report
----------------------
/etc => Permissions: drwxr-xr-x root root | Size: 12M
/var/log => Permissions: drwxrwxr-x root syslog | Size: 45M
...
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Script 4 — Log File Analyzer
```bash
./script4.sh /var/log/syslog error
```

- **Argument 1:** Path to the log file
- **Argument 2:** Keyword to search for (defaults to `error` if not provided)

**Sample Output:**
```
Keyword 'error' found 17 times in /var/log/syslog
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### Script 5 — Open Source Manifesto Generator
```bash
./script5.sh
```

You'll be prompted to answer 3 questions. After that, a manifesto file named `manifesto_<yourusername>.txt` is generated in the current directory.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Requirements

| Requirement | Details |
|-------------|---------|
| **OS** | Ubuntu / Debian-based Linux (tested on Ubuntu 22.04+) |
| **Shell** | Bash (`/bin/bash`) |
| **Tools** | `dpkg`, `apt-cache`, `awk`, `grep`, `du`, `uname`, `whoami`, `uptime` |
| **Package** | `python3` (for Script 2 — should already be installed on most distros) |
| **Permissions** | Some scripts may need `sudo` to read certain log files |

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


