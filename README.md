# jenkins2025

## Jenkins Server Setup
### Jenkins Installation

Continuous Integration (CI) and Continuous Delivery/Deployment (CD) are foundational practices in modern DevOps workflows. CI involves developers frequently integrating code into a shared repository, triggering automated builds and tests to detect issues early. CD extends this by automatically delivering or deploying tested code to production or staging environments, ensuring faster and more reliable software releases.

Jenkins is a widely used open-source automation server that plays a crucial role in enabling CI/CD. It allows teams to define custom pipelines (using Jenkinsfiles) that automate building, testing, and deploying software. Jenkins supports integration with various tools like Git, Docker, Maven, and Kubernetes, making it highly flexible in managing end-to-end delivery pipelines.

By automating repetitive tasks and reducing manual intervention, Jenkins enhances the consistency, speed, and quality of software delivery. Its plugin ecosystem and scalability make it a central component in implementing DevOps practices, facilitating continuous feedback and rapid iteration.

In essence, Jenkins is not just a tool for automation—it is a critical enabler of CI/CD pipelines that drive modern, agile, and resilient software development processes.



To Install Jenkins the following steps were taken
1. Spun up an EC2 Server on AWS
2. Allowed Network access to the internet on ports 22, and 8080
3. Updated package reporisoties
4. installed java jdk
5. installed jenkins
![Alt text](./Status.png)
![Alt text](./Jenkinsimage.png)
6. Connected Jenkins to github account
7. Ran simple freestyle job to demonstrate build
![Alt text](./JenkinsJob.png)


Jenkins Pipeline Implementation Documentation
1. Jenkins Installation and Setup
Jenkins was successfully installed on a local Ubuntu environment. After installation, the service was started and configured via the web interface using the default admin credentials. Required plugins, including Git, Docker, and Pipeline, were installed to support CI/CD tasks.

2. Docker Installation and Integration
Docker was installed and configured on the same host. Jenkins was granted permission to interact with the Docker daemon by adding the Jenkins user to the Docker group. This enabled the pipeline to build and run Docker containers directly from within Jenkins.

3. Project Repository Integration
A public Git repository was connected to Jenkins. This repository contained the application source code and a Jenkinsfile for pipeline execution. Jenkins was configured to poll the repository for changes and trigger builds automatically.

4. Jenkinsfile Pipeline Configuration
A Jenkinsfile was created and committed to the project repository. The pipeline defined in the Jenkinsfile included multiple stages:

Clone Repository – pulled the latest code from the remote Git repository.

Build Docker Image – built a Docker image using the application’s Dockerfile.

Run Docker Container – deployed the application in a Docker container, mapping appropriate ports.

5. Pipeline Execution and Deployment
The pipeline was successfully executed within Jenkins. All stages completed without error, demonstrating end-to-end automation from code commit to containerized deployment. Logs and stage outputs were verified through the Jenkins UI to confirm successful implementation.


