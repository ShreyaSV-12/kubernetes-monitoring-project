
# 🌐 Kubernetes Monitoring Project – Prometheus + Grafana

This project showcases real-time monitoring of a custom Kubernetes application using Prometheus and Grafana.
The app — Shreya-K8s-App — exposes metrics that are scraped by Prometheus and visualized in Grafana dashboards.


## 🎯 What I Implemented

✔ Deployed a Flask web application on Kubernetes

✔ Enabled monitoring through Prometheus annotations

✔ Configured Prometheus scrape jobs

✔ Integrated Grafana for dashboard visualization

✔ Created a custom dashboard displaying app status with my app label

✔ Successfully tracked uptime & active deployments



## 📌 Key Features

✔ Kubernetes deployment

✔ Monitoring annotations

✔ Auto-discovered app metrics

✔ Custom uptime graph

✔ Uses standard PromQL query

✔ Your name visible on dashboard (unique!)


## 🚀 Technologies Used

- Kubernetes – for container orchestration and managing application deployment

- Docker – to containerize the application

- Prometheus – for metrics scraping and monitoring the application performance

- Grafana – for visualizing real-time metrics with custom dashboards

- Node Exporter / Pod Annotations – to expose metrics from the Kubernetes app

- YAML (Kubernetes Manifests) – for deployments, services, configmaps

- Python / Flask App – simple web application running inside Kubernetes

- kubectl CLI – to interact with and manage Kubernetes clusters

- Git & GitHub – version control and project hosting

- VS Code – development and configuration editing
## 📌 Project Architecture

Kubernetes Cluster

└── Custom App (Python + Flask)

└── Exposes metrics on /metrics

└── Prometheus

└── Scrapes metrics from the App

└── Grafana

└── Visualizes Prometheus metrics via dashboards

<img width="1536" height="1024" alt="project structure" src="https://github.com/user-attachments/assets/8670036a-5e27-4fae-8ac3-8fc381c437e7" />




     
## ⚙️ How to Deploy (Steps)

* Build and push Docker Image
docker build -t shreyasv912/shreya-k8s-monitoring-app:v1 .
docker push shreyasv912/shreya-k8s-monitoring-app:v1

* Deploy App
kubectl apply -f kubernetes/

* Deploy Prometheus + Grafana
kubectl apply -f monitoring/

* Check running pods
kubectl get pods

* Access Grafana
http://localhost:30001

* Access App UI
http://localhost:30007



## 📸 Results & Dashboards
<img width="1920" height="1080" alt="kubernetes app output" src="https://github.com/user-attachments/assets/0bbbe51a-700a-4985-b746-46153cb9b5af" />

<img width="1920" height="1080" alt="k8s-prometheus pods running" src="https://github.com/user-attachments/assets/99a51a08-9b0b-48e3-b3c7-8864702ece01" />

<img width="1920" height="1080" alt="prometheus-overview-dashboard" src="https://github.com/user-attachments/assets/395fb7c5-c025-4a51-aa34-af91170cdc48" />

<img width="1920" height="1080" alt="grafana-custom-app-up-metrics" src="https://github.com/user-attachments/assets/d4785c6a-11c5-490a-99a6-ada85a8b17e3" />

🛡 Project Status

🚀 Monitoring is working successfully
📈 Metrics shown live in Grafana with app name: shreya-k8s-app



## 🛠 Why This Project is Used in Real-World

- Ensures high availability by continuously checking whether pods and services are running

- Helps detect failures early to prevent outages and downtime

- Tracks CPU, memory, and network usage to avoid performance bottlenecks

- Supports auto-scaling decisions based on real-time metrics (ex: scale up when traffic spikes)

- Improves application performance and user experience through continuous optimization

- Enables faster troubleshooting by providing detailed insights into cluster and app health

- Helps DevOps/SRE teams maintain SLAs like 99.99% uptime

- Provides custom business metrics (ex: success rates, orders per minute, active users)

- Acts as a core part of the DevOps observability stack

- Allows data-driven decision-making for infrastructure and capacity planning

- Enhances security monitoring by detecting unusual traffic or resource consumption

- Integrates seamlessly with Kubernetes ecosystem for cloud-native operations





## 🙋‍♀️ Author

Shreya S V

DevOps Learner | Kubernetes | Monitoring | Cloud
