
##SIMPLE TO-DO APPLICATION ON MERN WEB STACK

Objective: The objective of this project is to create a simple To-do application using the MERN stack. See sample below.

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

Our database of choice is Mongodb, which is a NoSQL database, hence we need to create a model.
A model is at the heart of JavaScript based application making it interactive. And we will use models to define our database schema.
To create a schema and a model, we use mongoose, which is a Node.js package.

![image](https://user-images.githubusercontent.com/24277138/129429091-2dd1ee55-8ec0-4765-b160-5158f9811349.png)

![image](https://user-images.githubusercontent.com/24277138/129429194-7ee26d44-ddab-4288-8ec1-9b5bef852c03.png)

At this point we need to update the api.js file in the routes directory.

![image](https://user-images.githubusercontent.com/24277138/129429544-6b8c061c-35b3-4de8-97a7-ffaa6f73e964.png)

Once this is done we proceed to the MongoDB database
Since we need a database to  store our data, for this demonstration we would use mLab ( MLab provides MongoDB as a service DBaaS).
We will sign up for a free tier and explore !

We login and create a database named myFirstDatabase.

![image](https://user-images.githubusercontent.com/24277138/129429844-7755db00-02e8-41f7-a5c1-33d5b885f022.png)

Our index.js file specified process.env to access enviromental variables (since we installed dotenv) but the file has not been created.
creating a .env file in the Todo directory, and modify as so.

       DB = 'mongodb+srv://<#username#>:<#password#>@<network-address>/<dbname>?retryWrites=true&w=majority'

![image](https://user-images.githubusercontent.com/24277138/129430157-7eeba8f5-b691-41d6-b75a-7f280dfcdf60.png)

Next we update the index.js files to use the .env file we just created.

![image](https://user-images.githubusercontent.com/24277138/129430312-e6ff1604-b839-40c8-ae94-c6e693d56012.png)

![image](https://user-images.githubusercontent.com/24277138/129430355-c760fc33-2a8e-4517-9cd3-bc968dc945de.png)

At this point the backend of our To-Do application has been configured and it's connected to it's database.

Next milestone to set up our frontend which will be using ReactJS code, we will use Postman to test our API.

![image](https://user-images.githubusercontent.com/24277138/129430538-a2dd4ab7-0274-42d1-9628-fc6f0eb47605.png)

Using the GET command, we're able to get what we just posted and also the previous post into the database.

![image](https://user-images.githubusercontent.com/24277138/129430629-f8789ff5-769c-40db-a370-be2e224a2fd1.png)

With this we have successfully tested our backend application.

To proceed with the frontend application, we jump into the same directory where our backend application resides.

Installing create-react-app client - this will create a directory where the react code will be added.

![image](https://user-images.githubusercontent.com/24277138/129430807-92a684a0-ef98-43c1-b78b-f73e378af178.png)

![image](https://user-images.githubusercontent.com/24277138/129430844-25cd8da6-0c37-475a-abeb-55d95be4a11f.png)

Now we are installing concurrently - This is used to run more than one command from the same window.

![image](https://user-images.githubusercontent.com/24277138/129430914-76d22769-2ef1-4661-9a03-22aec4b8d51f.png)

The nodemon module is need to run and monitor the server i.e if there's any change in the server code, this module will restart it automatically and load the new changes.

![image](https://user-images.githubusercontent.com/24277138/129430954-6e421266-6653-454b-a289-e8d29d86f4cf.png)

Next we edit the package.json file into the Todo directory.

![image](https://user-images.githubusercontent.com/24277138/129431064-409a0171-b08d-4e55-a9ea-2893358f7514.png)

Now we move to the client directory and add the proxy settings to the package.json file in the client directory

![image](https://user-images.githubusercontent.com/24277138/129431241-0f4d0db3-9e77-4749-ad64-e49b4577a644.png)

As a milestone check we run the command npm run dev ( inside the Todo directory)

![image](https://user-images.githubusercontent.com/24277138/129431297-5b58b265-6826-4559-928b-dc52da920411.png)


To further our frontend development, we need to create three components ( two stateful and one stateless) in our client directory.

You can guess which is statefull or stateless amongst the files created.

![image](https://user-images.githubusercontent.com/24277138/129431497-94417be5-47c5-43f8-986b-4e1cb9b1e876.png)

We installed axios above which is a promise-based HTTP client for the browser and node.js

We now proceed back to the components directory and edit the remaining files.

![image](https://user-images.githubusercontent.com/24277138/129431588-72c7b8a9-1eb4-4414-981b-612a434b6b20.png)

![image](https://user-images.githubusercontent.com/24277138/129431649-93103afb-230f-4e3c-8bf9-2b30a3a7cf36.png)

All done, but an adjustment needs to be done to our react code in the src directory, App.js

![image](https://user-images.githubusercontent.com/24277138/129431838-fcfc6235-66f5-4b16-b940-c5025ca57fed.png)

And also the App.css and index.css
Since our application was never stopped, it simply kept re-compiling as more code was added.

![image](https://user-images.githubusercontent.com/24277138/129432018-b64fc61d-0eab-40ac-90f1-06eee9cdca71.png)

And we verify the web front-end. 

![image](https://user-images.githubusercontent.com/24277138/129432041-b07eab67-34ca-4b24-9fe4-fcb427bd889d.png)

