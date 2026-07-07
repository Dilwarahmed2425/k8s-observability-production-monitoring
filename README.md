# Production Monitoring & Incident Management Platform

## 🚀 Project Overview
Implemented an end-to-end cloud-native monitoring and observability solution on Amazon EKS using Prometheus and Grafana. Configured active alert rules to identify microservice downtime and practiced real-time incident resolution.

## 🛠️ Technologies Used
* **Orchestration:** Kubernetes (AWS EKS), Kubectl
* **Observability:** Prometheus, Grafana, Alertmanager
* **Package Management:** Helm
* **Scripting & OS:** Bash, Linux

## 📉 Incident Lifecycle Simulated
1. **The Alert Configured:** Created a custom `PrometheusRule` (`PodFrequentlyCrashing`) tracking rapid container restarts.
2. **The Incident:** Patched a live application deployment with a faulty configuration, forcing a `CrashLoopBackOff` state.
3. **The Detection:** Monitored the alert state shifting from `Normal` ➡️ `Pending` ➡️ `Firing` in Grafana.
4. **The Mitigation:** Investigated state logs via `kubectl describe` and rolled back the problematic deployment patch to restore normal operations.
