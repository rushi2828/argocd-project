# Deploying Pet-Clinic (Spring Boot App) with Argo CD
### # Using Pet-Clinic image from Dockerhub
![image](https://github.com/user-attachments/assets/227fe835-0e88-407e-b515-7fc924b0cfbe)

### # Stat Minikube cluster
![image](https://github.com/user-attachments/assets/e11faf5d-8190-498f-82a4-d6845e16e1ea)

### # Install helm chart: https://helm.sh/docs/intro/install/
![image](https://github.com/user-attachments/assets/4052682b-a457-4a3b-b8e4-cc049425734a)

### # Create helm chart for pet-clinic
![image](https://github.com/user-attachments/assets/3d14fce7-a627-4bbd-af2b-ab9262f680a1)

### # Update values.yaml with image name and tag.
![image](https://github.com/user-attachments/assets/111249f2-93ab-4a71-a5dc-9a41155df9b8)

### # Also update service type from ClusterIP to NodePort
![image](https://github.com/user-attachments/assets/cc9140de-77f8-42f0-8a61-019da7692830)

### # Updated file pushed to git repository
![image](https://github.com/user-attachments/assets/8bbbddc9-bf32-4451-bf15-b16deefdf024)

### # Git repo look like
![image](https://github.com/user-attachments/assets/1e13cd08-6bfe-45c4-ae00-7761a7d7d757)

### # Install ArgoCD : https://argo-cd.readthedocs.io/en/stable/getting_started/
![image](https://github.com/user-attachments/assets/f804e95a-0514-4537-8c0a-70a0c3ad5f7a)

### # Open ArgoCD UI with using port-forwording
kubectl port-forward svc/argocd-server -n argocd 8080:443
![image](https://github.com/user-attachments/assets/262a3fe1-43cc-4254-9d61-8f3b12fcafdf)

### # Get password and logged in
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
![image](https://github.com/user-attachments/assets/8a255688-bc1a-4f89-8b0c-1bd31b4e9003)

### # Configure git repo with ArgoCD
![image](https://github.com/user-attachments/assets/f5711ecb-39ab-4c19-949c-cb6a1453648a)

### # Create application in argocd
![image](https://github.com/user-attachments/assets/8643d50f-c227-49a2-9d2e-4d804ccba995)
![image](https://github.com/user-attachments/assets/165647fd-e92a-4299-8dab-a2abe71d026f)
![image](https://github.com/user-attachments/assets/1226b984-13a7-41a4-9195-c3077b52b174)

### # Sync the project
![image](https://github.com/user-attachments/assets/5130718b-d85f-4845-984a-07ed0f921f47)

### # Verify pod in details:
![image](https://github.com/user-attachments/assets/409db75d-ee31-44df-8e8c-c561fdd85585)

### # Updated replicas from 1 to 4 in values.yaml file and pushed 
![image](https://github.com/user-attachments/assets/c473f4f3-518a-43ff-8704-6767db7690cc)
![image](https://github.com/user-attachments/assets/031f5556-ef02-447f-9b98-fd3e18b8df97)

### # ArgoCD automatically updated pod with 4 replicas
![image](https://github.com/user-attachments/assets/17810b72-bf83-4ebe-9837-0b46f87ef968)
