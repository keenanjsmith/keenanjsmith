# Keenan Smith

Air Force veteran working in IT support and building toward identity and access management
engineering. San Antonio, TX.

I build infrastructure labs on real hardware, document what breaks, and publish the runbook along
with the failures. The build logs are the point. Anyone can follow a tutorial that works. What is
worth writing down is what happens when it doesn't.

---

## Projects

### [active-directory-project](https://github.com/keenanjsmith/active-directory-project)
A Windows Server 2022 domain built from scratch on VirtualBox: AD DS, DNS, DHCP, NAT routing, and
1000 bulk-provisioned users. Four extension labs on top of the core build.

| Lab | What it covers |
| --- | --- |
| DNS records and the resolver cache | A records, CNAMEs, cache staleness, and why flushing DNS does not fix a hosts file entry |
| File shares and NTFS permissions | Share versus NTFS, tested as an actual standard user rather than assumed |
| Account lockout and password management | Group Policy lockout, unlock, reset, disable, and the event IDs each one produces |
| Network traffic and Windows Firewall | Five protocols captured live in Wireshark, plus a firewall rule to break one on purpose |

Findings include a domain controller that audits the administrator unlocking an account but not the
failed passwords that locked it, and an account lockout GPO that silently does nothing when linked
to an OU instead of the domain root.

### [osticket-lab](https://github.com/keenanjsmith/osticket-lab)
A help desk ticketing system built from nothing: IIS with CGI, PHP 7.3, MySQL 5.5, and osTicket on
top. Four layers, each configured by hand, then hardened afterward.

Includes the security step most walkthroughs treat as housekeeping, and 37 minutes lost to Windows
Explorer silently dropping three folders from a zip archive.

### [azure-iam-lab](https://github.com/keenanjsmith/azure-iam-lab)
An identity and access management lab in Azure Entra ID: users, groups, role assignments with least
privilege, device join, Identity Protection, and Conditional Access baseline policies.

### [cert-quiz-bot](https://github.com/keenanjsmith/cert-quiz-bot)
A Discord bot that posts a daily CompTIA A+ Core 2 question to my cohort's study server. Python,
SQLite, discord.py. Question bank weighted to the real domain percentages, with a two-pass
no-repeat picker and per-user progress tracking.

---

## Certifications

- CompTIA Security+
- CompTIA A+ Core 1 (July 2026)
- CompTIA A+ Core 2, targeted September 2026

Currently enrolled in the IT Systems Administration program at MyComputerCareer.

---

## On AI

The documentation in these repositories is drafted with AI assistance and I say so in every repo.
Every step was executed on real infrastructure, every screenshot is from my own build, and every
problem in the build logs is one I actually hit.

Using the tooling well and being straightforward about it is more useful than pretending otherwise.

---

## Coming next

Post-install configuration and ticket lifecycle labs on osTicket, then a CyberArk privileged access
management lab using Conjur OSS and Apache Guacamole.

---

[LinkedIn](https://www.linkedin.com/in/connect-with-keenan)
