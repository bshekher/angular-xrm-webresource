
# work-in-progress: I will remove this comment when done (2017-05-28). Expect it to happen within a few days.


# Building Microsoft Dynamic 365 WebResources with Visual Studio and angular 4

This project demonstrates an easy track to develop Microsoft Dynamic 365 WebResource components with angular 4. 

## How to use, and where will in end up leaving you.

This guide is a step by step guide for building a very simple Visual Studio Solution that will allow you to create a full angular 4 application that can run inside a Dynamic 365 solution, online or on-premises.

Even though a dynamic web resource is a web application, this project is using a simple command line tool as template. The reason for this is the basic nature of a dynamic 365 web resource. It only allow simple html, javascript, css and image files. Nothing else. So any Visual Studio Web template will add things that are not supported anyway, ex. ASP.NET controllers and more.
Secondly, the deployment model of web resources is also very strict. Files need to be uploaded to CRM as WebResources, and eventually they will be deployed as single files (possible in sub folder structure). The angular cli build process is a perfect resource to optimize and prepare as few files as possible to be uploaded. This project will show you how, and even give you the needed code to automate the process. The automation process is included in the command line tool (Deploy).

## The following topics will be covered

1. Creating a solution
1. Create an angular application with angular cli
1. Add the angular application to your solution
1. Deploy the application to your Dynamic 365

## Creating a solution

This project is a demo reference only, so the best starting point is proberbly not just to download this solution. But in very few steps, you can have your own solution up running.

1. Open visualstudio
1. Create new project, using the template [Other Project Types > Visual Solutions > Blank Solution ], in this guide I assume you are naming i ''''MyAngularSolution''''
1. Add a Command line project to the solution, name it Deploy, because that is what is eventually gonna do.
1. If you wish to use Git or other source control repository, now is the time to add the solution to source control. Use whatever process you normally use


## Create an angular application with angular cli

If you didn�t already install the angular cli tool, you need to do so now. Follow the guide from this link.

Before you run to fast, just do the installation of angular cli for now. Get back here when you are ready to create a new angular app.

![Angular CLI](https://cli.angular.io/)

Now you have the angular cli tool as part of your development environment. 

Open a command prompt, and navigate the the root of the Deploy project folder. ( de ..whatever.folder is your root ) 

````C:\Projects\MyAngularSolution\Deploy''''

```cmd
ng new demo
```

