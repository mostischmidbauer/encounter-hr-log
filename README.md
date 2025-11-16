# HCP Anti-Deepfake Liveness & Licence Verification Prototype  
### A research-only optical-liveness security layer for telehealth, insurers & regulators  
**Author:** Moustafa Mohammed Elsayed Elsayed Ali  
**Languages:** EN / DE / ES  
**Version:** 1.0

---

## 📌 Overview

This project provides a **client-only, browser-based anti-deepfake liveness indicator** for verifying the presence and validity of **healthcare professionals (HCPs)** during virtual, cross-border telehealth activity.

The tool uses **remote photoplethysmography (rPPG)** extracted from webcam video to detect:

- Real physiological micro-oscillations  
- Multi-region coherence (forehead + cheeks)  
- Signal-quality SNR  
- Cross-region correlation  
- Liveness score (0–100)  
- Indicators of **spoofing, replay, synthetic video or deepfakes**

It also captures **licence metadata** and generates an **audit-ready CSV log** for insurers, ministries, and compliance units.

⚠️ **NOT a medical device.**  
⚠️ **NOT identity verification.**  
⚠️ **NOT for clinical decision-making.**  
This is an **administrative security-support layer only.**

---

## 🧠 Key Features

- ✔ Pure HTML/JS (no backend, no cloud, no dependencies)  
- ✔ EN–DE–ES language support  
- ✔ Remote PPG extraction (green-channel rPPG)  
- ✔ Multi-ROI physiological coherence scoring  
- ✔ Anti-deepfake liveness score (PASS/BORDERLINE/SUSPICIOUS)  
- ✔ HCP licence form & timestamped logs  
- ✔ CSV export for regulators/insurers  
- ✔ GDPR/EHDS-compliant local processing  
- ✔ Deployable on GitHub Pages / intranet instantly  

---

## 🖥 Architecture

Browser
├─ Webcam (WebRTC getUserMedia)
├─ Canvas frame capture (60 FPS)
├─ ROI segmentation (forehead, cheek L, cheek R)
├─ rPPG pipeline (green channel mean → smoothing → peak detection)
├─ HR estimation
├─ Signal quality (SNR-like)
├─ ROI correlation (Pearson)
├─ Liveness score (weighted)
├─ LocalStorage logging
└─ CSV Export

Use Cases

Telehealth provider onboarding

Start-of-session verification for remote HCPs

Fraud-prevention checks for insurers

Licensing & compliance audits

Cross-border health workforce supervision

MoH credential integrity monitoring

Randomized high-risk consultation checks
🛡 Compliance Positioning (Summary)
FDA (USA)

NOT a medical device under 21 USC 321(h)

NOT clinical decision support

NOT identity verification

Falls under Digital Health Enforcement Discretion: Administrative Use

EU (MDR/IVDR)

Not a medical device under MDR 2017/745

Not IVDR

No CE marking required

Falls under EHDS/NIS2 administrative support tool

GDPR/EHDS

Local-only data

No biometric identification

No patient data

No cloud transfer

⚠️ Limitations

Not a replacement for official licence verification

Not an identity proofing system

Not accurate in low lighting or excessive motion

Can produce false positives/false negatives

Multi-ROI coherence is advisory only

🤝 Contribution Guidelines

PRs are welcome for:

New signal-processing techniques

Challenge-response tests (blink, nod, smile)

Infrared / depth-sensor support

Additional languages

📄 License

MIT License
Contact

Author:
Moustafa Mohammed Elsayed Elsayed Ali
📧 mostischmidbauer@web.de

📧 agentic@virtualcaresolution.de

📍 Germany

### ✨ `/docs/index.html`
(Professional landing page for GitHub Pages)

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>HCP Anti-Deepfake Liveness & Licence Verification – Docs</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<header>
  <h1>HCP Anti-Deepfake Liveness & Licence Verification Prototype</h1>
  <h2>Documentation Portal (EN–DE–ES)</h2>
</header>

<nav>
  <a href="#overview">Overview</a>
  <a href="#architecture">Architecture</a>
  <a href="#liveness">Liveness Algorithm</a>
  <a href="#workflow">Integration Workflow</a>
  <a href="#compliance">Regulatory Position</a>
  <a href="#downloads">Downloads</a>
</nav>

<section id="overview">
  <h2>1. Overview</h2>
  <p>This documentation describes the anti-deepfake liveness verification layer for telehealth compliance, licensing audits and cross-border HCP supervision.</p>
</section>

<section id="architecture">
  <h2>2. Architecture</h2>
  <pre>
Browser (Client-only)
 ├ WebRTC (Camera)
 ├ ROI Extraction
 ├ rPPG Pipeline
 ├ Liveness Scoring
 └ Logs + CSV Export
  </pre>
</section>

<section id="liveness">
  <h2>3. Liveness Algorithm</h2>
  <p>Describes multi-ROI rPPG extraction, correlation mapping, SNR evaluation and weighted liveness scoring.</p>
</section>

<section id="workflow">
  <h2>4. Integration Workflow</h2>
  <ol>
    <li>HCP enters licence data</li>
    <li>Start camera</li>
    <li>Run Anti-Deepfake Check (~30s)</li>
    <li>Save event → localStorage</li>
    <li>Export CSV for regulator/insurer</li>
  </ol>
</section>

<section id="compliance">
  <h2>5. Regulatory Position</h2>
  <p>Non-medical, administrative-use only. Not SaMD. Not MDR. Not identity verification.</p>
</section>

<section id="downloads">
  <h2>Downloads</h2>
  <ul>
    <li><a href="../Integration_Guide.pdf">Integration Guide PDF</a></li>
    <li><a href="../Regulatory_Technical_File.pdf">Regulatory Technical File</a></li>
    <li><a href="../Risk_Management_File.pdf">ISO 14971 Risk File</a></li>
    <li><a href="../GDPR_EHDS_DPIA.pdf">GDPR/EHDS DPIA</a></li>
  </ul>
</section>

<footer>
  <p>© 2025 – Moustafa Mohammed Elsayed Elsayed Ali</p>
</footer>

</body>
</html>
