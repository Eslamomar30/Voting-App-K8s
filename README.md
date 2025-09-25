 Project Description: Voting App on Minikube (Kubernetes)

This project showcases the deployment of a containerized microservices voting application on a Minikube Kubernetes cluster using declarative YAML manifests.

🛠️ Components & YAML Files:

vote-deployment.yaml → Python frontend app for voting.

result-deployment.yaml → Node.js frontend app to display results.

worker-deployment.yaml → Background service to process votes.

redis-deployment.yaml → In-memory database for temporary vote storage.

db-deployment.yaml → PostgreSQL database for persistent vote storage.

ingress.yaml → NGINX Ingress configuration to expose services externally.

 Implementation Details:

Deployed all services on Minikube using kubectl apply -f *.yaml.

Configured ClusterIP Services to enable internal communication between Pods.

Used Ingress with host voting.local to route traffic:

/vote → vote frontend.

/result → result frontend.

Verified Pod communication with environment variables and debugging (kubectl exec, kubectl logs).

Solved common issues such as 500 Internal Server Error caused by DB connection.

Outcome:

Successfully deployed and tested the Voting App end-to-end on Minikube.

Demonstrated hands-on skills in Kubernetes deployments, services, ingress routing, and troubleshooting.

Built a working microservices pipeline with frontend, backend, cache, and database layers.
