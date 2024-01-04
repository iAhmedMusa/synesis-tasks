# Instructions on how to access the deployed application

### Kubernetes Deployment

1. Install and configure Minikube/Docker-desktop or use a Kubernetes cluster of your choice.

2. Deploy the application using Kubernetes manifests:

3. Clone the repository:

```bash
git clone https://github.com/iAhmedMusa/synesis-tasks.git
cd assignment-3/k8s
```

4. Create a namespace `synesis` inside of the cluster

```bash
kubectl create namespace synesis
```

5. Deploy Secrets, ConfigMap, Deployments, Services, etc:

```bash
- kubectl apply -f secrets.yml
- kubectl apply -f configmap.yml
- kubectl apply -f postgres-pvc.yml
- kubectl apply -f postgres.yml
- kubectl apply -f backend-app.yml
- kubectl apply -f frontend-app.yml
```

6. See all resources:

```bash
kubectl get all -n synesis
```

7. Monitor the deployments:

```bash
kubectl get pods -n synesis
```

8. Get all services and access the application according to :

```bash
- kubectl get svc -n synesis
```

Visit the external IP to access the application.

The application will be accessible at [http://localhost:3000](http://localhost:3000).
