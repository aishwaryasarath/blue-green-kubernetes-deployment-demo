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
<img width="289" alt="image" src="https://user-images.githubusercontent.com/49971693/164517095-6b7aa2ae-c844-45b5-bedf-334a77346afe.png">
<img width="331" alt="image" src="https://user-images.githubusercontent.com/49971693/164517121-947aed0c-5b75-4840-b9fb-0d3db17ed0a5.png">

4. Confirm that it works
```Get the node IP & node port number```
<img width="261" alt="image" src="https://user-images.githubusercontent.com/49971693/164519699-070148c0-ba31-4a80-94f0-a0f053f49439.png">
<img width="718" alt="image" src="https://user-images.githubusercontent.com/49971693/164519725-02b87d01-d2f5-40eb-b9c5-6ea5608d30bd.png">
<img width="186" alt="image" src="https://user-images.githubusercontent.com/49971693/164519798-c3cc3c10-76e9-4e9e-a5b8-478dc0439c41.png">
<img width="816" alt="image" src="https://user-images.githubusercontent.com/49971693/164519817-a2893d4f-edc3-46c2-9bc1-3bee548dcd31.png">
<img width="493" alt="image" src="https://user-images.githubusercontent.com/49971693/164519556-b2a5d126-200a-4efa-b3e1-fc65a2fc31f2.png">
<img width="635" alt="image" src="https://user-images.githubusercontent.com/49971693/164519896-831a5aaa-71c4-4d9e-b1c8-ed24d5d7832a.png">

5. Copy the existing deployment file blue.yaml to green.yaml. Change labels in delpoyment selector matchLabels from env: original to env: green and deploy the green deployment.
<img width="419" alt="image" src="https://user-images.githubusercontent.com/49971693/164517578-a8ebf1c2-5e00-4003-abf9-52e42851bb9a.png">
<img width="548" alt="image" src="https://user-images.githubusercontent.com/49971693/164517537-0c5e85c3-7129-44f2-b665-b20a8411c815.png">

6. Confirm the new green deployment is working
7. Edit the app service to point the selectors to green
8. Confirm the new service is working
