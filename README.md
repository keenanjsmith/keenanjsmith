# Hi, I'm Keenan 👋

I build identity and access infrastructure, with privileged access as the specialization.

I came to this from help desk. Years supporting Apple and Windows fleets, working tickets, and
doing remote support through BeyondTrust, which is a privileged access product even if nobody
called it that at the time. Identity was the layer underneath every problem I touched, so I went
and learned it properly instead of working around it.

Everything below is built by hand and documented. When something breaks, I write down what broke
and why, because that is the part every tutorial leaves out.

---

## 🔐 Privileged access

**[cyberark-pam-lab](https://github.com/keenanjsmith/cyberark-pam-lab)**

A working PAM environment built from free components. A credential vault that stores and rotates
privileged accounts under policy, and a session proxy that brokers and records every SSH and RDP
session to two isolated targets.

- Access control defined as code. Two machine identities against the same credentials, one with
  `update` and one without
- The boundary tested rather than asserted: the application identity authenticates, reads the
  credential, and is refused at the write
- Targets on a network with no default route at all, proven three ways
- Every session recorded to its own directory, replayable with a timestamped keystroke log and
  activity histogram
- Full runbook, a build log of seven failures with root causes, and an honest limits section
  naming eight lab shortcuts

Conjur OSS where the Digital Vault goes, Apache Guacamole where PSM goes. Not CyberArk, whose
binaries sit behind a customer portal. The same architecture from components that behave the same
way mechanically.

**[teleport-access-lab](https://github.com/keenanjsmith/teleport-access-lab)**

The other side of PAM. Where the vault lab stores and rotates standing credentials, this one gets
rid of them. Teleport Community Edition in front of three Linux servers and a PostgreSQL database,
where every login needs MFA, every pass is a short-lived certificate, and every session is recorded.

- Least privilege as code. A developer role scoped by label to dev servers and one non-admin
  Linux account, which can't even see prod or the database
- Servers join through outbound reverse tunnels, so every firewall denies all incoming traffic and
  access still works
- Sessions played back from the audit side, and the exact SQL query captured with who ran it and
  as which database user
- PostgreSQL that only accepts Teleport-signed certificates, reached through a read-only user
- Four runbooks written for someone who has never used Linux, a build log of nine problems with
  fixes, and a lab shortcuts section naming ten

---

## 🗂️ Identity and directory services

**[active-directory-project](https://github.com/keenanjsmith/active-directory-project)**

A Windows Server 2022 domain built from scratch in VirtualBox. Domain controller running AD DS,
DNS, DHCP, and RRAS/NAT, roughly 1000 provisioned accounts, and a Windows 11 Enterprise client
that joins and authenticates against it.

- Four extension labs: DNS records and resolver cache, file shares and NTFS permissions, account
  lockout policy, and traffic analysis with Wireshark and Windows Firewall
- Build log of 24 entries with exact error text
- Corrected publicly after a reader caught an error in the DNS writeup

Built on Josh Madakor's Active Directory tutorial and carried well past it.

**[azure-iam-lab](https://github.com/keenanjsmith/azure-iam-lab)**

End-to-end Azure tenant build with identity controls applied. Entra ID configuration, OUs, domain
join, admin accounts, Conditional Access, and Identity Protection.

---

## 🎫 Service operations

**[osticket-lab](https://github.com/keenanjsmith/osticket-lab)**

A help desk platform installed on Windows Server and worked end to end across multiple roles and
accounts.

- Department controls visibility, role controls capability, and the two are independent
- SLA clocks measure from ticket creation, not first response, proved live when a Sev-A timer
  expired mid-lab
- Corrected after a reader flagged the wrong file permission principal

---

## 🛠️ Tools

**[cert-quiz-bot](https://github.com/keenanjsmith/cert-quiz-bot)**

A Discord bot running daily certification practice questions for my cohort. Python, discord.py,
and SQLite, with swappable question banks, answer positions shuffled at post time, user stats, and
a leaderboard.

Built it because my classmates needed it, and about forty people use it.

---

## 🚧 Next

- **Azure and Terraform series.** Cost management, secure network infrastructure, and Entra ID
  access governance, all as code

---

## 📜 Certifications

| | |
|---|---|
| CompTIA Security+ | Earned |
| CompTIA A+ Core 1 (220-1201) | July 2026 |
| CompTIA A+ Core 2 (220-1202) | August 2026 |
| Microsoft Azure Fundamentals (AZ-900) | September 2026 |
| Microsoft Azure AI Fundamentals (AI-901) | September 2026 |

Currently enrolled in an IT Systems Administration program.

---

## 🤖 On AI

I use AI as a working partner and I say so in every repo. The
[disclosure in the PAM lab](https://github.com/keenanjsmith/cyberark-pam-lab/blob/master/HOW-I-USED-AI.md)
includes a section on what the model got wrong and I caught by running it.

How someone uses these tools says more than whether they use them, and hiding it would be the
wrong call.

---

## 📫 Reach me

[LinkedIn](https://www.linkedin.com/in/connect-with-keenan)
