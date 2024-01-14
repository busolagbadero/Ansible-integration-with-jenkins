# Integration-of-Ansible-Playbooks-with-Jenkins
This guide outlines the process of integrating Ansible with Jenkins using a Jenkinsfile. The Jenkins pipeline defined in the Jenkinsfile automates the execution of an Ansible playbook to configure EC2 instances. This integration allows for streamlined and automated infrastructure configuration.

## Prerequisites
Before proceeding with the integration, ensure the following prerequisites are met:

- Jenkins Installation: Jenkins should be installed and configured in your environment.

- Ansible Installation: Ansible must be installed on the Jenkins server or the agent where the pipeline will be executed.

- SSH Key Pair: Ensure that you have an SSH key pair to authenticate with the target server where Ansible will run the playbook.
  
- SSH Pipeline Steps Plugin: Install the SSH Pipeline Steps Plugin in Jenkins.

## Jenkinsfile Overview
The provided Jenkinsfile is a declarative pipeline that defines a single stage to execute an Ansible playbook. Here's a brief overview of the Jenkinsfile:

![ans2](https://github.com/busolagbadero/Integration-of-Ansible-Playbooks-with-Jenkins/assets/94229949/5d9118f6-11e5-4ef8-9d78-5bfc20268658)

## Usage
- Configure Jenkins Credentials:

Ensure that you have the SSH private key stored as a Jenkins credential. In the provided Jenkinsfile, it refers to the credential with the ID 'eks-pem-ubuntu'. Update the credentialsId on jenkins accordingly.

- Update Ansible Server Information:

Set the correct IP address or hostname of your Ansible server in the ANSIBLE environment variable.

- Update Ansible Playbook:

The Jenkinsfile executes the Ansible playbook named docker-playbook3.yaml. Update the playbook name or path as needed.

- Run the Pipeline:

Trigger the Jenkins pipeline, and it will execute the defined stage to run the Ansible playbook on the specified Ansible server.

![ans3](https://github.com/busolagbadero/Integration-of-Ansible-Playbooks-with-Jenkins/assets/94229949/78e6660f-e5d1-4642-9a5d-6803da1be05c)

![ans4](https://github.com/busolagbadero/Integration-of-Ansible-Playbooks-with-Jenkins/assets/94229949/6fd376d2-57e5-4ebd-bd0f-1045f16e7c6c)

![ans5](https://github.com/busolagbadero/Integration-of-Ansible-Playbooks-with-Jenkins/assets/94229949/abfeef07-d0f2-4be1-97ff-d585efcaed77)

![ans6](https://github.com/busolagbadero/Integration-of-Ansible-Playbooks-with-Jenkins/assets/94229949/3c511552-6196-48a1-8f99-ddec2566ad78)

## Additional Notes
The inclusion of the ansible.sh script is optional and can be removed if Ansible and its dependencies are already installed on the target server.


