# Open-Linux-Software-

- Name: Swarup Rajkumar Yevlekar
- Roll Number: 24BAS10036
- Course: Open Source Software (OSS NGMC)
- Chosen Software for Audit: `Git`

This repository contains all required deliverables for **The Open Source Audit** capstone:
- Five shell scripts (`.sh`) with comments and Linux-focused logic
- Documentation to run each script
- Report template aligned with Parts A-D from the assignment

# The Open Source Audit Report: Git

---

## Part A — Origin and Philosophy (Units 1 & 2)

### A1. The problem Git was created to solve (Detailed Origin Story)

In early 2000s, large-scale software development faced a serious coordination problem. The Linux kernel, one of the largest collaborative software projects in the world, was being developed by thousands of contributors across different countries and time zones. Managing code changes, tracking history, and ensuring stability were extremely difficult tasks.

Before Git, the Linux community used a proprietary tool called BitKeeper. While it offered advanced version control features, it conflicted with the philosophy of the Linux ecosystem because it was not open source. Developers were dependent on a tool they could not fully control or modify.

This dependency became a major issue when disagreements arose between the Linux community and the company maintaining BitKeeper. As a result, free access to the tool was revoked. Overnight, the Linux kernel lost its primary development system.

At that time, other version control systems existed, such as CVS and Subversion, but they had significant limitations:

* They were centralized, meaning all developers depended on a single server.
* They were slow when handling large repositories.
* They struggled with branching and merging.
* They were not designed for distributed collaboration.

Linus Torvalds decided to solve this problem himself. Instead of patching existing tools, he created a completely new system with a different design philosophy. His goals were:

* Speed: Operations should be extremely fast.
* Distributed design: Every user should have a complete copy of the repository.
* Data integrity: Changes must be cryptographically secure.
* Scalability: The system must handle massive projects like Linux.

Git was developed in just a few weeks, which is remarkable given its impact. Its distributed nature removed reliance on a central server, allowing developers to work independently and merge changes later. This was a revolutionary shift in how version control systems worked.

Torvalds chose to release Git as open source to avoid repeating the BitKeeper problem. By making it open, no company could restrict its use in the future. This decision ensured long-term freedom and sustainability.

Git’s origin is not just technical—it is philosophical. It represents a rejection of dependency on closed systems and a commitment to developer freedom.

---

### A2. The license — what it actually says (Deep Analysis)

Git is released under the GNU General Public License version 2 (GPLv2). This license is designed to guarantee freedom rather than just free usage.

#### The Four Freedoms of Free Software

1. Freedom to run the program for any purpose.
2. Freedom to study how the program works.
3. Freedom to modify the program.
4. Freedom to distribute copies (original or modified).

Git satisfies all four freedoms. Any individual or organization can use Git without restriction, inspect its source code, modify it, and share it.

#### Can companies modify and sell Git?

Yes, but with conditions. Under GPLv2:

* A company can modify Git and sell it.
* However, if they distribute the modified version, they must also release the source code.

This ensures that improvements remain accessible to the community. This principle is called **copyleft**.

#### GPL vs MIT License

| Feature              | GPL License             | MIT License   |
| -------------------- | ----------------------- | ------------- |
| Code freedom         | Strong (must stay open) | Flexible      |
| Commercial use       | Allowed with conditions | Fully allowed |
| Modification sharing | Mandatory               | Optional      |

GPL protects openness, while MIT encourages adoption.

If I were to build software:

* I would choose GPL if I want to protect community ownership.
* I would choose MIT if I want widespread commercial use.

#### Free Beer vs Free Freedom

* Free beer: No cost.
* Free freedom: Control over the software.

Git represents **freedom**, not just zero cost. Developers can shape and evolve it.

---

### A3. The ethics of open source (Critical Thinking)

Open source raises complex ethical questions.

#### Should all software be open source?

**Arguments for:**

* Transparency builds trust.
* Bugs and vulnerabilities can be identified quickly.
* Encourages collaboration.

**Arguments against:**

* Companies lose competitive advantage.
* Sensitive systems (e.g., security software) may be risky if fully open.
* Developers may struggle to monetize their work.

#### Is it ethical for companies to profit from open source?

Companies like Red Hat and Google rely heavily on open-source tools. This raises fairness concerns.

Ethically, it is acceptable if companies:

* Contribute back to the community
* Improve the software
* Support development financially

However, using open-source purely for profit without contribution can be seen as exploitation.

#### Standing on the shoulders of giants

This phrase means building on existing knowledge. In software:

* Open source accelerates innovation
* Developers avoid reinventing basic tools
* More time is spent solving new problems

Rather than reducing originality, open source expands possibilities.

---

## Part B — Linux Footprint (Unit 2)

### Installation Method

On Debian-based systems:

```
sudo apt update
sudo apt install git
```

On RPM-based systems:

```
sudo yum install git
```

Git can also be compiled from source for custom configurations.

---

### Key Directories

* Binary: `/usr/bin/git`
* System config: `/etc/gitconfig`
* User config: `~/.gitconfig`
* Repository metadata: `.git/`
* Logs: `.git/logs/`

The `.git` directory is the core of Git—it stores commits, branches, and history.

---

### User and Group

Git runs under the current user. It does not require a dedicated system user.

This matters for security because:

* Access is controlled via file permissions
* Unauthorized users cannot modify repositories

---

### Service Management

Git is not a daemon by default. However, in server setups:

```
sudo systemctl start git-daemon
sudo systemctl stop git-daemon
sudo systemctl restart git-daemon
```

Git is often used over SSH rather than as a standalone service.

---

### Update Model

Updates are delivered through:

* Linux package managers
* Community contributions
* Security patches reviewed globally

Because the code is open, vulnerabilities are identified faster.

---

## Part C — The FOSS Ecosystem (Units 3 & 4)

### Dependencies

Git relies on:

* C programming language
* zlib (compression)
* OpenSSL (security)

---

### What Git Has Enabled

Git has revolutionized development:

* Platforms like GitHub and GitLab
* Distributed teamwork
* Open collaboration

It is the backbone of modern DevOps workflows.

---

### Role in Web Development

Git is not part of LAMP directly, but:

* Manages source code
* Supports deployment pipelines
* Enables version tracking

---

### Community and Governance

Git is maintained by a global developer community.

Governance model:

* Contributions reviewed via mailing lists
* Maintainers approve changes
* No single corporate control

This ensures neutrality and long-term sustainability.

---

## Part D — Open Source vs Proprietary (Critical Analysis)

| Dimension   | Git (Open Source) | Proprietary Alternative (Perforce) |
| ----------- | ----------------- | ---------------------------------- |
| Cost        | Free              | Expensive                          |
| Security    | Transparent       | Closed                             |
| Support     | Community         | Paid support                       |
| Flexibility | High              | Limited                            |
| Control     | Community-driven  | Corporate                          |

---

### Final Conclusion (Expanded)

Git is one of the most important tools in modern software development. Its distributed architecture, speed, and reliability make it suitable for both individuals and large organizations.

While proprietary tools may offer better dedicated support and simplified workflows, they lack the transparency and freedom that Git provides.

I would strongly recommend Git for real-world deployment because:

* It is scalable
* It is secure
* It has a massive ecosystem

I would also be willing to contribute to Git or its ecosystem because it represents a collaborative approach to problem-solving and innovation.

---

**End of Report**
