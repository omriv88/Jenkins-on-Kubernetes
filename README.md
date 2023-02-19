# Isntall Jenkins on Kubernetes 

  
Step - 1 - Installing Jenkins on Kubernetes
  - kubectl create namespace jenkins
  - kubectl create -f jenkins.yaml --namespace jenkins
  - kubectl get pods -n jenkins
  - kubectl create -f jenkins-service.yaml --namespace jenkins
  - kubectl get services --namespace jenkins

Step - 2 - Accessing the Jenkins UI
  - kubectl get nodes -o wide
  - kubectl get pods -n jenkins
  - check the Pod’s logs for the admin password : 
    - 1 kubectl logs jenkins-r6g53rg5-nrg3 -n jenkins
    - 2 Copy your_jenkins_password, return to your browser and paste it into the Jenkins UI.
