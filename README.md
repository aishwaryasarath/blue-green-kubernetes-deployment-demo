# blue-green-kubernetes-deployment-demo
A blue green deployment demo on kubernetes
1. Create a namespace
<img width="295" alt="image" src="https://user-images.githubusercontent.com/49971693/164511296-a3ac799a-c6fa-4715-a19d-a9cd15b74742.png">
2. Create the blue deployment
<img width="273" alt="image" src="https://user-images.githubusercontent.com/49971693/164511414-94145160-dfb0-42ff-9fbe-99338f4f2267.png">

4. Copy the existing deployment file app.yaml to app-green.yaml
5. Change labels in delpoyment selector matchLabels from env: original to env: green
6. Confirm the new green deployment is working
7. Edit the app service to point the selectors to green
8. Confirm the new service is working
