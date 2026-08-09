# Awesome-Secrets-Scanning

# Top Secrets Scanning Tools Ecosystem

**Curated List of SaaS/Commercial Products & Open-Source GitHub Projects**  
*Focused on Detecting Hardcoded Secrets, API Keys, Credentials & Sensitive Data in Code, Git History & CI/CD*  
**Last updated: August 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Secrets Scanning**. These tools scan source code, git history, containers, and other artifacts to find accidentally committed credentials (API keys, tokens, passwords, certificates) so teams can rotate them and prevent leaks.

**Examples** include GitGuardian, TruffleHog, GitHub Secret Scanning, GitLab Secret Detection, SpectralOps, Cycode, Checkmarx Secrets, SentinelOne PingSafe, Gitleaks, and Apiiro (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosted or CLI-based secret detection — ideal for teams that want fast pre-commit/CI scanning, full control, and no per-seat licensing for basic detection.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[GitGuardian](https://www.gitguardian.com/)**  
  Leading secrets detection and remediation platform that monitors public and private repositories, provides real-time alerts, validity checks, and incident workflows for leaked credentials.

- **[GitHub Secret Scanning](https://docs.github.com/en/code-security/secret-scanning)**  
  Native GitHub capability (with push protection) that detects known secret patterns and partners with providers for validity checks and automatic revocation where supported.

- **[GitLab Secret Detection](https://docs.gitlab.com/ee/user/application_security/secret_detection/)**  
  Built-in GitLab security feature that scans repositories and pipelines for secrets as part of the DevSecOps workflow.

- **[SpectralOps](https://spectralops.io/)** (Check Point), **[Cycode](https://cycode.com/)**, **[Checkmarx Secrets](https://checkmarx.com/)**, **[SentinelOne PingSafe](https://www.sentinelone.com/)**, **[Apiiro](https://apiiro.com/)**  
  Commercial application security and code-risk platforms that include secrets detection alongside broader ASPM, SCA, or supply-chain capabilities.

- **[TruffleHog Enterprise](https://trufflesecurity.com/)** & **[Gitleaks commercial offerings](https://gitleaks.io/)**  
  Enterprise/commercial versions of the leading open-source scanners that add centralized management, support, and additional features.

## Open-Source GitHub Projects

- **[TruffleHog](https://github.com/trufflesecurity/trufflehog)**  
  Powerful open-source secrets scanner with 800+ detectors and live credential verification (checks whether a found key is still valid via provider APIs). Scans git history, filesystems, S3, Docker, Slack, and more. AGPL-3.0.

- **[Gitleaks](https://github.com/gitleaks/gitleaks)**  
  Fast, lightweight, MIT-licensed secret scanner focused on git repositories, files, and pre-commit hooks. Excellent CLI speed, high rule coverage, and easy CI/CD integration. One of the most widely adopted open-source tools.

- **[detect-secrets](https://github.com/Yelp/detect-secrets)**  
  Yelp’s open-source secret detection tool with baseline support, useful for existing codebases that already contain known secrets and for gradual remediation.

- **[ggshield](https://github.com/GitGuardian/ggshield)**  
  Open-source CLI from GitGuardian (MIT) that brings local and CI scanning capabilities; can work standalone or with the GitGuardian platform.

- **[Trivy (secrets module)](https://github.com/aquasecurity/trivy)**  
  Comprehensive open-source security scanner that includes secret detection alongside vulnerability, misconfiguration, and SBOM scanning for containers, filesystems, and git repos.

- **[git-secrets](https://github.com/awslabs/git-secrets)**  
  AWS Labs tool that prevents committing secrets by installing git hooks and scanning for patterns (especially AWS credentials).

- **[Nosey Parker](https://github.com/praetorian-inc/noseyparker)** & other specialized scanners  
  Additional open-source engines focused on high-performance or multi-source secret hunting across code and artifacts.

- **[Combined / wrapper tools](https://github.com/)**  
  Community projects that orchestrate TruffleHog + Gitleaks (or similar) for broader coverage and classification in a single pipeline.

### Additional Strong Open-Source Options

- Pre-commit framework hooks that run Gitleaks, detect-secrets, or similar on every commit.
- Custom regex + entropy scanners tailored to internal secret formats.
- Integration of secret scanning into broader SAST/SCA pipelines (Semgrep, Checkov, etc.).
- Many organization-specific detectors and allow-list management tools released as open source.

**Frameworks for building custom systems**: Use **Gitleaks** as a fast pre-commit and PR gate. Run **TruffleHog** (with verification) in CI or periodic full-history scans for higher confidence. Add **detect-secrets** baselines for legacy repositories. Layer platform-native scanning (GitHub/GitLab) for continuous coverage, and centralize findings in your existing security tooling or issue tracker.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS/commercial or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Secret scanning reduces risk but is not perfect — false positives and false negatives both occur. Always combine automated detection with developer education, short-lived credentials, secret managers, and least-privilege practices. Open-source tools give excellent detection capabilities but leave remediation workflows, alerting, and ownership tracking to your team.
- Never commit real secrets “for testing”; use placeholders and proper secret management from the start.

---

**Made for AppSec engineers, DevOps teams, and developers who want to keep secrets out of code.**  
Let's make credential leaks rarer and detection more open.
