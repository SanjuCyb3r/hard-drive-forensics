# Hard-Drive Forensics Exam – Expert Witness Report

End-to-end forensic examination of a **40 GB Seagate Barracuda 7200.7** HDD acquired with a **WiebeTech Forensic UltraDock v5.5** and verified in **FTK Imager 4.3.1.1**. The repo includes the full report, acquisition log, exhibits, and a clean methodology you can reproduce.

<p align="center">
  <img alt="badge" src="https://img.shields.io/badge/Discipline-Digital%20Forensics-blue">
  <img alt="badge" src="https://img.shields.io/badge/Tools-FTK%20Imager%20|%20Autopsy%20|%20UltraDock%20v5.5-orange">
  <img alt="badge" src="https://img.shields.io/badge/Focus-Chain%20of%20Custody%20|%20Artifact%20Analysis-green">
</p>

## ✨ Highlights
- Forensically acquired the disk in **E01** with **MD5/SHA-1 verification** (FTK Imager 4.3.1.1).
- Write-protected acquisition using **WiebeTech UltraDock v5.5** (photographic exhibits included).
- Autopsy analysis recovered: mailbox data (PST), **financial spreadsheet (iPhones.xlsx)**, **browser artifacts consistent with jailbreak activity**, and a **VPN configuration (rasphone.pbk)** tying usage to anonymization.
- Clear **chain-of-custody** and reproducible methodology for classroom or lab use.

---

## 🧾 Evidence Summary

| Field | Value |
|---|---|
| Drive model | **ST340014AS** (Seagate Barracuda 7200.7), 40 GB |
| Interface | SCSI (via write-blocker) |
| Sector size / count | 512 bytes / 78,125,000 |
| Hashes (E01) | MD5: `5e024fd596e916ad6bf8905c57456ca7`  ·  SHA-1: `4436c4694e21e075d685c0d7d0ce52717ba2851f` |
| Imaging tool | FTK Imager **4.3.1.1** |
| Write-blocker | **WiebeTech Forensic UltraDock v5.5** |
| Case info | Case: JJL06172020 • Evidence: FP-2020 |

> The full FTK acquisition/verification log is in `evidence/FinalProject.E01.txt`.

---

## 📚 Repository Contents

```
hard-drive-forensics-exam/
├─ README.md
├─ LICENSE
├─ .gitignore
├─ report/
│  └─ Sanjay_Samala_Forensic_Final_Report.pdf
├─ evidence/
│  ├─ FinalProject.E01.txt
│  └─ exhibits/
│     ├─ ultradock_front.jpg
│     ├─ ultradock_menu.jpg
│     ├─ ultradock_label.jpg
│     ├─ hdd_label.jpg
│     ├─ hdd_side.jpg
│     └─ hdd_pcb.jpg
└─ docs/
   ├─ executive-summary.md
   ├─ methodology.md
   ├─ artifact-findings.md
   └─ chain-of-custody.md
```

---

## 🖼️ Exhibits (inline preview)

<p align="center">
  <img src="evidence/exhibits/ultradock_front.jpg" alt="WiebeTech UltraDock front" width="45%"/>
  <img src="evidence/exhibits/hdd_label.jpg" alt="Seagate HDD label" width="45%"/>
</p>

> More photos in `evidence/exhibits/`.

---

## 🛠️ Tooling
- **Acquisition**: FTK Imager 4.3.1.1 → Expert Witness Format (**.E01**) with verify pass.
- **Write-blocking**: WiebeTech UltraDock v5.5 (USB/Power attached; menu screenshots included).
- **Analysis**: Autopsy (timeline, keyword search, file carving, email parsing, web artifacts).

---

## 🔬 Method (summary)
1. **Scene & Intake** → photographed HDD, documented identifiers, attached to UltraDock (write-protected).
2. **Acquisition** → FTK Imager physical image to E01; computed **MD5/SHA-1**; verified post-acquisition.
3. **Triage** → mounted E01 in Autopsy; enumerated users, partitions, and volume metadata.
4. **Artifact Analysis** → email archives, spreadsheets, browser history/cache, **`rasphone.pbk`** VPN config, thumbnails.
5. **Attribution** → correlated artifacts to user profiles; prepared evidence tables and timeline.
6. **Reporting** → exported artifacts, wrote findings, and maintained chain-of-custody.

For the full narrative, see `docs/methodology.md` and `docs/artifact-findings.md`.

---

## 📄 Full Report
👉 [`report/Sanjay_Samala_Forensic_Final_Report.pdf`](report/Sanjay_Samala_Forensic_Final_Report.pdf)

---

## 🔖 License
MIT License — educational and defensive forensic training purposes only.

---

👤 **Author:** Sanjay Kumar Samala  
🎓 Graduate Teaching Assistant | Cybersecurity • Digital Forensics • Malware RE • Cloud Security
