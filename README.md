# Jenkins-K8S


1. Deploy jenkins with master and slave using helm chart

  helm install --name my-release stable/jenkins

2. Create a jenkins job using the pod template plugin to run an ubuntu pod nd use it to run the command: df -h

  kubectl get svc my-release-jenkins -o=jsonpath='{.spec.ports[?(@.port==8080)].nodePort}'
  
  
3. Describe what just happened.


printf $(kubectl get secret --namespace default my-release-jenkins -o
jsonpath="{.data.jenkins-admin-password}" | base64 --decode);echo
