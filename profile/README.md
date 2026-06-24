

<p align="center">
  <img width="2120" height="742" alt="banner" src="https://github.com/user-attachments/assets/d59deda5-18a6-45cd-b6e7-9b193acfee52" alt="Kernel Guard — Runtime Protection. Verifiable Security." width="100%">
</p>

# Kernel Guard

**Kernel Guard builds open-source security tooling for Linux, eBPF, runtime enforcement, and compatibility evidence.**

We work on systems where security decisions must be validated against real execution environments, not assumed from static claims. Our projects focus on kernel-level protection, eBPF artifact validation, runtime security, CI/CD security gates, and infrastructure evidence that engineers can inspect, reproduce, and automate.

---

## What we build

Kernel Guard focuses on practical security infrastructure for Linux and cloud-native environments:

- **eBPF compatibility evidence** for compiled BPF artifacts
- **Kernel-level runtime enforcement** for Linux workloads
- **CI/CD security gates** backed by reproducible validation
- **Policy-driven prevention and audit workflows**
- **Kubernetes-oriented security deployment**
- **Forensic-grade runtime telemetry and reports**

The goal is simple:

> Make security behavior testable, enforceable, and explainable across real kernels, workloads, and deployment environments.

---

## Featured projects

### [`bpfcompat`](https://github.com/Kernel-Guard/bpfcompat)

`bpfcompat` is an open-source compatibility validator for compiled eBPF artifacts.

It answers a practical question:

> Will this `.bpf.o` load and attach on the kernels we care about?

Instead of relying only on assumptions from CO-RE, BTF, or kernel version numbers, `bpfcompat` validates artifacts against real kernel profiles and produces structured compatibility evidence for local testing or CI gates.

**Use cases**

- Validate eBPF artifacts before release
- Detect load/attach regressions across kernel versions
- Test compatibility against enterprise and cloud kernels
- Produce JSON/Markdown evidence for CI workflows
- Investigate verifier, BTF, map, program, and attach-type failures

**Links**

- Repository: https://github.com/Kernel-Guard/bpfcompat
- Demo: https://bpfcompat.kernelguard.net
- Website: https://www.kernelguard.net/projects/bpfcompat/

---

### [`Aegis-BPF`](https://github.com/Kernel-Guard/Aegis-BPF)

`Aegis-BPF` is an eBPF-based runtime security engine for Linux workloads.

It focuses on enforcement-first runtime protection using BPF LSM hooks, policy-driven blocking, structured audit events, cgroup-scoped controls, and Kubernetes deployment support.

**Core areas**

- Kernel-level file and network enforcement
- BPF LSM based prevention
- Cgroup-scoped policy controls
- Audit-only fallback when enforcement hooks are unavailable
- Prometheus metrics and structured logging
- Signed policy bundles and integrity verification
- Kubernetes deployment through Helm/DaemonSet workflows

**Links**

- Repository: https://github.com/Kernel-Guard/Aegis-BPF

---

## Engineering principles

Kernel Guard projects are designed around a few operating principles:

| Principle | Meaning |
|---|---|
| **Evidence over assumptions** | Security claims should be backed by reproducible validation. |
| **Runtime truth** | Kernel behavior must be tested where it actually executes. |
| **Clear failure modes** | Failures should explain what broke, where, and why. |
| **Secure-by-default design** | Safety, isolation, and auditability should be part of the architecture. |
| **Operational simplicity** | Tools should integrate cleanly into developer and platform workflows. |
| **Open technical review** | Security infrastructure benefits from public inspection and reproducible results. |

---

## Where Kernel Guard fits

Modern Linux and cloud-native security depends on details that are easy to miss:

- kernel versions and vendor backports
- BTF availability and CO-RE relocation behavior
- verifier constraints
- program and attach-type support
- container and OverlayFS behavior
- cgroup identity
- CI runner capabilities
- runtime policy enforcement posture

Kernel Guard builds tooling for that boundary: the point where security engineering meets real kernel behavior.

---

## For contributors and reviewers

We are especially interested in feedback from:

- Linux kernel engineers
- eBPF developers
- runtime security engineers
- cloud-native security teams
- observability and platform engineers
- CI/CD and infrastructure maintainers

Useful contributions include:

- kernel compatibility profiles
- eBPF test artifacts
- runtime security rule examples
- documentation improvements
- CI integration examples
- bug reports with reproducible evidence
- design review for enforcement and trust models

---

## Project status

Kernel Guard is an early-stage open-source security organization.

The current focus is building technically credible, reproducible, and reviewable systems before expanding the surface area. Projects may evolve quickly, and production use should follow each repository’s individual status, documentation, and security notes.

---

## Links

- Website: https://kernelguard.net
- bpfcompat demo: https://bpfcompat.kernelguard.net
- GitHub: https://github.com/Kernel-Guard
- LinkedIn: https://www.linkedin.com/company/kernel-guard/
- Contact: contact@kernelguard.net

---

## Security

If you believe you have found a security issue in a Kernel Guard project, please avoid public disclosure until the issue can be reviewed.

Use the security policy of the relevant repository when available, or contact the maintainers directly.

---

<p align="center">
  <sub>Runtime protection. Verifiable security.</sub>
</p>
