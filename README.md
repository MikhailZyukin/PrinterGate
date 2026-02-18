# dotfiles — Arch Linux Pentesting Workstation

Hostname: `NPI08R488`  
OS: Arch Linux  
Hardware: Laptop  
Stage: Early setup (pre-Hyprland)

This repository tracks the configuration and setup of a minimal, learning-focused Arch Linux workstation intended for security fundamentals and future pentesting work.

The goal is **discipline over bloat**: a small, well-understood toolchain instead of Kali-style metapackages.

---

## Philosophy

- This is **not** Kali Linux
- Tools are installed only if they teach fundamentals
- No automation before understanding
- Clean base system, reproducible config
- Secrets are never committed to Git

This setup prioritizes:
- Learning networking, OS internals, and web fundamentals
- Manual workflows over GUI wrappers
- Long-term maintainability

---

## System State (Current)

- Fresh Arch Linux installation
- No desktop environment yet
- No display manager yet
- TTY-based workflow
- GitHub authentication handled securely via keyring

---

## Installed Base Packages

### Core System & Development
Installed via `pacman`:

- `base-devel`
- `git`
- `curl`, `wget`
- `unzip`, `zip`
- `tmux`
- `neovim`
- `htop`
- `lsof`
- `strace`
- `file`
- `which`

Purpose:
- Understand Linux internals
- Debug processes and binaries
- Build software from source when needed

---

## Networking & Recon Fundamentals

Installed:

- `nmap`
- `netcat`
- `tcpdump`
- `wireshark-cli`
- `bind` (for `dig`)
- `whois`

Focus:
- TCP/IP fundamentals
- DNS and OSINT basics
- Packet-level understanding (CLI-first)

---

## Web Fundamentals (Minimal)

Installed:

- `firefox`
- `ffuf`
- `jq`

Notes:
- No Burp Suite yet
- No automated scanners
- Focus on raw HTTP understanding first

---

## Binary / Exploitation Basics

Installed:

- `gdb`
- `radare2`
- `binutils`

Notes:
- No GDB plugins yet (pwndbg/gef intentionally deferred)
- Learning raw debugging and reversing first

---

## Python Environment Discipline

Installed:

- `python`
- `python-pip`
- `python-virtualenv`

Rule:
> All Python security tools must run in isolated virtual environments.  
System Python is not touched.

## Firewall 
- Firewall : UFW (nftables backend)
- Default policy : deny incoming allow outgoing
- SSH explicitly allowed
- Enabled on boot

## Network Anonimity (Basic)
-Wifi managed via iwd
-Randomization of MAC Address
-Mode: one Randomized mac per network 
