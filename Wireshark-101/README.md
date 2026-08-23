Structure of a TryHackMe Writeup (for GitHub)

A good writeup has two goals: show your methodology and demonstrate your thinking, not just paste answers. Recruiters and hiring managers look for this.

📁 Recommended GitHub Repo Structure
THM-Writeups/
├── README.md               ← Index of all rooms
├── Wireshark-101/
│   ├── README.md           ← The actual writeup
│   └── screenshots/        ← Evidence images
├── Nmap/
│   └── README.md
└── ...
📝 Writeup Template (Wireshark Room Example)

Here's the Markdown template you should follow:

markdown
# 🔍 TryHackMe — Wireshark: The Basics

| Field         | Details                              |
|---------------|--------------------------------------|
| Platform      | TryHackMe                            |
| Room          | Wireshark: The Basics                |
| Difficulty    | Easy                                 |
| Category      | Network Analysis / SOC               |
| Date          | August 2026                          |
| Status        | ✅ Completed                          |

---

## 📌 Room Overview

Brief 2–3 line summary of what the room covers.  
> e.g., "This room introduces Wireshark for packet capture analysis, filtering traffic,
> and identifying suspicious patterns — core skills for a L1 SOC Analyst."

---

## 🎯 Learning Objectives

- Understand how to open and navigate .pcap files
- Apply display filters to isolate traffic
- Identify protocols and anomalies in packet captures
- Extract files/credentials from traffic

---

## 🧰 Tools Used

| Tool       | Purpose                    |
|------------|----------------------------|
| Wireshark  | Packet capture analysis    |
| tshark     | CLI-based packet analysis  |

---

## 📖 Walkthrough

### Task 1 — Introduction

Brief description of what the task covers.

**Key Concept:** What Wireshark is and why it matters in SOC work.

---

### Task 2 — Tool Overview

**Question:** What is the name of the packet detail pane?

**Approach:**
Explain *how* you found it — don't just give the answer.
> "Opened Wireshark → observed the three main panels: Packet List, Packet Details,
> and Packet Bytes. The middle pane is the Packet Detail pane."

**Answer:** `Packet Details`

📸 *(Screenshot: wireshark-panels.png)*

---

### Task 3 — Packet Filtering

**Question:** Filter HTTP traffic. How many packets are shown?

**Filter Used:**

http


**Approach:**
> "Applied the display filter `http` in the filter bar. The status bar at the bottom
> shows the filtered count."

**Answer:** `15`

---

## 🔑 Key Takeaways (SOC Relevance)

Connect what you learned to real-world L1 work:

- **Wireshark filters** let analysts quickly isolate C2 traffic, exfil, or lateral movement
- **Following TCP streams** reveals full session content — useful for detecting data theft
- **Protocol anomalies** (e.g., HTTP on port 4444) are red flags worth escalating

---

## 📚 References

- [Wireshark Display Filter Reference](https://www.wireshark.org/docs/dfref/)
- [TryHackMe Room Link](https://tryhackme.com/room/wiresharkthebasics)

---

## 🏅 Proof of Completion

![Badge or Certificate Screenshot](screenshots/completion.png)
✅ Golden Rules for a Quality Writeup

Show your reasoning, not just answers. For every question, write 1–2 lines on how you approached it. This is what separates a good writeup from an answer sheet.

Use screenshots liberally. Paste them in /screenshots/ and reference inline. Hiring managers love visual evidence.

Write the SOC relevance section. For every room, add a short "how does this apply to real SOC work?" section. This is what makes your writeup stand out for an L1 role specifically.

Keep it consistent. Use the same template across all rooms so your repo looks organized and professional.

Don't copy others' writeups. THM's rules prohibit sharing answers publicly while a room is active. Write in your own words; reference what filters/commands you used and why.

🗂️ Your Main README (Repo Index)

Your repo's root README.md should act as a dashboard:

markdown
# 🛡️ TryHackMe Writeups — [Your Name]

Preparing for L1 SOC Analyst | Blue Team Focus

## 📋 Completed Rooms

| Room | Category | Difficulty | Date |
|------|----------|------------|------|
| [Wireshark: The Basics](./Wireshark-101/) | Network Analysis | Easy | Aug 2026 |
| [Nmap](./Nmap/) | Recon | Easy | Aug 2026 |

## 🧠 Skills Demonstrated
`Wireshark` `Nmap` `Log Analysis` `SIEM` `Network Forensics`
💡 Pro Tips for L1 Job Hunting
Pin this repo to your GitHub profile
Link it directly in your resume under "Projects"
For each writeup, add a one-line description of what SOC skill it maps to (log analysis, alert triage, packet inspection, etc.)
Complete the SOC Level 1 learning path on THM — writeup each room in that path specifically

Want me to generate a ready-to-use README.md file for a specific Wireshark room so you can just fill in the answers?
