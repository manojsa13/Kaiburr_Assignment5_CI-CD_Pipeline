## CI/CD Pipeline Project

I have done a CI/CD end to end pipeline for the task. <br />
For the pipeline I have made a normal user interface to get a information as a survey,
The HTML and CSS code but run in jsp &
Maven is used in the jenkins to the build the code.<br /><br />

This image is a base outline for CI/CD pipeline I made. 
![image](https://user-images.githubusercontent.com/63357275/228558186-e676ec7c-8aff-4719-b06c-867034c180cc.png)
<br /> In have launched a multiple instance to delopy jenkins, tomcat, docker, anisble and kubernetes.
![image](https://user-images.githubusercontent.com/63357275/228557688-6b3440eb-df85-4410-b461-120a1b923d24.png)
<br /><br /> As show in the first image I have used git to commite the code and added thoses chances added to the github using gitbash after this the code pulled from the github to build code in the maven through jenkins. As shown in image below I have made to jobs, in the CI if there is any changes in code CI will automatically deloyed using the poll function and CD is called after the of the CI build.
![Screenshot 2023-03-29 191653](https://user-images.githubusercontent.com/63357275/228560082-d8291e67-a6a5-4640-b72f-6a9c4f31a861.png)
<br /><br /> As I mentioned before the image shows the process of poll
![image](https://user-images.githubusercontent.com/63357275/228560752-bea4db64-b1a6-4edc-9535-b1f6f40bcccc.png)
<br /><br />Just given  the pom.xml file and goal to deploy.
![image](https://user-images.githubusercontent.com/63357275/228560981-1416ad89-3acd-4430-8eda-5f94853fc7a2.png)
<br /><br /> Here I had given the trigger option to start CD process after CI.
![image](https://user-images.githubusercontent.com/63357275/228561269-442ee326-1db5-4f38-8bd8-fb22b2591979.png)
<br /><br /> Here I have given the ssh server direction to access the webapp and given a executable command to get ansible playbook fo r creating the docker image.
![image](https://user-images.githubusercontent.com/63357275/228561772-f685b795-972a-4161-a5a1-bbdc7c694254.png)
Here you see the modules built and successful completion of the CI process and the trigger of CD process.
![image](https://user-images.githubusercontent.com/63357275/228563163-59e898b4-272f-4bac-9384-7f1eb772ec1c.png)
<br /><br /> Here you could see the successful completion of the console ouputs.
![image](https://user-images.githubusercontent.com/63357275/228563770-033c5cd8-6fbb-41fd-a8f3-eae03647715b.png)
<br /><br />It is a dockerfile used to create image in tomcat to deploy the final output in the ansible server.
![image](https://user-images.githubusercontent.com/63357275/228568814-15f22245-6652-40f6-ba13-5849456d85de.png)
<br /><br />Here you could see a ansible playbook to create image using dockerfile and then it has the command to push the docker images to docker hub.
![image](https://user-images.githubusercontent.com/63357275/228569581-16c7f223-aa5f-44dd-9f40-939d7979d512.png)
<br /><br /> Here you could see a preview of my dockerhub, the regapp is the docker image it is pushed newly by ansible playbook commands for every execution command. 
![image](https://user-images.githubusercontent.com/63357275/228572303-cf399e72-f6e3-4c5d-b3fb-04cd5ad33897.png)
<br /><br /> Here kubernets deployment and service yml called through ansible book.  
![image](https://user-images.githubusercontent.com/63357275/228570662-d0b1f4e6-7c3f-4ac4-ae74-abdd7b955b08.png)
<br /><br /> Here you could see the deployment yml file of kubernets to create the pods.
![image](https://user-images.githubusercontent.com/63357275/228593602-b17acf21-810a-437f-8918-4032ab4dbd25.png)
<br /><br /> In the image you will find the service yml of kubernerts to deploy the service.
![image](https://user-images.githubusercontent.com/63357275/228594354-52b1ec37-f299-4255-a413-07b8d9355df5.png)
<br /><br /> Here you will see the number of pods and service created in the EKS Elastic kubernets through "kubectl get all" command.
![image](https://user-images.githubusercontent.com/63357275/228572851-5dfdec10-d84a-4dda-be8d-5cc575a17809.png)
<br /><br />In this page you could see the configure page for CD job and SSH server for ansible to execute command to run kubernets deployment file.
![image](https://user-images.githubusercontent.com/63357275/228582208-db478ff3-cab0-4b3f-ae4a-2bde88a32ae2.png)
<br /><br /> Here you will see the creation of load balance and the aws link to deploy the builded code in server. 
![image](https://user-images.githubusercontent.com/63357275/228573121-7e13a07a-54d2-4add-b557-f7471fd14e8a.png)
<br /><br />  In this image you could see the cloudformation to deploy the code in the server.
![image](https://user-images.githubusercontent.com/63357275/228573394-92fa37ae-c1c0-44dc-90a6-b238c44780d5.png)
<br /><br /> Through this picture you will find the modules build and deployed in the Continuous deployment/delivery part. 
![image](https://user-images.githubusercontent.com/63357275/228581514-ecc23659-2e49-43d8-8d8f-1e2069c1ac2f.png)
<br /><br /> Through this process I have succefully deployed and hosted the webapp in the Elastic kubernets container with end to end fully CI/CD pipeline every change in continuously build and deployed in the server.
<br />#Final image
![image](https://user-images.githubusercontent.com/63357275/228573758-83a928b6-7b2c-4a45-b40a-fc4976004fdf.png)
<br /><br /> Link for the deployed CI/CD connection webpage <br /><br />
http://a0d3485e498a447b19767e8806824c90-1960516858.us-east-1.elb.amazonaws.com:8080/webapp/
