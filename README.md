# Christian Heimes (he/him)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-christianheimes-0077B5?style=flat-square&logo=linkedin)](https://de.linkedin.com/in/christianheimes)
[![PyPI](https://img.shields.io/badge/PyPI-tiran-3775A9?style=flat-square&logo=pypi)](https://pypi.org/user/tiran/)
[![SpeakerDeck](https://img.shields.io/badge/SpeakerDeck-tiran-009287?style=flat-square&logo=speakerdeck)](https://speakerdeck.com/tiran)

📍 Based in Hamburg, Germany 🇩🇪 · working remotely

I'm a software engineer at **Red Hat** and a Python core developer, with more than
25 years of open-source experience. My work centers on **Python packaging and build
systems, security and cryptography, and AI/ML infrastructure**, grounded in a long
track record in the CPython standard library. Earlier in my career I built identity-
and secrets-management systems and contributed to the Zope and Plone web platforms.
My current focus is **building infrastructure for Red Hat's AI platform**.

---

## About Me

- 🤖 I currently build infrastructure for **Red Hat's AI platform** — packaging and
  distributing Python and ML software across CPU, GPU, and AI-accelerator targets.
- 📦 I have long-standing expertise in **Python packaging and build systems**, and
  I publish **[agent-skills](https://github.com/tiran/agent-skills)** to share that
  knowledge with other engineers.
- 🐍 **CPython core developer** since 2007; former maintainer of the `ssl` and
  `hashlib` modules and author of several security-focused PEPs.
- 🏅 **PSF Fellow** since 2008; emeritus member of the Python Security Response Team
  and the PSF Diversity & Inclusion Working Group.
- 🔒 Creator and maintainer of **[defusedxml](https://github.com/tiran/defusedxml)**,
  a library that hardens Python's XML parsers against bomb and XXE attacks.
- 🎩 Earlier at Red Hat, I worked across the identity stack — **FreeIPA / RHEL
  IdM**, **Custodia**, and **python-ldap** — and spent time as a Core Maintainer of
  **InstructLab**.
- 🐧 A Linux user since 1997 and a Python programmer since 2001.

---

## Areas of Expertise

| Area | Projects & Topics |
|---|---|
| 🤖 Red Hat AI | AI/ML build & distribution infrastructure, RHAI container images, accelerator wheel builds (CUDA/ROCm/Spyre), WheelNext |
| 📦 Python packaging | Wheel-build tooling (fromager), build backends, packaging utilities, agent skills |
| 🐍 Python & open source | CPython core development, PSF Fellow, `defusedxml`, PEP authorship |
| 🔒 Security & cryptography | CPython `ssl`/`hashlib`, OpenSSL, FIPS & system crypto-policies, pyca/cryptography |
| 🎩 Identity management | FreeIPA / RHEL IdM, Custodia, python-ldap, Dogtag PKI |
| 🕰️ Earlier career | Zope & Plone, Plone Foundation board |

---

## Selected Work

### 🤖 Red Hat AI

[![fromager Stars](https://img.shields.io/github/stars/python-wheel-build/fromager?style=flat-square&logo=github&label=fromager)](https://github.com/python-wheel-build/fromager)

As **Staff & Senior Principal Software Engineer for Red Hat's AI Platform
Ecosystem**, I build the infrastructure that packages and distributes Python and ML
software with optimized builds across accelerator targets — CPU, NVIDIA CUDA, AMD
ROCm, and IBM Spyre — published at
**[packages.redhat.com](https://packages.redhat.com/domains/public-rhai/distributions)**.
I also build the **Red Hat AI (RHAI) container images** used across Red Hat's AI
products, including
**[Red Hat AI Inference](https://www.redhat.com/en/products/ai/inference)** (vLLM).

The wheel-building toolchain behind this is open source.
**[fromager](https://github.com/python-wheel-build/fromager)** is the foundation — a
build-from-source wheel maker — supported by packaging and binary-analysis tools I
work on: **[elfdeps](https://pypi.org/project/elfdeps/)** (ELF shared-library
dependency analysis), **[retread](https://github.com/tiran/retread)** (compares
downstream wheel rebuilds against upstream to catch differences),
**[zipwire](https://github.com/tiran/zipwire)** (reads files from remote ZIP
archives over HTTP range requests), and
**[torch-abi-audit](https://github.com/Quansight/torch-abi-audit)** (audits
extensions for PyTorch and CPython stable-ABI compliance).

I'm Red Hat's liaison to **[WheelNext](https://wheelnext.dev/)**, the cross-industry
effort to evolve the Python wheel format — in particular **wheel variants**
([PEP 825](https://peps.python.org/pep-0825/)) for hardware-specific builds.

Earlier I was a Core Maintainer of
**[InstructLab](https://github.com/instructlab/instructlab)**, which uses
**Large-Scale Alignment for ChatBots (LAB)** — an alignment tuning method for LLMs
that leverages synthetic data — to train a model using custom taxonomy data. There I
worked on hardware enablement (Intel Gaudi, CUDA, Apple MLX) and build, test, and
packaging infrastructure. The project has since been refactored, with its core
building blocks (synthetic data generation and training) moving into separate
successor projects.

---

### 📦 Python Packaging & Build Systems

I have deep, long-standing expertise in Python packaging — build backends, the wheel
format, PEP-based packaging standards, and the tooling around building and
distributing packages (several of my packaging and binary-analysis tools are listed
in the Red Hat AI section above). I also publish
**[agent-skills](https://github.com/tiran/agent-skills)**, a collection of portable,
agent-neutral "skills" and playbooks for Python and packaging tasks. Each skill is
dual-purpose: a guide an engineer can read directly, and a structured instruction
set an AI coding assistant (such as Claude Code or Codex) can load to carry out a
specialized task — covering areas like build-backend selection, FIPS/crypto audits,
type-stub generation, and secure release pipelines. Together they distill two
decades of Python experience into reusable references for both people and agents.

---

### 🐍 CPython

[![GitHub Stars](https://img.shields.io/github/stars/python/cpython?style=flat-square&logo=github&label=Stars)](https://github.com/python/cpython)

I joined the CPython core team in late 2007 and have contributed close to 700 pull
requests over the years (among the most active contributors by commit count). For
much of that time I maintained the **`ssl` and `hashlib`** modules — including
porting them across the **OpenSSL 1.1 and 3.0** API transitions — and served on the
**Python Security Response Team (PSRT)**. My work also spans the wider standard
library, project governance, and CPython's **WebAssembly** port (the WASI and
Emscripten build targets).

PEPs I authored as sole creator:

- **[PEP 370](https://peps.python.org/pep-0370/)** — Per-user `site-packages`
  directory, the mechanism behind `pip install --user`.
- **[PEP 456](https://peps.python.org/pep-0456/)** — Secure and interchangeable
  hash algorithm (SipHash, now CPython's default string-hash algorithm).
- **[PEP 644](https://peps.python.org/pep-0644/)** — Require OpenSSL 1.1.1 or newer.

I also co-authored:

- **[PEP 452](https://peps.python.org/pep-0452/)** — the cryptographic
  hash-function API. (co-author)
- **[PEP 543](https://peps.python.org/pep-0543/)** — a unified TLS API. (co-author)
- **[PEP 594](https://peps.python.org/pep-0594/)** — "removing dead batteries."
  (co-author)

---

### 🔒 Security & Cryptography

[![defusedxml Stars](https://img.shields.io/github/stars/tiran/defusedxml?style=flat-square&logo=github&label=defusedxml)](https://github.com/tiran/defusedxml)
[![PyPI Downloads](https://img.shields.io/pypi/dm/defusedxml?style=flat-square&logo=pypi&label=defusedxml%2Fmonth&color=blue)](https://pypistats.org/packages/defusedxml)

I created and maintain **defusedxml**, which provides drop-in replacements for
Python's XML parsers that defend against entity-expansion ("billion laughs"),
external-entity (XXE), and DTD-retrieval attacks. For roughly a decade I also
maintained CPython's `ssl` and `hashlib` modules — moving hostname verification
onto OpenSSL's native checks, bringing up TLS 1.3 support, making `SSLContext`
secure by default, and porting both modules through successive OpenSSL API
transitions. I implemented the `usedforsecurity` mechanism and a C-based HMAC so
Python behaves correctly under FIPS-mode OpenSSL, contributed fixes upstream to
**[OpenSSL](https://github.com/openssl/openssl)** itself, and wrote the FIPS-mode
algorithm restrictions in
**[pyca/cryptography](https://github.com/pyca/cryptography)**. My CPython
`--with-ssl-default-suites=openssl` build option
is what lets Fedora/RHEL's system-wide crypto-policies apply to Python's `ssl`
connections.

---

### 🎩 Identity Management — FreeIPA, Custodia & python-ldap

[![FreeIPA Stars](https://img.shields.io/github/stars/freeipa/freeipa?style=flat-square&logo=github&label=FreeIPA)](https://github.com/freeipa/freeipa)
[![Custodia Stars](https://img.shields.io/github/stars/latchset/custodia?style=flat-square&logo=github&label=Custodia)](https://github.com/latchset/custodia)
[![python-ldap Stars](https://img.shields.io/github/stars/python-ldap/python-ldap?style=flat-square&logo=github&label=python-ldap)](https://github.com/python-ldap/python-ldap)

Much of my earlier work at Red Hat was across the identity-management stack.
**FreeIPA** (shipped as Red Hat Identity Management, RHEL IdM) is an open-source
identity-management system, largely written in Python, that integrates an LDAP
directory (389 Directory Server), Kerberos (MIT krb5), a certificate authority
(Dogtag PKI), and DNS into a single managed security domain. In FreeIPA I designed
and implemented four features — Member Manager, Hidden Replicas, LDAPI Autobind,
and Subordinate IDs (the last relevant to Podman and rootless containers) — each
with a published design document on
[freeipa.readthedocs.io](https://freeipa.readthedocs.io). I co-maintained
**[Custodia](https://github.com/latchset/custodia)**, a secrets-management service
for cloud applications, together with its founder Simo Sorce. I also contributed to
**python-ldap** as an upstream collaborator, including its modernization to the
stable `abi3` ABI and a number of memory-leak and security fixes.

---

## 🎤 Speaking

I've spoken at Python and open-source conferences for well over a decade, including
PyCon US, EuroPython, PyCon DE, PyCon UK, and DevConf (Czechia and India). Topics have
ranged from TLS/PKI and Python's `ssl` module to security engineering, WebAssembly,
and open-source AI. Keynotes include:

- **DevConf.IN 2018** (Bengaluru, India) — "Everyday Security Issues and How to
  Avoid Them," the keynote at the first-ever DevConf India.
- **[PyCon DE 2022](https://2022.pycon.de/blog/keynote-3-christian-heimes/)**
  (Berlin) — "Python 3.11 in the Web Browser – A Journey," on CPython's
  WebAssembly port.

Slides for many of my talks are on [SpeakerDeck](https://speakerdeck.com/tiran).

---

## 🐘 Zope & Plone

[**Zope**](https://www.zope.dev/) is one of the original Python web application
servers (with its own object database, the ZODB), and [**Plone**](https://plone.org/)
is the content management system built on top of it — for years one of the most
widely deployed Python web platforms.

From **2003 to 2007** I was a core developer of both and an elected board member of
the **Plone Foundation**. I was the primary maintainer of **Products.Archetypes**
(the schema-based content-type framework) and **Products.ATContentTypes** (Plone's
default content types built on it).

---

## 🕰️ Earlier Career

Before CPython and Red Hat, roughly in order:

- **1997–1999** — Built and ran a Linux server and Internet router for my school
  under the German [*Schulen ans Netz*](https://de.wikipedia.org/wiki/Schulen_ans_Netz)
  ("Schools on the Net") initiative to bring schools online.
- **2000–2005** — Administered a student dormitory network: qmail mail server,
  Courier IMAP, and network security.
- **2008–2013** — **semantics GmbH**: Python developer on **Visual Library**, a
  digitization and digital-library platform for libraries, archives, and museums
  (stack: Python, CherryPy, Firebird, lxml; METS/MODS metadata; SAN storage over a
  Fibre Channel fabric).
- **2014–2015** — **About You / Project Collins** (Otto Group): backend / Shop API
  developer on the e-commerce platform (Python, Elasticsearch, Redis).
