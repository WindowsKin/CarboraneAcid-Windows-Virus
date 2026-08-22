# CarboraneAcid-Windows-Virus

# 🧪 CarboraneAcid Virus

> **⚠️ WARNING – FOR EDUCATIONAL USE ONLY**  
> This sample is provided **solely for security research and learning purposes**.  
> **DO NOT** execute it on any production or personal system outside of a fully isolated virtual machine.  
> **The author assumes no responsibility for any data loss or system damage.**

---

## 📖 Description

**CarboraneAcid** is a malicious proof-of-concept that targets **Windows 7 through 11 (and later)** – similar to well-known GDI-effect viruses like **MEMZ**.

Its key characteristic is the ability to perform **full physical disk overwrite (low‑level formatting)** from **user mode (Ring 3)** – **without** requiring a kernel driver to construct and send IRP write requests.

---

## ⚠️ Critical Warnings

- This virus will **forcibly perform a low‑level format** on **all** detected storage devices.
- **All data will be permanently destroyed** – there is no recovery.
- **Only run `CarboraneAcid.exe` inside a virtual machine** with no critical data attached.

---

## 🧬 Technical Insight

| Aspect              | Detail |
|---------------------|--------|
| **Target OS**       | Windows 7 – 11 / higher |
| **Privilege Level** | Ring 3 (user mode) |
| **Attack Vector**   | Direct physical disk access without driver‑based IRP submission |
| **Effect**          | Complete low‑level format of every storage device |
| **Comparable to**   | MEMZ and other GDI‑effect POCs |

---

## 📌 Disclaimer

**THIS SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.**  
Use it at your own risk. The author and contributors are not liable for any damages, data loss, or system corruption resulting from the use of this code.

---

## 📁 Sample File

- `CarboraneAcid.exe` – the compiled binary (not included in this repository).

---

## 🔒 Responsible Use

If you are a security researcher, always:

- Run in an **isolated VM** (e.g., VMware, VirtualBox) with **network disabled**.
- Take a **full snapshot** before execution.
- Never point it at physical hardware containing important data.

---

## 📄 License

This project is released for **academic and research purposes only**.  
Any malicious or illegal use is strictly prohibited.

---

*Last updated: 2026*
