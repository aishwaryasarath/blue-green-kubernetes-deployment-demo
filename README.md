# blue-green-kubernetes-deployment-demo
A blue green deployment demo on kubernetes
1. Create a namespace

```
kubectl create ns bluegreen-ns
```
<img width="308" alt="image" src="https://user-images.githubusercontent.com/49971693/164511515-535a5a03-cfe6-4e4e-b942-5dddb6214b0e.png">

2. Create the blue deployment & check the presence of the pods
```
kubectl create -f blue.yaml
kubectl get po -n bluegreen-ns
```
<img width="1263" alt="image" src="https://user-images.githubusercontent.com/49971693/164511569-195e8856-1916-4c62-9158-ba13b317cee8.png">

3. Create a service for the deployment
```
kubectl create -f blue-svc.yaml
```
<img width="331" alt="image" src="https://user-images.githubusercontent.com/49971693/164517121-947aed0c-5b75-4840-b9fb-0d3db17ed0a5.png">

4. Confirm that it works

```
Get the node IP & node port number
kubectl get nodes -o wide
kubectl get svc -n bluegreen-ns
```
<img width="718" alt="image" src="https://user-images.githubusercontent.com/49971693/164519725-02b87d01-d2f5-40eb-b9c5-6ea5608d30bd.png">
<img width="816" alt="image" src="https://user-images.githubusercontent.com/49971693/164519817-a2893d4f-edc3-46c2-9bc1-3bee548dcd31.png">

```
Exec into one of the blue pods
```
<img width="493" alt="image" src="https://user-images.githubusercontent.com/49971693/164519556-b2a5d126-200a-4efa-b3e1-fc65a2fc31f2.png">

```
Curl the nodeIP:nodePort to check if it is running as expected
```
<img width="635" alt="image" src="https://user-images.githubusercontent.com/49971693/164519896-831a5aaa-71c4-4d9e-b1c8-ed24d5d7832a.png">

5. Copy the existing deployment file blue.yaml to green.yaml. Change labels in delpoyment selector matchLabels from env: original to env: green and deploy the green deployment.
```
kubectl create -f green.yaml
kubectl get deploy -n bluegreen-ns
```
<img width="419" alt="image" src="https://user-images.githubusercontent.com/49971693/164517578-a8ebf1c2-5e00-4003-abf9-52e42851bb9a.png">
<img width="548" alt="image" src="https://user-images.githubusercontent.com/49971693/164517537-0c5e85c3-7129-44f2-b665-b20a8411c815.png">

6. Confirm the new green deployment is working
```
kubectl exec -it web-frontend-7459c9fcdc-fqmh2  -n bluegreen-ns -- bash
```
<img width="503" alt="image" src="https://user-images.githubusercontent.com/49971693/164532842-4cf16903-87b5-4295-9b0a-62d10938ec1e.png">

8. Edit the app service to point the selectors to green
   
10. Confirm the new service is working
