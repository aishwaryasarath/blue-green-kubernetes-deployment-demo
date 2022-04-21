# blue-green-kubernetes-deployment-demo
A blue green deployment demo on kubernetes
1. Create a namespace
<img width="295" alt="image" src="https://user-images.githubusercontent.com/49971693/164511296-a3ac799a-c6fa-4715-a19d-a9cd15b74742.png">
<img width="308" alt="image" src="https://user-images.githubusercontent.com/49971693/164511515-535a5a03-cfe6-4e4e-b942-5dddb6214b0e.png">

2. Create the blue deployment
<img width="273" alt="image" src="https://user-images.githubusercontent.com/49971693/164511414-94145160-dfb0-42ff-9fbe-99338f4f2267.png">
<img width="416" alt="image" src="https://user-images.githubusercontent.com/49971693/164511545-1fea16d5-d646-4142-9f60-8919c7c29bed.png">
<img width="1263" alt="image" src="https://user-images.githubusercontent.com/49971693/164511569-195e8856-1916-4c62-9158-ba13b317cee8.png">

3. Create a service for the deployment
4. 
5. Copy the existing deployment file blue.yaml to yaml.yaml
6. Change labels in delpoyment selector matchLabels from env: original to env: green
7. Confirm the new green deployment is working
8. Edit the app service to point the selectors to green
9. Confirm the new service is working
