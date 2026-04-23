<div align="center">

# 🛡️ DevSecOps Roadmap — Do Zero ao Profissional
### Guia completo, gratuito e em português para integrar segurança ao ciclo de desenvolvimento

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/viniciusldiniz/DevSecOps-Roadmap?style=social)](https://github.com/viniciusldiniz/DevSecOps-Roadmap)

> **"Segurança não é uma fase — é parte de cada linha de código."**
> Este repositório reúne trilhas, ferramentas, cursos gratuitos e projetos práticos para quem quer integrar segurança ao pipeline de DevOps.

[📚 Trilha de Estudos](#-trilha-de-estudos) • [🎓 Cursos Gratuitos](#-cursos-gratuitos) • [🛠️ Ferramentas](#️-ferramentas-essenciais) • [📜 Certificações](#-certificações) • [🤝 Contribuir](#-como-contribuir)

</div>

---

## 📋 Índice

- [O que é DevSecOps?](#-o-que-é-devsecops)
- [Por que DevSecOps?](#-por-que-devsecops)
- [Trilha de Estudos](#-trilha-de-estudos)
  - [Nível 1 — Fundamentos de Segurança](#nível-1--fundamentos-de-segurança)
  - [Nível 2 — Segurança no Pipeline](#nível-2--segurança-no-pipeline)
  - [Nível 3 — Segurança Avançada](#nível-3--segurança-avançada)
- [Cursos Gratuitos](#-cursos-gratuitos)
- [Ferramentas Essenciais](#️-ferramentas-essenciais)
- [Certificações Recomendadas](#-certificações)
- [Projetos para o Portfólio](#-projetos-para-o-portfólio)
- [Comunidades](#-comunidades)
- [Como Contribuir](#-como-contribuir)

---

## 🤔 O que é DevSecOps?

DevSecOps é a evolução natural do DevOps — integra **Segurança (Sec)** desde o início do ciclo de desenvolvimento, ao invés de tratá-la como uma fase final.

```
Dev → Sec → Ops → (integrados desde o primeiro commit)

Desenvolvimento → [SAST] → Build → [SCA] → Deploy → [DAST] → Monitoramento
       |_______________________Security Pipeline_________________________|
```

**Pilares do DevSecOps:**
- 🔍 **Shift Left** — segurança aplicada desde o início do desenvolvimento
- 🤖 **Automação** — testes de segurança integrados ao pipeline CI/CD
- 📦 **Supply Chain Security** — verificação de dependências e imagens
- 🔐 **Secrets Management** — gerenciamento seguro de credenciais
- 📊 **Monitoramento Contínuo** — detecção de ameaças em produção
- 🏗️ **Infrastructure Security** — infraestrutura segura como código

---

## 💡 Por que DevSecOps?

| Métrica | Segurança Tradicional | DevSecOps |
|---|---|---|
| Quando detecta vulnerabilidades | No final (produção) | No início (desenvolvimento) |
| Custo de correção | Alto (100x mais caro) | Baixo |
| Velocidade de entrega | Lenta (bloqueios de segurança) | Rápida (automatizada) |
| Responsabilidade | Só do time de segurança | De todos os times |
| Frequência de auditorias | Eventual | Contínua |

📈 **Mercado:** Profissionais de DevSecOps são dos mais valorizados da TI, com alta demanda e ainda baixíssima oferta no Brasil.

---

## 📚 Trilha de Estudos

### Nível 1 — Fundamentos de Segurança

> ⏱️ Tempo estimado: 2 a 3 meses

#### 🔐 Conceitos Essenciais de Segurança
- [ ] CIA Triad: Confidencialidade, Integridade e Disponibilidade
- [ ] Autenticação vs Autorização
- [ ] Princípio do menor privilégio
- [ ] Criptografia básica: simétrica, assimétrica, hashing
- [ ] Principais tipos de ataque: SQLi, XSS, CSRF, IDOR
- [ ] OWASP Top 10 — as 10 vulnerabilidades mais críticas

**Recursos:**
- 📖 [OWASP Top 10 (gratuito)](https://owasp.org/www-project-top-ten/)
- 📖 [CS50 Cybersecurity - Harvard (gratuito)](https://cs50.harvard.edu/cybersecurity/)
- 🎥 [Segurança da Informação - Canal do YouTube Lobo](https://www.youtube.com/@gabriellobopt)

---

#### 🐧 Linux e Segurança de Sistemas
- [ ] Gerenciamento de usuários e permissões
- [ ] Firewall com `iptables` e `ufw`
- [ ] Análise de logs do sistema (`/var/log/`)
- [ ] SSH hardening e chaves públicas/privadas
- [ ] Crontabs e processos suspeitos
- [ ] Auditoria com `auditd`

**Recursos:**
- 📖 [Linux Journey (gratuito)](https://linuxjourney.com/)
- 🎥 [Hardening Linux - LINUXtips](https://www.youtube.com/c/linuxtips)

---

#### 🌐 Redes e Segurança de Rede
- [ ] TCP/IP, DNS, HTTP/HTTPS — como funcionam e onde falham
- [ ] Ataques de rede: Man-in-the-Middle, DDoS, DNS Poisoning
- [ ] SSL/TLS — como funciona o handshake
- [ ] VPNs e Zero Trust Network
- [ ] Análise de tráfego com Wireshark
- [ ] Port scanning com Nmap

**Recursos:**
- 📖 [Networking Basics - Cisco (gratuito)](https://www.netacad.com/courses/networking/networking-basics)
- 🎥 [Hacking Ético - Desec Security (PT-BR)](https://www.youtube.com/@DesecSecurity)

---

#### 🔧 Git e Segurança no Versionamento
- [ ] Boas práticas para não commitar segredos
- [ ] `.gitignore` e arquivos sensíveis
- [ ] Assinatura de commits com GPG
- [ ] Branch protection rules
- [ ] Auditoria de histórico do repositório
- [ ] Ferramentas: `git-secrets`, `truffleHog`, `gitleaks`

**Recursos:**
- 📖 [GitHub Security Docs (gratuito)](https://docs.github.com/pt/code-security)

---

### Nível 2 — Segurança no Pipeline

> ⏱️ Tempo estimado: 3 a 4 meses

#### 🔍 SAST — Análise Estática de Código
- [ ] O que é SAST e quando usar
- [ ] **Semgrep** — análise de código multi-linguagem
- [ ] **Bandit** — análise de segurança para Python
- [ ] **SonarQube** — qualidade e segurança de código
- [ ] Integrando SAST no GitHub Actions
- [ ] Interpretando e priorizando vulnerabilidades

**Recursos:**
- 📖 [Semgrep Docs (gratuito)](https://semgrep.dev/docs/)
- 📖 [SonarQube Community (gratuito)](https://www.sonarqube.org/downloads/)
- 🎥 [SAST com GitHub Actions - DevSecOps Studio](https://www.youtube.com/@DevSecOpsStudio)

---

#### 🐳 Segurança em Containers
- [ ] Vulnerabilidades comuns em imagens Docker
- [ ] **Trivy** — scanning de imagens e filesystems
- [ ] **Grype** — scanner de vulnerabilidades
- [ ] **Docker Bench Security** — hardening de Docker
- [ ] Imagens mínimas: Alpine, Distroless
- [ ] Usuário não-root em containers
- [ ] Assinatura de imagens com Cosign

**Recursos:**
- 📖 [Trivy Docs (gratuito)](https://aquasecurity.github.io/trivy/)
- 📖 [Docker Security Best Practices](https://docs.docker.com/develop/security-best-practices/)
- 🎥 [Container Security - TechWorld with Nana (inglês)](https://www.youtube.com/@TechWorldwithNana)

---

#### 🔑 Secrets Management
- [ ] Por que nunca colocar segredos no código
- [ ] **HashiCorp Vault** — gerenciamento centralizado de segredos
- [ ] GitHub Secrets e variáveis de ambiente seguras
- [ ] **AWS Secrets Manager** e **Parameter Store**
- [ ] Rotação automática de credenciais
- [ ] Detecção de segredos expostos: `gitleaks`, `truffleHog`

**Recursos:**
- 📖 [HashiCorp Vault Learn (gratuito)](https://developer.hashicorp.com/vault/tutorials)
- 📖 [Gitleaks GitHub](https://github.com/gitleaks/gitleaks)

---

#### ⚙️ Segurança no CI/CD
- [ ] Conceito de pipeline seguro
- [ ] Análise de dependências: **Dependabot**, **Snyk**, **OWASP Dependency-Check**
- [ ] Assinatura de artefatos (SLSA Framework)
- [ ] Permissões mínimas em workflows do GitHub Actions
- [ ] Supply Chain Attacks — como se proteger
- [ ] **SBOM** (Software Bill of Materials)

**Recursos:**
- 📖 [SLSA Framework (gratuito)](https://slsa.dev/)
- 📖 [Snyk Learn (gratuito)](https://learn.snyk.io/)
- 🎥 [DevSecOps Pipeline - Zero to Hero (inglês)](https://www.youtube.com/@DevSecOpsStudio)

---

#### 🌐 DAST — Análise Dinâmica
- [ ] O que é DAST e diferença do SAST
- [ ] **OWASP ZAP** — scanner de vulnerabilidades web
- [ ] **Nikto** — scanner de servidores web
- [ ] Testes de API com segurança
- [ ] Fuzzing básico
- [ ] Integrando DAST no pipeline

**Recursos:**
- 📖 [OWASP ZAP (gratuito)](https://www.zaproxy.org/)
- 🎮 [DVWA - Damn Vulnerable Web Application (laboratório)](https://github.com/digininja/DVWA)
- 🎮 [WebGoat - OWASP (laboratório)](https://github.com/WebGoat/WebGoat)

---

### Nível 3 — Segurança Avançada

> ⏱️ Tempo estimado: 4 a 6 meses

#### ☸️ Segurança em Kubernetes
- [ ] Arquitetura de segurança do K8s
- [ ] RBAC — Role-Based Access Control
- [ ] Network Policies — segmentação de rede
- [ ] **OPA/Gatekeeper** — políticas de segurança
- [ ] **Falco** — detecção de ameaças em runtime
- [ ] **Kube-bench** — CIS Benchmark para K8s
- [ ] Pod Security Standards
- [ ] Secrets encryption at rest

**Recursos:**
- 📖 [Kubernetes Security Docs (gratuito)](https://kubernetes.io/docs/concepts/security/)
- 📖 [Falco Docs (gratuito)](https://falco.org/docs/)
- 🎥 [K8s Security - LINUXtips (PT-BR)](https://www.youtube.com/c/linuxtips)

---

#### ☁️ Cloud Security
- [ ] **AWS Security Hub** e **GuardDuty**
- [ ] IAM — políticas de menor privilégio
- [ ] CloudTrail — auditoria de ações na cloud
- [ ] **CIS Benchmarks** para AWS/Azure/GCP
- [ ] **Prowler** — auditoria de segurança AWS
- [ ] **ScoutSuite** — auditoria multi-cloud
- [ ] Conformidade: SOC2, ISO 27001, LGPD

**Recursos:**
- 📖 [AWS Security Learning (gratuito)](https://aws.amazon.com/security/security-learning/)
- 📖 [Prowler GitHub (gratuito)](https://github.com/prowler-cloud/prowler)
- 📖 [CIS Benchmarks (gratuito)](https://www.cisecurity.org/cis-benchmarks)

---

#### 📊 Monitoramento e Resposta a Incidentes
- [ ] SIEM básico — coleta e correlação de eventos
- [ ] **ELK Stack** para análise de logs de segurança
- [ ] **Wazuh** — SIEM open source
- [ ] Detecção de anomalias em logs
- [ ] Playbooks de resposta a incidentes
- [ ] Threat Intelligence básico
- [ ] Forense digital introdutória

**Recursos:**
- 📖 [Wazuh Docs (gratuito)](https://documentation.wazuh.com/)
- 📖 [ELK Security (gratuito)](https://www.elastic.co/security)
- 🎥 [Blue Team Labs Online (laboratórios gratuitos)](https://blueteamlabs.online/)

---

#### 🔴 Red Team / Pentest Básico
- [ ] Metodologias: OWASP, PTES, OSSTMM
- [ ] **Kali Linux** — distribuição para pentest
- [ ] **Metasploit** — framework de exploração
- [ ] **Burp Suite** — interceptação de requisições web
- [ ] Reconhecimento passivo e ativo
- [ ] Relatório de vulnerabilidades

**Recursos:**
- 📖 [TryHackMe (gratuito parcialmente)](https://tryhackme.com/)
- 📖 [HackTheBox (gratuito parcialmente)](https://www.hackthebox.com/)
- 🎥 [Hacking do Zero - Mente Binária (PT-BR)](https://www.youtube.com/@MenteBinaria)

---

## 🎓 Cursos Gratuitos

| Plataforma | Curso | Nível | Idioma |
|---|---|---|---|
| [TryHackMe](https://tryhackme.com/) | SOC Level 1 / Pre-Security | Iniciante | 🇺🇸 |
| [HackTheBox Academy](https://academy.hackthebox.com/) | Bug Bounty Hunter | Iniciante | 🇺🇸 |
| [CS50 Harvard](https://cs50.harvard.edu/cybersecurity/) | Cybersecurity | Iniciante | 🇺🇸 |
| [OWASP](https://owasp.org/) | Top 10 / Guias | Todos | 🇧🇷/🇺🇸 |
| [Snyk Learn](https://learn.snyk.io/) | DevSecOps Prático | Intermediário | 🇺🇸 |
| [HashiCorp Learn](https://developer.hashicorp.com/vault) | Vault | Intermediário | 🇺🇸 |
| [Blue Team Labs](https://blueteamlabs.online/) | Defesa e Resposta | Todos | 🇺🇸 |
| [LetsDefend](https://letsdefend.io/) | Blue Team / SOC | Iniciante | 🇺🇸 |
| [Desec Security](https://www.youtube.com/@DesecSecurity) | Hacking Ético | Iniciante | 🇧🇷 |
| [Mente Binária](https://www.youtube.com/@MenteBinaria) | Pentest / RE | Intermediário | 🇧🇷 |

---

## 🛠️ Ferramentas Essenciais

```
🔍 SAST                    📦 SCA / SUPPLY CHAIN     🐳 CONTAINER SECURITY
├── Semgrep                ├── Snyk                  ├── Trivy
├── SonarQube              ├── Dependabot             ├── Grype
├── Bandit (Python)        ├── OWASP Dep-Check        ├── Docker Bench
└── Checkov (IaC)          └── Syft (SBOM)            └── Cosign

🌐 DAST                    🔑 SECRETS MGMT           ☸️ K8s SECURITY
├── OWASP ZAP              ├── HashiCorp Vault        ├── Falco
├── Nikto                  ├── Gitleaks               ├── Kube-bench
└── Nuclei                 └── TruffleHog             └── OPA/Gatekeeper

☁️ CLOUD SECURITY          📊 SIEM / MONITORAMENTO   🔴 PENTEST
├── Prowler (AWS)          ├── Wazuh                  ├── Kali Linux
├── ScoutSuite             ├── ELK Stack              ├── Metasploit
├── CloudSploit            └── Grafana + Loki         ├── Burp Suite
└── Steampipe                                         └── Nmap
```

---

## 📜 Certificações

> Certificações que realmente valem no mercado de DevSecOps!

### 🔐 Segurança
| Certificação | Nível | Custo | Validade |
|---|---|---|---|
| [CompTIA Security+](https://www.comptia.org/certifications/security) | Fundamental | ~$392 USD | 3 anos |
| [CEH - Certified Ethical Hacker](https://www.eccouncil.org/train-certify/certified-ethical-hacker-ceh/) | Intermediário | ~$950 USD | 3 anos |
| [OSCP - Offensive Security](https://www.offsec.com/courses/pen-200/) | Avançado | ~$1.499 USD | Vitalício |
| [eJPT - eLearnSecurity](https://ine.com/certifications/ejpt-certification) | Iniciante | ~$200 USD | Vitalício |

### ⚙️ DevSecOps / Cloud Security
| Certificação | Nível | Custo |
|---|---|---|
| [CKS - Certified K8s Security Specialist](https://training.linuxfoundation.org/certification/certified-kubernetes-security-specialist/) | Avançado | $395 USD |
| [AWS Security Specialty](https://aws.amazon.com/certification/certified-security-specialty/) | Avançado | $300 USD |
| [Certified DevSecOps Professional - CDP](https://www.practical-devsecops.com/certifications/practical-devsecops-professional/) | Intermediário | $400 USD |
| [GitHub Advanced Security](https://examregistration.github.com/) | Intermediário | $250 USD |

💡 **Dica:** Comece pela **eJPT** (mais acessível) ou **CompTIA Security+** antes de ir para as avançadas.

---

## 💰 Salários e Mercado

> Dados baseados em pesquisas salariais brasileiras (2024/2025)

| Cargo | Júnior | Pleno | Sênior |
|---|---|---|---|
| DevSecOps Engineer | R$ 6.000 - R$ 10.000 | R$ 12.000 - R$ 20.000 | R$ 22.000 - R$ 40.000+ |
| Security Engineer | R$ 7.000 - R$ 12.000 | R$ 14.000 - R$ 22.000 | R$ 25.000 - R$ 45.000+ |
| Pentester / Red Team | R$ 5.000 - R$ 9.000 | R$ 10.000 - R$ 18.000 | R$ 20.000 - R$ 35.000+ |
| AppSec Engineer | R$ 8.000 - R$ 14.000 | R$ 16.000 - R$ 25.000 | R$ 28.000 - R$ 50.000+ |

🌎 **Remoto Internacional:** Salários em USD podem variar de $4.000 a $15.000/mês para sênior.

---

## 💼 Projetos para o Portfólio

### 🟢 Iniciante
- [ ] **Pipeline com SAST** — GitHub Actions rodando Semgrep ou Bandit automaticamente
- [ ] **Scanner de vulnerabilidades em imagens** — Trivy integrado ao pipeline Docker
- [ ] **Detector de segredos expostos** — Gitleaks no pre-commit hook
- [ ] **Analisador de logs de segurança** — Script Python para detectar padrões suspeitos

### 🟡 Intermediário
- [ ] **Pipeline DevSecOps completo** — SAST + SCA + DAST + scanning de container em um único workflow
- [ ] **Vault + aplicação** — App consumindo segredos do HashiCorp Vault
- [ ] **Kubernetes hardening** — Cluster K8s com OPA, Falco e Network Policies configurados
- [ ] **SIEM simples** — ELK Stack + Wazuh monitorando uma aplicação real

### 🔴 Avançado
- [ ] **Threat Modeling** — Documentação completa de ameaças de uma aplicação real
- [ ] **Bug Bounty** — Participar de programas no HackerOne ou Bugcrowd
- [ ] **Red vs Blue** — Ambiente de laboratório com ataque e defesa automatizados
- [ ] **Compliance as Code** — Políticas de segurança implementadas com OPA/Gatekeeper

---

## 🗺️ Roadmap Visual

```
ANO 1
├── MÊS 1-2: Fundamentos (CIA, OWASP Top 10, Linux Security, Redes)
├── MÊS 3-4: Ferramentas básicas (SAST, Trivy, Gitleaks, Secrets)
├── MÊS 5-6: Pipeline seguro (GitHub Actions + SAST + SCA + DAST)
└── MÊS 7-12: Container + K8s Security + Cloud Security básica

ANO 2
├── MÊS 1-3: Kubernetes Security avançado (OPA, Falco, CKS)
├── MÊS 4-6: SIEM + Monitoramento + Resposta a Incidentes
├── MÊS 7-9: Certificações (eJPT / Security+ / CKS)
└── MÊS 10-12: Red Team / Pentest / Bug Bounty
```

---

## 📖 Livros Recomendados

| Livro | Autor | Link |
|---|---|---|
| The DevSecOps Playbook | Sean D. Mack | [Amazon](https://www.amazon.com.br/) |
| Hacking: The Art of Exploitation | Jon Erickson | [Amazon](https://www.amazon.com.br/) |
| The Web Application Hacker's Handbook | Stuttard & Pinto | [Amazon](https://www.amazon.com.br/) |
| Kubernetes Security and Observability | Brendan Creane | [Amazon](https://www.amazon.com.br/) |
| The Phoenix Project | Gene Kim et al. | [Amazon](https://www.amazon.com.br/) |

---

## 🤝 Comunidades

### 🇧🇷 Comunidades Brasileiras
- [Mente Binária - Discord](https://mentebinaria.com.br/)
- [Desec Security - Telegram](https://t.me/desec_security)
- [DevSecOps Brasil - LinkedIn](https://www.linkedin.com/groups/)
- [OWASP Brazil Chapter](https://owasp.org/www-chapter-brazil/)

### 🌍 Comunidades Internacionais
- [r/netsec - Reddit](https://www.reddit.com/r/netsec/)
- [OWASP Slack](https://owasp.slack.com/)
- [TryHackMe Discord](https://discord.com/invite/tryhackme)

### 🎙️ Podcasts
- [Segurança Legal (PT-BR)](https://www.segurancalegal.com/)
- [Darknet Diaries (inglês)](https://darknetdiaries.com/)
- [Risky Business (inglês)](https://risky.biz/)

---

## 📰 Fontes para se Manter Atualizado

- 📧 [tl;dr sec Newsletter](https://tldrsec.com/)
- 📰 [Krebs on Security](https://krebsonsecurity.com/)
- 📰 [The Hacker News](https://thehackernews.com/)
- 🐦 Twitter/X: `@SwiftOnSecurity` `@thegrugq` `@MalwareTechBlog`
- 📺 [John Hammond (YouTube)](https://www.youtube.com/@_JohnHammond)
- 📺 [IppSec (YouTube - HackTheBox walkthroughs)](https://www.youtube.com/@ippsec)

---

## 🗂️ Estrutura de Repositório Sugerida

```bash
meu-projeto-devsecops/
├── 📁 .github/
│   └── workflows/
│       ├── sast.yml           # Análise estática (Semgrep/Bandit)
│       ├── sca.yml            # Análise de dependências (Snyk)
│       ├── container-scan.yml # Scanning de imagem (Trivy)
│       └── dast.yml           # Análise dinâmica (OWASP ZAP)
├── 📁 docker/
│   ├── Dockerfile             # Imagem segura (non-root, minimal)
│   └── docker-compose.yml
├── 📁 terraform/
│   ├── main.tf
│   └── security.tf            # Políticas e grupos de segurança
├── 📁 kubernetes/
│   ├── deployment.yaml
│   ├── network-policy.yaml    # Segmentação de rede
│   └── rbac.yaml              # Controle de acesso
├── 📁 vault/
│   └── policies/              # Políticas do HashiCorp Vault
├── 📁 monitoring/
│   ├── falco-rules.yaml       # Detecção de ameaças runtime
│   └── wazuh-config.xml       # SIEM
├── 📁 scripts/
│   ├── audit.sh               # Script de auditoria
│   └── secrets-scan.sh        # Verificação de segredos
├── 📄 .pre-commit-config.yaml # Hooks de segurança
├── 📄 .gitignore
├── 📄 Makefile
└── 📄 README.md
```

---

## 🤝 Como Contribuir

Contribuições são muito bem-vindas! Este é um projeto da comunidade para a comunidade.

```bash
# 1. Fork o repositório
# 2. Crie sua branch
git checkout -b feature/novo-recurso

# 3. Faça suas mudanças e commit
git commit -m "feat: adiciona recurso X"

# 4. Push e Pull Request
git push origin feature/novo-recurso
```

**O que você pode contribuir:**
- 📚 Novos cursos gratuitos de segurança
- 🛠️ Ferramentas que você usa no dia a dia
- 💼 Projetos de portfólio
- 🐛 Correções de links quebrados
- 🌍 Recursos em português

---

## ⭐ Apoie o Projeto

Se este repositório te ajudou, deixa uma ⭐ — isso ajuda mais pessoas a encontrar o conteúdo!

---

## 📄 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

---

<div align="center">

**Feito com ❤️ para a comunidade DevSecOps brasileira**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/viniciuslessadiniz)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/viniciusldiniz)

*"A segurança não é um produto, é um processo."* 🛡️

</div>