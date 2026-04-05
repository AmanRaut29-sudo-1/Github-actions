-> Implemented CI/CD pipelines using GitHub Actions to automate build of Spring Boot application, Docker image creation , push , and Kubernetes deployment.
-> .github/workflows/main.yml :- path for yaml file or pipeline
-> This project has integration of all the components include jobs ,steps , actions and management of secrets in github .

Workflow :-

git push
   ↓
GitHub Actions Trigger
   ↓
Build JAR
   ↓
Upload artifact
   ↓
Build Docker image
   ↓
Push DockerHub
   ↓
Deploy Kubernetes


<img width="2926" height="980" alt="image" src="https://github.com/user-attachments/assets/5701f653-41dd-42cc-b6df-85bfe87e9006" />
