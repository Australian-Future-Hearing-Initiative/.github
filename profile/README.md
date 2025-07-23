# AFHI Web Demos – Known Issues, Feature Roadmap, and Version History

This repository serves as the **central hub** for the Australian Future Hearing Initiative (AFHI) web-based hearing tests. It contains a summary of available test deployments, known issues, planned features, and a detailed version history.

---

## 🌐 Additional Information

For related context and perspectives connected to this project, you may find this TEDx talk by Simon Carlile of interest:
🎥 [**The Future of Hearing – TEDxSydney**](https://www.youtube.com/watch?v=Vup_coDYOoo)

---

## 🚀 Release Summary

We now have **three main releases**:

| Release  | Purpose                                       | Notes                             |
| -------- | --------------------------------------------- | --------------------------------- |
| **Main** | AFHI team's active development                | May restart or change at any time |
| **NAL**  | Configured for clinical testing (e.g. at NAL) | Stable during studies             |
| **UX**   | Configured for UX testing (e.g. at Google)    | Stable during studies             |

**Additional releases:**

* **Stable:** Usually a few versions behind Main; used to compare behavior.
* **Dev:** Internal only; used for early-stage testing.

---

## 🛠️ Known Issues & Future Features

Grouped by test type and ranked by priority:

### 🎧 Pure-Tone Audiometry (PTA)

| Priority | Description                                                         |
| -------- | ------------------------------------------------------------------- |
| P1       | Add second run of 1 kHz for left ear (Hughson-Westlake convention)  |
| P1       | Display PTA4 / hearing score and log it to results                  |
| P2       | Audio indication when test is over                                  |
| P2       | Adaptively adjust response window based on user reaction times      |
| P2       | Improve MAE metric – reduce quantization noise (5 dB steps)         |
| P2       | Add special symbols for max hearing loss (e.g. circles with arrows) |
| N/A      | Streamlit error: "Bad message format" – may be resolved already     |
| N/A      | Overlapping stimuli – no plan to address unless it recurs           |

### 📈 Categorical Loudness Scaling (CLS)

| Priority | Description                                                |
| -------- | ---------------------------------------------------------- |
| P1       | Map results to audiogram (convert y-axis to dBHL and flip) |

### 🔤 Consonant Confusion Test (VCV)

| Priority | Description                                             |
| -------- | ------------------------------------------------------- |
| P2       | Previously selected letter remains red – minor UI issue |
| N/A      | Background noise varies by VCV – intended behavior      |

### 🎛️ Tone Generator

| Priority | Description                                 |
| -------- | ------------------------------------------- |
| P1       | Add option to download WAV file of the tone |
| P1       | Add dither and colored noise options        |

### ⚙️ General App Features

| Priority | Description                                            |
| -------- | ------------------------------------------------------ |
| P1       | Add app-wide debugging/logging system                  |
| P2       | Add progress bars to PTA and Pip PTA                   |
| P2       | Remove Streamlit cloud footer                          |
| N/A      | Chrome audio indicator – not significant enough to fix |

---

## 📌 Urgent Changes for NAL Study

* VCV demo: fix output volume at 65 dB

## 🔄 Non-Urgent

* Document MP3 quality specifications for the VCV test

---

## 📦 Version History

<details>
<summary>Click to expand full version history</summary>

### ✅ Next Release

* PTA: Separated calibration for HW vs Adaptive PTA
* All: Log system volume when app is used locally

### 🔖 Release 4.1.0

* VCV: Increased button/font size
* CLS: Save loudness model parameters by ear
* All: Environment label added (UX, NAL, etc.)
* All: Streamlit version update to fix bugs

### 🔖 Release 4.0.0

* CLS: Advanced dynamic tone fitting mode
* VCV: Default settings updates
* All: Added APP\_TARGET\_AUDIENCE environment variable

### 🔖 Release 3.4.1

* CLS: Max iterations safeguard
* PTA: Log method used (HW or Adaptive)
* All: Log app version number

### 🔖 Release 3.4.0

* Adaptive PTA method added

### 🔖 Release 3.3.0

* PTA: Fixed infinite loop bug
* VCV: Full binaural support

### 🔖 Release 3.2.0

* CLS: Model per ear, calibration fixes
* VCV: Updated instructions, standardized volume
* All: Consistent layout + freeze settings during test

### 🔖 Release 3.1.0

* CLS: Volume calibration, basic/advanced mode toggle

### 🔖 Release 3.0.0

* Standardized data download process
* All: Graphs & audiograms included in ZIPs

### 🔖 Release 2.9.4 → 2.2.3

(Summarized)

* Numerous UI fixes, logic improvements, calibration enhancements, and tone generator utilities

</details>

---

## 🤝 Contributing

We welcome contributions to improve our tools and demos.

### Guidelines

* Use clear and consistent naming conventions.
* Write modular, testable code where possible.
* Submit all changes via pull requests.
* Include a short description and relevant context in your PRs.
* Follow the [MIT License](#license) terms.

If you’re contributing a new demo or test, we recommend:

* Using Streamlit or another web-friendly framework
* Writing a short README with setup instructions
* Keeping dependencies minimal

For major changes or ideas, feel free to reach out to the team first via email.

---

## 📢 Contact

This repo is maintained by the AFHI team. For questions or collaboration:

* Simon Carlile – [scarille@google.com](mailto:scarille@google.com)
* Julian Maclaren – [jmaclaren@xwf.google.com](mailto:jmaclaren@xwf.google.com)

---

## 📄 License

MIT License – Refer to individual sub-repos for more details.
