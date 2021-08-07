
##SIMPLE TO-DO APPLICATION ON MERN WEB STACK

Objective: The objective of this project is to create a simple To-do application using the MERN stack.

![image](https://user-images.githubusercontent.com/24277138/128539492-d72a9b5d-2ed9-40c8-b03c-edf5128a3e61.png)

##STEP 0 – PREREQUISITES

Linux machines, along with neccesary network permissions will be prerequisites, in this case we would proceed with Ubuntu Linux 20.04 ( Focal Fossa)

##STEP 1 – BACKEND CONFIGURATION

We upgrade and update the Platform to ensure up-to-date binaries.

Afterwards we get the location of Node.js software from Ubuntu repositories

![image](https://user-images.githubusercontent.com/24277138/128547479-027a3d85-5730-4147-812d-a38c3dfb7e22.png)

![image](https://user-images.githubusercontent.com/24277138/128547907-8b14afd3-b768-4a7b-9fc1-d652d9b6baf4.png)

Next we move to install node.js (N) as advised above.

![image](https://user-images.githubusercontent.com/24277138/128548966-69cd64ba-f095-4dd6-8d90-9e9180658cc2.png)

![image](https://user-images.githubusercontent.com/24277138/128573720-c80e402a-b5ae-41a4-abd7-85378a5b13e9.png)

We now initialize the project with the npm init command.

![image](https://user-images.githubusercontent.com/24277138/128576293-37ccdb28-ad65-4ca6-8165-11cee58b7f60.png)


##STEP 2 INSTALL EXPRESSJS

We will install express and dotenv using npm while also create an index.js file

![image](https://user-images.githubusercontent.com/24277138/128577159-57b1c0ed-0e04-451c-9c36-0940fbb65c5b.png)

With the code on the index.js file

![image](https://user-images.githubusercontent.com/24277138/128577693-6f589b15-575f-4199-b33f-f9350e68ac4d.png)

As highlighted above, we are using port 5000 for the application.

![image](https://user-images.githubusercontent.com/24277138/128577860-1ab06cda-9291-4212-b10b-4f328ae151f1.png)

If we recall, our To-do application needs to be able to at least three things.

1) Create a new task
2) Display a list of all task
3) Delete a completed task

Each task will be associated with some particular endpoint and will use different standard HTTP request methods: POST, GET, DELETE.

Hence, for each task, we need to create routes that will define various endpoints that the To-do app will depend on. So let us create a folder routes

![image](https://user-images.githubusercontent.com/24277138/128578982-52c65d2d-0416-43a1-8087-fccc3d1c18b7.png)

Next we go ahead to create models

A model is at the heart of JavaScript based applications, and it is what makes it interactive

To create a Schema and a model, install mongoose which is a Node.js package that makes working with mongodb easier.

![image](https://user-images.githubusercontent.com/24277138/128581621-9e638cbf-5554-455b-b87e-7b50c76e598d.png)

![image](https://user-images.githubusercontent.com/24277138/128582558-6733d868-1826-4a63-bd93-bc6df079f18c.png)

Afterwardsupdate our routes from the file api.js in /routes directory to make use of the new mode

![image](https://user-images.githubusercontent.com/24277138/128582862-e1d19dfc-bd86-4b13-ae9c-3ea8b0abccd6.png)


##STEP 5 MONGODB DATABASE INSTALLATION

As expected we would require a database for our To-do Application. For this we will make use of mLab. mLab provides MongoDB database as a service solution (DBaaS)

We will sign up for a new account and add an access-list

![image](https://user-images.githubusercontent.com/24277138/128583727-8f977794-4be5-4d2e-aacb-a532f2c51095.png)



