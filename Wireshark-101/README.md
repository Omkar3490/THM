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

Wireshark is an open-source, cross-platform network packet analyser tool capable of sniffing and investigating live traffic and inspecting packet captures (PCAP). It is commonly used as one of the best packet analysis tools. In this room, we will look at the basics of Wireshark and use it to perform fundamental packet analysis.
---

## 🎯 Learning Objectives

- Navigate and configure Wireshark
- Inspect packets and discover information from the different layers of TCP/IP
- Apply display filters

---

## 🧰 Tools Used

| Tool       | Purpose                    |
|------------|----------------------------|
| Wireshark  | Packet capture analysis    |
     

---

## 📖 Walkthrough

### Task 1 — Introduction

Brief description of what the task covers.

**Key Concept:** What Wireshark is and why it matters in SOC work.

---

### Task 2 — Tool Overview

Wireshark is one of the most potent traffic analyser tools available in the wild. There are multiple purposes for its use:

Detecting and troubleshooting network problems, such as network load failure points and congestion.
Detecting security anomalies, such as rogue hosts, abnormal port usage, and suspicious traffic.
Investigating and learning protocol details, such as response codes and payload data.

**Question:**Read the "capture file comments". What is the flag?

**Approach:**
> "Opened Wireshark → statistics → capture file properties → capture file comments section


**Answer:** `TryHackMe_Wireshark_Demo`

📸 *(Screenshot: wireshark-panels.png)*

---
**Question:**What is the total number of packets?
**Approach:**
> "Opened Wireshark → shows at bottom right side total number of packets
**Answer:*58620* ``

**Question:**What is the SHA256 hash value of the capture file?
**Approach:**
> "Opened Wireshark → statistics → capture file properties → Hash (SHA256)
**Answer:*f446de335565fb0b0ee5e5a3266703c778b2f3dfad7efeaeccb2da5641a6d6eb* ``

📸 *(Screenshot: wireshark-panels.png)*

### Task 2 - Packet dissection

**Question:** View packet number 38. Which markup language is used under the HTTP protocol?

**Approach:**
> at packet details section → application layer(HTTP) → application data(XML)

**Answer:** `eXtensible markup language`
📸 *(Screenshot: wireshark-panels.png)*
---
**Question:** What is the arrival date of the packet? (Answer format: Month/Day/Year)?
**Approach:**
> time section
**Answer:** `05/13/2004`

**Question:** What is the TTL value?
**Approach:**
> packet details pane → Internet Protocol Version 4 → Time to Live field
**Answer:** `47`
📸 *(Screenshot: wireshark-panels.png)*

**Question:** What is the TCP payload size?
**Approach:**
> packet details pane → Transmission control protocol → under the time stamp section
**Answer:** `424`
📸 *(Screenshot: wireshark-panels.png)*

**Question:** What is the e-tag value?
**Approach:**
> packet details pane → Hypertext transfer protocol → etag value field
**Answer:** `9a01a-4696-7e354b00`
📸 *(Screenshot: wireshark-panels.png)*

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
