<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=28&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=600&lines=Sadiqul+Islam;DevOps+%26+Cloud+Infrastructure+Engineer;Building+Reliable+Systems+at+Scale" alt="Typing SVG" />

<br/>

<p align="center">
  <a href="https://www.linkedin.com/in/sadiq-bup/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  &nbsp;
  <a href="https://github.com/Sadiq-code-nest" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-161B22?style=flat-square&logo=github&logoColor=white" alt="GitHub"/>
  </a>
  &nbsp;
  <a href="mailto:mdsadiq1221@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"/>
  </a>
</p>

</div>

---

## About

I design and operate cloud infrastructure that teams can trust — observable, automated, and built to recover gracefully. My work sits at the intersection of platform engineering, security, and delivery velocity: standing up Kubernetes clusters, wiring CI/CD pipelines, and ensuring production systems stay healthy through proper observability stacks.

Currently working under the **Cloudly DevOps Team** brand, delivering managed infrastructure and AIOps services for clients across AWS environments.

```
Focus areas  →  Container Orchestration · CI/CD Automation · Observability · Cloud Cost Optimization
Certifications →  AWS Solutions Architect (in progress)
Currently     →  100 Days of DevOps (Day 45+)  |  github.com/Sadiq-code-nest/100DaysofDevOps
```

---

## Infrastructure & Delivery Stack

#### Container & Orchestration

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)

#### CI/CD

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)

#### Infrastructure as Code

![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)

#### Cloud — AWS

![EC2](https://img.shields.io/badge/EC2-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![VPC](https://img.shields.io/badge/VPC-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![ALB](https://img.shields.io/badge/ALB-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![IAM](https://img.shields.io/badge/IAM-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![EKS](https://img.shields.io/badge/EKS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazon-s3&logoColor=white)

#### Observability

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F5A800?style=flat-square&logo=grafana&logoColor=white)
![Wazuh](https://img.shields.io/badge/Wazuh_SIEM-005571?style=flat-square&logo=elastic&logoColor=white)

#### Languages & Scripting

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

#### Version Control

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-161B22?style=flat-square&logo=github&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white)

---

## CI/CD Pipeline Architecture

A typical delivery pipeline I build and maintain:

```
  Developer Pushes Code
          │
          ▼
  ┌──────────────────┐
  │  GitHub / GitLab │  ← Webhook trigger
  └────────┬─────────┘
           │
           ▼
  ┌──────────────────────────────────────────────────┐
  │              CI Stage (GitHub Actions / Jenkins) │
  │                                                  │
  │  ① Lint & Static Analysis                        │
  │  ② Unit & Integration Tests                      │
  │  ③ Docker Build + Image Scan (Trivy)             │
  │  ④ Push to Container Registry                    │
  └────────────────────┬─────────────────────────────┘
                       │
                       ▼
  ┌──────────────────────────────────────────────────┐
  │              CD Stage (ArgoCD / GitOps)          │
  │                                                  │
  │  ⑤ Update Helm values / Kustomize manifests      │
  │  ⑥ ArgoCD detects Git diff → sync to cluster    │
  │  ⑦ Rolling deploy to Kubernetes                  │
  │  ⑧ Health checks & readiness probes              │
  └────────────────────┬─────────────────────────────┘
                       │
                       ▼
  ┌──────────────────────────────────────────────────┐
  │           Observability Layer                    │
  │                                                  │
  │  Prometheus → Grafana dashboards                 │
  │  Loki / Promtail → Centralized log aggregation   │
  │  Wazuh → Security event monitoring               │
  └──────────────────────────────────────────────────┘
```

---

## Featured Projects

| Project | Description | Stack |
|---|---|---|
| [100 Days of DevOps](https://github.com/Sadiq-code-nest/100DaysofDevOps) | Structured public learning log — Linux → Git → Docker → K8s → IaC | Markdown, Docker, Kubernetes |
| [DevOps Academy MERN](https://github.com/Sadiq-code-nest/devops-academy-MERN) | Full-stack course platform with JWT auth, role-based access, PM2 deployment | Node.js, React, MongoDB, Docker |
| CloudGuardian Stack *(private)* | Grafana + Prometheus + Loki + Wazuh observability stack on AWS EKS | Kubernetes, Helm, AWS |
| Cloudly Pipeline App *(private)* | Internal delivery pipeline management tool for client infrastructure workflows | Docker, MySQL, Node.js |

---

## GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Sadiq-code-nest&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true" alt="GitHub Stats" />
&nbsp;&nbsp;
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sadiq-code-nest&layout=compact&theme=github_dark&hide_border=true&langs_count=6" alt="Top Languages" />

<br/>

<img src="https://streak-stats.demolab.com?user=Sadiq-code-nest&theme=github-dark-blue&hide_border=true&date_format=j%20M%5B%20Y%5D" alt="GitHub Streak" />

</div>

---

## Working Principles

```yaml
infrastructure_as_code:   always  # No manual console changes in production
observability_first:      true    # If it's not measured, it's not managed
git_workflow:             trunk-based with short-lived feature branches
on_call_philosophy:       build systems that page less, not more
documentation:            treated as part of the deliverable, not an afterthought
```

---

## Connect

I'm open to discussing infrastructure architecture, production incidents worth learning from, or new engineering challenges.

- **LinkedIn** → [linkedin.com/in/sadiq-bup](https://www.linkedin.com/in/sadiq-bup/)
- **GitHub** → [github.com/Sadiq-code-nest](https://github.com/Sadiq-code-nest)
- **Email** → [mdsadiq1221@gmail.com](mailto:mdsadiq1221@gmail.com)

<div align="center">
<sub>Profile views: <img src="https://komarev.com/ghpvc/?username=Sadiq-code-nest&style=flat-square&color=58A6FF" alt="Profile views"/></sub>
</div>
