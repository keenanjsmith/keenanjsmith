# Hi, I'm Keenan 👋

I'm building toward identity and access management, with privileged access as the target.

I came to this from help desk. Years of supporting Apple and Windows fleets, working tickets,
and doing remote support through BeyondTrust, which is a privileged access product even if
nobody called it that at the time. Identity was the layer underneath every problem I touched,
so I decided to go learn it properly instead of working around it.

Everything below is built by hand and documented. When something breaks, I write down what
broke and what fixed it, because that is the part every tutorial leaves out.

---

## 🔐 Identity projects

### On-premises

**[active-directory-project](https://github.com/keenanjsmith/active-directory-project)**

A working Windows Server 2022 domain built from scratch in VirtualBox. Domain controller
running AD DS, DNS, DHCP, and RRAS/NAT, roughly 1000 provisioned user accounts, and a Windows
11 Enterprise client that joins the domain and authenticates against it.

- Full runbook with 25 verification screenshots
- Build log of all 14 things that broke, with exact error text and fixes
- Honest write-up of the shortcuts the lab takes and why they would fail in production
- Built on Server 2022, Windows 11, and VirtualBox 7, where most guides for this stop at 2019

Built on Josh Madakor's Active Directory tutorial and carried forward from there.

### Cloud

**[azure-iam-lab](https://github.com/keenanjsmith/azure-iam-lab)**

End-to-end Azure tenant build with real identity controls applied.

- Resource group, VNet, and VM setup
- Microsoft Entra ID configuration, OUs, domain join, and admin accounts
- Conditional Access and Identity Protection
- Step-by-step documentation with screenshots, written for beginners

---

## 🛠️ Tools I've built

**[cert-quiz-bot](https://github.com/keenanjsmith/cert-quiz-bot)**

A Discord bot that runs daily CompTIA A+ Core 2 practice questions for my cohort. Python,
discord.py, and SQLite, with a question bank weighted to the real exam domain percentages,
user stat tracking, and a leaderboard.

Built it because my classmates needed it, and about forty people use it.

---

## 🚧 In progress

- **Extension labs** on the same domain: Group Policy, NTFS versus share permissions, account
  lockout policy, Windows Firewall rules
- **osTicket build** — the help desk half of the story
- **CyberArk PAM lab** — Conjur OSS vault with credential rotation, plus Apache Guacamole as a
  session-recording bastion. Enterprise-grade privileged access on free open source components,
  no license required.

---

## 📜 Certifications

| | |
|---|---|
| CompTIA Security+ | Earned |
| CompTIA A+ Core 1 (220-1201) | Passed |
| CompTIA A+ Core 2 (220-1202) | In progress |

Currently enrolled in an IT Systems Administration program.

---

## 🤖 On AI

I use AI as a working partner and I say so in every repo, with a table breaking down exactly
which parts it touched. The building, the troubleshooting, and the verification are mine. The
documentation is collaborative.

I think how someone uses these tools says more than whether they use them, and hiding it would
be the wrong call.

---

## 📫 Reach me

[LinkedIn](https://www.linkedin.com/in/connect-with-keenan)
