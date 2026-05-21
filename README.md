# RudraScan 🔍

An automated reconnaissance and vulnerability scanner for security researchers and penetration testers.

## Features

- **Subdomain Enumeration** — passive, bruteforce, permutations, cert transparency
- **OSINT** — WHOIS, email leaks, Google dorking, GitHub secret scanning, cloud buckets
- **Web Analysis** — screenshots, JS analysis, CMS detection, directory fuzzing
- **Vulnerability Scanning** — XSS, SQLi, SSRF, LFI, SSTI, CRLF, command injection
- **Port Scanning** — nmap/naabu with service fingerprinting and WAF/CDN detection
- **AI Reports** — auto-generated scan reports via local LLM (llama3)

## Installation

## 🎥 Full Video Tutorial (10 Minutes)

New users can follow this complete walkthrough covering installation, setup, configuration, and live scanning demo.

▶️ Watch here: [https://www.youtube.com/watch?v=i-SW3gJgOi4]

```bash
git clone https://github.com/sidhusec/Rudrascan
cd Rudrascan
./install.sh
```

## Usage

```bash
# Full recon
./rudrascan.sh -d target.com -r

# Passive only
./rudrascan.sh -d target.com -p

# Full recon + active attacks
./rudrascan.sh -d target.com -a

# Multiple targets
./rudrascan.sh -l targets.txt -r
```

## Scan Modes

| Flag | Mode |
|------|------|
| `-r` | Full recon (no attacks) |
| `-a` | Full recon + vulnerability checks |
| `-p` | Passive recon only |
| `-s` | Subdomain enumeration only |
| `-n` | OSINT only |
| `-w` | Web vulnerability checks |
| `-z` | Lightweight / zen mode |

## Docker

```bash
docker pull sidhusec/Rudrascan:main
docker run -it --rm -v "${PWD}/output:/rudrascan/Recon/" sidhusec/rudrascan:main -d target.com -r
```

## Requirements

- Linux / macOS with Bash 4+
- 10–20 GB free disk space
- Stable internet connection during install

## ⚠️ Disclaimer

Use only on targets you have explicit permission to test. Unauthorized scanning is illegal. The developers are not responsible for misuse.


