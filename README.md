## 🌐 Kubernetes Monitoring Project – Prometheus + Grafana

This project showcases real-time monitoring of a custom Kubernetes application using Prometheus and Grafana.
The app — Shreya-K8s-App — exposes metrics that are scraped by Prometheus and visualized in Grafana dashboards.

# 📌 Project Architecture

Kubernetes Cluster
└── Custom App (Python + Flask)
└── Exposes metrics on /metrics
└── Prometheus
└── Scrapes metrics from the App
└── Grafana
└── Visualizes Prometheus metrics via dashboards

# 🎯 What I Implemented

✔ Deployed a Flask web application on Kubernetes
✔ Enabled monitoring through Prometheus annotations
✔ Configured Prometheus scrape jobs
✔ Integrated Grafana for dashboard visualization
✔ Created a custom dashboard displaying app status with my app label
✔ Successfully tracked uptime & active deployments



# 📌 Key Features

✔ Kubernetes deployment
✔ Monitoring annotations
✔ Auto-discovered app metrics
✔ Custom uptime graph
✔ Uses standard PromQL query
✔ Your name visible on dashboard (unique!)


# 🚀 Technologies Used
  Tool                Purpose
Kubernetes	     Application Deployment
Prometheus	     Metrics Collection
Grafana	         Metrics Visualization
Docker	         Application Containerization
Python           Flask	Custom App
YAML	           Kubernetes Manifests


# 📂 Project Structure
kubernetes-monitoring-project/
│
├── app/
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
│
├── kubernetes/
│   ├── deployment.yaml
│   └── service.yaml
│
├── monitoring/
     ├── prometheus-configmap.yaml
     ├── prometheus-deployment.yaml
     ├── prometheus-service.yaml
     ├── grafana-deployment.yaml
     └── grafana-service.yaml


     
# ⚙️ How to Deploy (Steps)
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



# 📸 Results & Dashboards
<img width="1920" height="1080" alt="kubernetes app output" src="https://github.com/user-attachments/assets/0bbbe51a-700a-4985-b746-46153cb9b5af" />

<img width="1920" height="1080" alt="k8s-prometheus pods running" src="https://github.com/user-attachments/assets/99a51a08-9b0b-48e3-b3c7-8864702ece01" />

<img width="1920" height="1080" alt="prometheus-overview-dashboard" src="https://github.com/user-attachments/assets/395fb7c5-c025-4a51-aa34-af91170cdc48" />

<img width="1920" height="1080" alt="grafana-custom-app-up-metrics" src="https://github.com/user-attachments/assets/d4785c6a-11c5-490a-99a6-ada85a8b17e3" />
# 🛡 Project Status

🚀 Monitoring is working successfully
📈 Metrics shown live in Grafana with app name: shreya-k8s-app



# 🛠 Why This Project is Used in Real-World

Companies use Kubernetes Monitoring to:

    Goal	                                                Why It Matters
Track application health	                         Avoid downtime & failures
Detect performance issues early             	     Better user experience
Visualize system activity	                         Faster troubleshooting
Monitor scaling & resource usage	                 Cost savings & autoscaling
Production SRE/DevOps Observability	               Mission-critical operations



# 🙋‍♀️ Author

Shreya S V
DevOps Learner | Kubernetes | Monitoring | Cloud
