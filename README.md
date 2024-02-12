**Proof of Concept (POC) Description**
This initiative entails deploying a Flask application while also committing the code to GitHub. Jenkins orchestrates the process by establishing an image pipeline, culminating in the creation of the image in Docker Hub. Furthermore, Jenkins manages an additional pipeline dedicated to updating the Kubernetes deployment manifest file. Argo CD assumes a pivotal role in automating the deployment of the desired application states within the Kubernetes cluster environment.

**Implementation Method**

**Installation**
This repository, in conjunction with kubernetesmanifest https://github.com/jayshankar80/kubernetesmanifest, facilitates the establishment of a Jenkins pipeline imbued with GitOps principles for deploying code into a Kubernetes cluster. Continuous Integration (CI) responsibilities are undertaken by Jenkins, while Continuous Deployment (CD) tasks are delegated to ArgoCD (GitOps).

Jenkins Installation: Jenkins is deployed on an EC2 instance. Refer to the instructions outlined in Jenkins Documentation for installation guidance. https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/ . 
Docker Installation: After setting up Jenkins, install Docker on the EC2 instance. Follow the steps elucidated here. Alternatively, you can utilize your preferred Linux system with the requisite packages installed.
 https://serverfault.com/questions/836198/how-to-install-docker-on-aws-ec2-instance-with-ami-ce-ee-update

Git Installation: Install Git on the EC2 instance using the command sudo yum install git.

Kubernetes and ArgoCD Installation: For local development, Kubernetes (kubectl) is installed on a macOS system. ArgoCD installation instructions are available here.
Pipeline Configuration  https://argo-cd.readthedocs.io/en/stable/getting_started/

**Pipelines Configuration**

Kindly refer to the attached screenshot for the Jenkins pipeline configuration pertinent to each repository. You can locate the screenshot in the respective repository folder.

**Troubleshooting**
In case of encountering permission issues while attempting to login to Docker Hub from an AWS Linux virtual machine, consider the resolution steps outlined in this Stack Overflow thread.
make sure you install docker-pipeline from manage-pluging im jenkins else you will face grovey Java error while running the pipeline 


**Resulted Output**

Kindly refer to the attached screenshot for running buildimage, updatemanifest and ArgoCD pipeline 
