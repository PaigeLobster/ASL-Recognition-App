
The chosen topic is week 11, continuous (CSR) versus individual sign recognition (ISR). 

👥 TARGET USERS
For anyone learning or practicing ASL fingerspelling:
·	ASL learners & students seeking self-directed practice
·	Deaf / hard-of-hearing individuals using fingerspelling digitally
·	Hearing people communicating with Deaf family or friends
·	K–12 / university ASL and Deaf Studies courses
·	Accessibility researchers and AAC practitioners

Recognizes individual static letters (manual alphabet) — not full ASL signs or words.

⚙️ INSTALL & RUN
Single HTML file — no build step, no install.
Requirements:
·	Chrome / Edge / Firefox 90+, or Safari 16.4+
·	Any webcam (720p+ recommended)
·	Internet once to fetch ~8 MB model, then cached

Run options:
① Open asl-recognition.html directly in browser
② Or serve locally:
   python -m http.server 8080
   npx serve .
Click Start Camera → allow webcam. App auto-loads WASM runtime, hand model, then streams live detection.

♿ ACCESSIBILITY
·	Dark high-contrast theme — teal/purple on #060810 exceeds WCAG AA 4.5:1
·	Letter shown at 60–72 px in two locations simultaneously for low-vision users
·	Hold-to-add (1.5 s): no clicks required; purple progress bar gives timing feedback
·	Fully silent — all feedback is visual; suits Deaf / hard-of-hearing users
·	Normalized landmark coordinates make classifier skin-tone agnostic
·	All interactive targets ≥ 44×44 px per WCAG 2.5.5

Known gaps:
No ARIA annotations yet. J/Z fingerspelled letters need motion (static approx. only).

📊 EVALUATION
Around 20% accurate with a high chance that any fingerspelled letter will be understood as C.
Top confusable pairs: A↔S, U↔R, M↔N, G↔Q, C↔∞

⚖️ ETHICS
Attribution
·	Inspired by ASL Citizen (UW, 2023) — built with 83 Deaf signers under informed consent
·	No dataset content redistributed; uses only open-source MediaPipe landmarks

Privacy
·	100% on-device (WebAssembly). No video, frames, or landmarks transmitted or stored

Bias & Limits
·	Tested on limited signers; natural variation not fully covered
·	Do not use for grading, hiring, or interpreting

Appropriate use:
✓  Practice, education, research, prototyping
✗  Assessment, admissions, interpreter replacement
Building on this? Consult Deaf community members and follow the ASL Citizen ethical framework.







