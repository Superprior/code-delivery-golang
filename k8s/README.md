## About
- Kubernetes deploy

---

## Run the application
Before:
- Generate Kafka cluster API key & secret, [Confluent](https://www.confluent.io/)
- Generate Google Maps API Key
- Config .env of each project with credentails generated above
- Edit confimap.yaml of the simulator and backend folders with .env variables
- Connect to a kubernetes container cluster, [Google Cloud Kubernetes](https://cloud.google.com/kubernetes-engine) recommended.

Execute:

```bash
# simulator
kubectl apply -f simulator/configmap.yaml
kubectl apply -f simulator/deploy.yaml

# backend
kubectl apply -f backend/configmap.yaml
kubectl apply -f backend/deploy.yaml
kubectl apply -f backend/service.yaml

# frontend
kubectl apply -f frontend/configmap.yaml
kubectl apply -f frontend/deploy.yaml
```