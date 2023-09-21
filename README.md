# Setting Up Angular on Codesphere: A Comprehensive Guide


## [1] run the "Prepare" stage of the CI-Pipeline. This may take a few moments as the Angular CLI and NVM (Node Version Manager) will be installed.



Afterwards, you need to run the following command in a terminal to change the Node.js version that is compatible with Angular:

```
source ~/.nvm/nvm.sh && nvm install 18.10 && nvm use 18.10
```


## [2] Now, you can initialize your first-ever Angular project on Codesphere with the following command:

```ng new [ ]```

You need to replace "[ ]" with the name you want to give your project, but please note that there are some adjustments in the code if you do so.
You will be asked some questions in the terminal which you need to answer to proceed. You can decide how you answer these questions but generally you would enable Angular routing.
This command initialize a new project and generate all basic files you need to develope a Angular project.



# Setting Up the Server Environment:

## [3] move the server.js file
Go into the "angu" folder and right-click on "server.js," then select "Rename." Replace "angu" in the path with the name of your project folder. 
If you choose another project name, you'll need to replace "angu" in line 9 of the "server.js" file with your own project name.




## [4] insert the following command into the terminal:

```cd angu/ && ng build --configuration production && npm install --save express```
Again, replace "angu" with your project folder name. This may take a few moments. 


## [5] deploy the WebApp
Start the run stage of the CI-Pipeline. Remember to replace angu in "cd angu/" in the CI-Pipeline to your project name. You can do that by clicking configure and afterwards clicking edit. If you are done, submit the changes below in the menu.
If you do so, you'll see the provided Angular template, and your WebApp will be online. You can click the “open your deployment” button on the top right corner to open a new task in your browser to see your webpage. Now you would see the Angular starter Template.


# Development:

While developing your web app, there's another way to deploy it. Insert the following command in the terminal:
```ng serve --port 3000 --host 0.0.0.0 --public-host XXXXX-3000.2.codesphere.com```

Replace "XXXXX" with the number of your URL. This mode is useful during development, as you can see every change you make to your code directly in the browser. Every time you save your code changes with Ctrl + S, the code gets compiled and deployed to the server.



# Getting Started with the PDF Merge Tool:

To begin using the PDF Merge Tool, delete the "src" folder in your project folder and insert the "src" directory from the "angu" folder of the project into your project folder. You can do this by changing the name, which will also allow you to set up the path for the directory.

Also we need to install some additional libraries for this project:
Run this command in the terminal 
```npm install @angular/cdk && npm install pdf-lib```


Now you can deploy again either with the ng serve command. When you want to deploy your finished project with the run section of the CI-Pipeline, you need to run ng build --configuration production && npm install --save express in the project folder again to save all your changes.





