# blue-green-kubernetes-deployment-demo
A blue green deployment demo on kubernetes
1. Copy the existing deployment file app.yaml to app-green.yaml
2. Change labels in delpoyment selector matchLabels from env: original to env: green
3. Confirm the new green deployment is working
4. Edit the app service to point the selectors to green
5. Confirm the new service is working
