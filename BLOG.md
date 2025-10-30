Dockerizing My First App — Step-by-Step Guide
Task 2 of #40DaysOfKubernetes Challenge

In today’s Task 2, we will learn how to Dockerize an application from GitHub and run it as a container using a Dockerfile.

The repository we will use is the Docker Official Getting Started App, which has been uploaded to my own GitHub repository.

👉 GitHub Repo Link: https://github.com/GGWPEZGAMER/my-getting-started-app

### Step-by-Step Process ###
### Step 1 --- Clone the Application

git clone https://github.com/docker/getting-started-app.git
-------------------------------------------------------------------------------------------------------------
### Step 2 --- Push to my own github repository ###

cd getting-started-app
git remote remove origin
git remote add origin https://github.com/GGWPEZGAMER/getting-started-app.git
git branch -M main
git push -u origin main
------------------------------------------------------------------------------------------------------------
### Step 3 --- Build Docker Image ###

docker build -t getting-started-app .
-------------------------------------------------------------------------------------------------------------
### Step 4 --- Run the Container ###

docker run -d -p 3000:3000 getting-started-app

(note: after running the containner , u can be access the webpage with http://localhost:3000)
--------------------------------------------------------------------------------------------------------------
### Step 5 --- Explore docker init ###

docker init
-------------------------------------------------------------------------------------------------------------
<iframe width="560" height="315" src="https://www.youtube.com/watch?v=nfRsPiRGx74"
title="YouTube video" frameborder="0" allowfullscreen></iframe>
