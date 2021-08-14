
##SIMPLE TO-DO APPLICATION ON MERN WEB STACK

Objective: The objective of this project is to create a simple To-do application using the MERN stack.

![image](https://user-images.githubusercontent.com/24277138/128539492-d72a9b5d-2ed9-40c8-b03c-edf5128a3e61.png)

##STEP 0 – PREREQUISITES

Linux machines, along with neccesary network permissions will be prerequisites, in this case we would proceed with Ubuntu Linux 20.04 ( Focal Fossa)

##STEP 1 – BACKEND CONFIGURATION

We upgrade and update the Platform to ensure up-to-date binaries.

Afterwards we get the location of Node.js software from Ubuntu repositories

![image](https://user-images.githubusercontent.com/24277138/129426284-a537dc8e-9af3-4b85-b400-5d627aef6e2b.png)

![image](https://user-images.githubusercontent.com/24277138/128547907-8b14afd3-b768-4a7b-9fc1-d652d9b6baf4.png)

Next we move to install node.js (N) as advised above.

![image](https://user-images.githubusercontent.com/24277138/129426374-e907660d-b5e1-48a3-9db4-7b60a7448eb7.png)

![image](https://user-images.githubusercontent.com/24277138/129426444-97e929c8-0d0e-4c07-91af-472998ce808e.png)

We now initialize the project with the npm init command in the Todo directory

![image](https://user-images.githubusercontent.com/24277138/129426642-45d6cb1a-f1b5-461e-8ede-61ef0e93a21e.png)

Express is a framework for Node.js, hence a lot of things developers would have programmed is already taken care of out of the box. However it simplifies development, and abstracts a lot of low level details.

We're know installing Express in the Todo directory.

![image](https://user-images.githubusercontent.com/24277138/129426957-09ba731b-256b-41d0-a075-b316c97c32ca.png)

The dotenv is a simple way that allows us to create secret keys that application needs to function and also keep them from going public - basically a way to seperate secret from pubic source code

![image](https://user-images.githubusercontent.com/24277138/129427071-675fa6f9-309e-47f5-bc01-ec1a702d05df.png)

We then proceed to populating our index.js file - This ( index.js) is where we load the framwork and define the routes.

![image](https://user-images.githubusercontent.com/24277138/129427478-90630a9c-2516-4b80-aab9-9972a9ebe784.png)

We run the node index.js command, which shows in our browser.

![image](https://user-images.githubusercontent.com/24277138/129428237-0008bf1c-75dd-40d3-b26d-3b836dad5263.png)

While take into account our objective, our Todo application - The Todo Application needs to be able to do the following.

1) Create a new task
2) Display list of all tasks
3) Delete a completed task

Hence for each of these task, we would create routes that will define various endpoints (Each task will be associated with some particular endpoints) that the To-do app will depend on.
Creating a directory routes and creating the api.js

![image](https://user-images.githubusercontent.com/24277138/129428762-56678d1d-a59a-4662-baa1-f60b475bf515.png)






























##PS Do this project with sudo permissions not as root.

