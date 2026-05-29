# kubernetes-multi-service-app
Kubernetes Multi-Service Project – Short Notes
Project Overview

Built a microservices application on Kubernetes using multiple services:

Frontend Service (UI)
Backend Service (Python/Flask API)
PostgreSQL Service (Database)
Redis Service (Cache)
Components Used
Component	Purpose
Deployment	Manages Pods and self-healing
Service	Provides stable networking
PostgreSQL	Stores application data
Redis	Caching and fast data access
Kubernetes DNS	Service discovery
Docker	Containerization
Architecture
Frontend
    |
Backend API
   /    \
Postgres Redis
Key Kubernetes Concepts Demonstrated
Created Deployments for all applications.
Exposed applications using Services.
Used ClusterIP for internal communication.
Used NodePort for external access.
Verified Service Discovery using Kubernetes DNS.
Tested communication between Pods and Services.
Used Docker images from container registry.
Commands Used

Deploy:

kubectl apply -f .

Verify:

kubectl get pods
kubectl get svc
kubectl get deployments

DNS Check:

kubectl exec -it <pod-name> -- nslookup postgres-service
kubectl exec -it <pod-name> -- nslookup redis-service
Learning Outcomes
Container orchestration
Pod lifecycle management
Service discovery
Internal cluster networking
Microservices deployment
Kubernetes troubleshooting
Deployment and Service YAML creation
