-> In this projects i have implemented  CI/CD pipeline using GitHub Actions to automate build of Spring Boot application, Docker image creation , push , and Kubernetes deployment.

-> .github/workflows/main.yml :- path for yaml file or pipeline

-> This project has integration of all the components include jobs ,steps , actions and management of secrets in github .

-> Created Self hosted runner in aws for build :-

steps :- 

# Create a folder
$ mkdir actions-runner && cd actions-runner# Download the latest runner package
$ curl -o actions-runner-linux-x64-2.333.1.tar.gz -L https://github.com/actions/runner/releases/download/v2.333.1/actions-runner-linux-x64-2.333.1.tar.gz# Optional: Validate the hash
$ echo "18f8f68ed1892854ff2ab1bab4fcaa2f5abeedc98093b6cb13638991725cab74  actions-runner-linux-x64-2.333.1.tar.gz" | shasum -a 256 -c# Extract the installer
$ tar xzf ./actions-runner-linux-x64-2.333.1.tar.gz

Configure
# Create the runner and start the configuration experience
$ ./config.sh --url https://github.com/AmanRaut29-sudo-1/Github-actions --token BR646LLEUIIDLKO2SDFQSXDJ2IQB2# Last step, run it!
$ ./run.sh

Using your self-hosted runner
# Use this YAML in your workflow file for each job
runs-on: self-hosted

Workflow :-

git push ->  GitHub Actions Trigger ->  Build JAR -> Upload artifact ->  Build Docker image ->  Push DockerHub -> Deploy Kubernetes 


<img width="2926" height="980" alt="image" src="https://github.com/user-attachments/assets/5701f653-41dd-42cc-b6df-85bfe87e9006" />
