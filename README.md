Write your first declarative CI/CD pipeline using Jenkins

Setting Up Jenkins and Docker on EC2:
Launch an AWS EC2 instance, preferably with Ubuntu.
Configure inbound rules in the security group to allow traffic on ports 8080, 5000, and 22.
SSH into the instance and update the package repository: sudo apt update.
Install Java and Jenkins.
Install Docker and grant permissions to the ubuntu user and Jenkins to access Docker.
Reboot the instance.
Access Jenkins via the instance's Public IP on port 8080, set up the password, and complete the setup.
Reboot the instance again for changes to take effect.

Creating and Writing Multiple Stages in the Pipeline:
Log in to Jenkins, create a new pipeline item, and link it to your GitHub project.
Write the pipeline script with the following stages:
Clone Stage: Fetch the code from the Git repository.
Build Stage: Use Docker to build the application image from the Dockerfile.
Pushing the Image to DockerHub Stage: Push the Docker image to DockerHub.
Deploy Stage: Deploy the application container using Docker Compose.

Running Your Application as a Container Using Docker:
Initiate the pipeline build in Jenkins.
Monitor the pipeline's progress in the Jenkins dashboard.
Once the pipeline completes successfully, access your deployed application by visiting the EC2 instance's Public IP along with the specified port.

Additional Considerations:
Ensure Docker Compose is installed on the EC2 instance.
Maintain proper indentation in the Docker Compose file.
Securely configure DockerHub credentials in Jenkins for image push.
Verify each stage's success in the Jenkins pipeline dashboard.
Following these straightforward steps will enable you to establish a CI/CD pipeline for your Flask-based TODO app using Jenkins and Docker on an EC2 instance.






