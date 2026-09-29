# Awesome-Cloud-Resource-Optimization

## Top Cloud Resource Optimization Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Kubernetes Rightsizing, Spot Orchestration, Bin Packing & FinOps Automation*  

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Resource Optimization**. These tools help platform teams, FinOps practitioners, and DevOps engineers reduce cloud waste by rightsizing workloads, optimizing node provisioning, automating spot instance usage, and consolidating underutilized infrastructure.



**Examples** include Cast AI, Spot by NetApp, Zesty, Densify, PerfectScale, ProsperOps, Turbonomic, StormForge, Granulate, and CloudBolt (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom optimization logic, and transparent cost data — ideal for teams that need full control over their optimization pipeline without revenue-share fees or vendor lock-in.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Cast AI](https://cast.ai/)**

  All-in-one Kubernetes automation, optimization, security, and cost management platform. Abstracts provider-specific complexity across AWS, GCP, Azure, OCI, and on-premises (Cast AI Anywhere). Features real-time cost monitoring at cluster/namespace/workload levels, automatic optimization via autoscaling, Spot instance automation, bin packing, and **workload autoscaling** to right-size containers based on actual usage . Karpenter Enterprise suite adds commitments support, continuous rebalancing, and Container Live Migration to move workloads without restarts .



- **[StormForge](https://www.stormforge.io/)**

  ML-powered Kubernetes resource optimization. Deployed on EKS Auto Mode, achieving **65% reduction in cluster upgrade time, 25% reduction in pod count, and 30-40% infrastructure cost reduction** . Uses an agent to collect workload metrics, applies ML for rightsizing recommendations, and integrates with Karpenter, HPA, VPA, and GitOps workflows.



- **[PerfectScale](https://www.perfectscale.io/)**

  Automated Kubernetes optimization with **intent-aware rightsizing**. Incorporates traffic patterns and workload criticality into every recommendation. Features **Optimization Policies** (MaxSavings, Balanced, ExtraHeadroom, MaxHeadroom) that can be set at cluster or workload level to balance cost savings against resilience for mission-critical services .



- **[Spot by NetApp](https://spot.io/products/ocean/)**

  Serverless container infrastructure platform. Automates cluster scaling, bin-packing, and spot instance management to reduce Kubernetes compute costs by 60-90% while maintaining reliability.



- **[Zesty](https://zesty.co/)**

  Automated cloud cost optimization platform. Dynamically adjusts committed use discounts and reserved instances based on real-time workload demand.



- **[Densify](https://www.densify.com/)**

  Cloud resource optimization using machine learning for rightsizing and workload placement across Kubernetes and virtualized environments.



- **[ProsperOps](https://www.prosperops.com/)**

  Automated commitment management platform. Optimizes Reserved Instances and Savings Plans to reduce cloud costs without manual intervention.



- **[Turbonomic](https://www.ibm.com/products/turbonomic)**

  Application resource management platform (IBM). Assures performance while optimizing cost across cloud, on-premises, and hybrid environments.



- **[Granulate](https://granulate.io/)**

  Autonomous workload optimization platform (acquired by Intel). Reduces CPU utilization and latency without code changes.



- **[CloudBolt](https://www.cloudbolt.io/)**

  Cloud management platform with cost optimization, automation, and governance capabilities. Provides visibility and control across multi-cloud environments.



## Open-Source GitHub Projects



### Kubernetes Rightsizing & Optimization



- **[Kube Resource Suggest (KRS)](https://github.com/joe-l-mathew/kube-resource-suggest)**

  **Suggestion-first, GitOps-safe** Kubernetes resource optimizer. Never modifies workloads directly — produces `ResourceSuggestion` objects for review. Uses **hybrid Prometheus + Kubelet methodology** for accuracy. Zero developer config: install once cluster-wide, every developer gets recommendations. No dependencies required (self-reliant) .



- **[CruiseKube](https://github.com/truefoundry/CruiseKube)**

  Kubernetes-native **closed-loop control system** that autonomously right-sizes CPU and memory at **runtime and admission time**. Observes real workload behavior and incrementally converges resource requests toward optimal values. Eliminates persistent over-provisioning while preserving reliability .



- **[k8s-rightsizer](https://github.com/mcpunzo/k8s-rightsizer)**

  Production-grade rightsizing controller with **automatic rollback safety**. If a pod fails to start (OOMKilled, CrashLoopBackOff, Unschedulable), it immediately restores the previous stable configuration. **Real-world results**: 36% and 23% cost reduction on production EKS clusters with zero downtime .



- **[KubeSurvival](https://github.com/aporia-ai/kubesurvival)**

  Reduces Kubernetes costs by finding the cheapest machine types that can run your workloads. Analyzes resource requirements and recommends optimal instance types .



- **[SleepCycles](https://github.com/rekuberate-io/sleepcycles)**

  **Define sleep and wake-up cycles** for Kubernetes resources (Deployments, StatefulSets, CronJobs, HPAs). Schedule resource-hungry workloads during off-hours to depressurize clusters, decrease costs, reduce power consumption, and lower carbon footprint .



- **[Cloud-Native K8s Optimizer](https://github.com/Sudharsanselvaraj/Cloud-Native-K8s-Cluster-Resource-Analysis-and-Optimization-Engine)**

  Cloud-native optimization engine that analyzes workload utilization, detects overprovisioned deployments, and generates CPU/memory recommendations. Features configurable safety buffers, overprovision ratio detection, max reduction caps, and Prometheus metrics .



### FinOps Platforms & Cost Management



- **[OptScale (Hystax)](https://github.com/hystax/optscale)**

  **Most comprehensive open-source FinOps platform** (2,190 stars). Supports AWS, Azure, GCP, Alibaba Cloud, and Kubernetes. Includes **cost analytics, anomaly detection, rightsizing recommendations, budget management**, and **MLOps cost optimization** for AI workloads. Thoughtworks Radar recommends it as a "platform capability investment" with broader non-Kubernetes FinOps coverage than OpenCost .



- **[OpenCost](https://github.com/opencost/opencost)**

  CNCF Incubating open-source cost monitoring for Kubernetes and cloud spend. Real-time cost allocation by cluster, node, namespace, controller, service, or pod. Multi-cloud support, GPU costs, carbon costs, and MCP server for AI agents. Apache-2.0 .



- **[CostScope](https://github.com/costscope/costscope)**

  Open FinOps and Governance platform for **AI/LLM and GPU workloads**. **FOCUS 1.2 compatible**. Converts AWS CUR, Azure, and GCP billing into normalized FinOps schema. Features GPU & Energy Metrics (Kepler integration), AI/LLM governance, Prometheus/OpenTelemetry observability, and SBOM/signatures for integrity .



- **[ecos](https://github.com/ecos-labs/ecos)**

  Open-source FinOps data stack that transforms AWS CUR into clean, enriched, high-performance datasets. **40+ pre-built dbt models** for cost analysis and optimization. Modular and extensible, runs in your infrastructure. Includes MCP server for AI-powered cost insights .



- **[Koku](https://github.com/project-koku/koku)**

  Open-source solution for cost management of cloud and hybrid cloud environments. Provides cost visibility and reporting across providers .



- **[Fadvisor (FinOps Advisor)](https://github.com/gocrane/fadvisor)**

  Collection of exporters that collect cloud resource pricing and billing data. Provides cost allocation insight for containers and Kubernetes resources .



- **[Komiser](https://github.com/tailwarden/komiser)**

  Open-source cloud resource manager that scans cloud accounts, builds full inventory, and surfaces misconfigurations, underutilized infrastructure, and hidden cost drivers. Supports AWS, Azure, GCP, DigitalOcean, Civo, and more .



- **[Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian)**

  CNCF Incubating project using YAML-based DSL to create and enforce cloud governance rules. Can schedule cloud "off hours" for resources to reduce waste .



- **[Steampipe](https://github.com/turbot/steampipe)**

  Query live cloud APIs using SQL without ETL pipelines. 150+ plugins covering AWS, Azure, GCP, and Kubernetes. Surface idle resources, underutilized instances, and spend patterns .



- **[Multi-Cloud FinOps](https://github.com/priyaranjan-sahu/multi-cloud-finops)**

  Multi-cloud cost optimization and anomaly detection (FOCUS 1.0) for AWS, GCP, and Azure. Features spend aggregation, forecasting, rightsizing, Prometheus/Grafana monitoring, and KEDA autoscaling .



- **[Terracost](https://github.com/cycloidio/terracost)**

  Cloud cost estimation for Terraform in your CLI. Shift FinOps left by estimating costs before deployment .



### Additional Strong Open-Source Options



- **Kubernetes Rightsizing**: **KRS** (suggestion-first, GitOps-safe) , **CruiseKube** (closed-loop runtime) , **k8s-rightsizer** (auto-rollback safety) , **KubeSurvival** (cheapest instance types) .

- **Scheduling & Waste Reduction**: **SleepCycles** (off-hours scheduling) .

- **FinOps Platforms**: **OptScale** (comprehensive, MLOps) , **CostScope** (AI/GPU focus, FOCUS 1.2) , **ecos** (dbt models) , **Koku** (multi-cloud) .

- **Cloud Governance**: **Cloud Custodian** (YAML DSL) , **Komiser** (resource inventory) , **Steampipe** (SQL queries) .



**Frameworks for building custom systems**: Combine **OptScale** for comprehensive multi-cloud FinOps with anomaly detection, **OpenCost** for Kubernetes cost allocation, **KRS** or **CruiseKube** for safe workload rightsizing, and **CostScope** for AI/GPU cost governance. Add **SleepCycles** for off-hours scheduling, **Prometheus + Grafana** for observability, and **PostgreSQL** for persistence.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Cloud resource optimization tools require accurate cloud billing API integration; on-demand list pricing may misrepresent actual invoices without reconciliation.

- **Open-source reality**: The open-source ecosystem is **mature and production-ready** for Kubernetes rightsizing (**KRS**, **CruiseKube**, **k8s-rightsizer**) and FinOps platforms (**OptScale**, **OpenCost**, **CostScope**) . However, comprehensive optimization requires **infrastructure ownership** (Prometheus, Grafana, PostgreSQL, potentially ClickHouse) and **engineering time** for operations — the software is free, but the operational cost is real . For teams without dedicated FinOps engineering, commercial platforms like Cast AI and StormForge offer faster time-to-value with autonomous optimization .
