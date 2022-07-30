# Sapir Cloud DevOps - Final Lab

# `Analiza Chat App`

## Introduction

If you're building and deploying cloud native applications and microservices, then understanding container development and orchestration is a must have skill.

In this Lab you'll learn how to use both `Docker` and `Docker Compose` to build and run containers.

In this Lab scenario you'll work with 3 containers:

* `React` (front-end)
* `Express` (Back-end)
* `Mongodb` (Database)
![image](https://user-images.githubusercontent.com/30344406/181800731-23acc432-e764-49cf-be0c-49d6d025f82e.png)

This Lab will teach you how to use use Docker Compose, a tool for defining and running multi-container Docker applications, to configure and launch the Full Stack (front-end , Back-end , db) environment.
![image](https://user-images.githubusercontent.com/30344406/181816851-d7dee2d7-8fca-4249-99cf-39450a1cacb7.png)
### Upon completion of this Lab, you will be able to:

* Use a **Dockerfile** to create a web application
* Use a **Docker Compose** file to create a multi-container setup
* Use the **docker compose** command to launch a multi-container setup
* Test and validate the container setup using the **cur**l command




## Step 1️⃣: `Login to AWS Management Console`

Firstly , login to aws console using the following credentials:

| Account ID | 777203705741 |
| ---------- | ------------ |
| Username   | analiza      |
| Password   | Analiza2022$ |

## Step 2️⃣: `Create an EC2 Instance`

Use EC2 to create a new instance with the following properties:

| Instance Name: | sapir-<your_firstname>-<your_last_name> | Example: sapir-fadi-iraqi |
| ---------- | ------------ | ------------ |
| AMI:   |  ami-02292f97f5e004ea6 | AnalizaOS - Customized Ubuntu 22.04 with `Docker` & `Docker Compose` |
| Type:  | t2.micro | |
| Region:   | N.Virginia | |
| Storage:   | 15 GB | |

Then , Connect to the instance within `EC2 Instance Connect`:

![image](https://user-images.githubusercontent.com/30344406/181844662-0567ac18-5f77-4f2d-a527-5f1ecdb4259d.png)

## Step 3️⃣: `clone the repo`

Clone the repo to your server using `git clone` , then navigate into the folder

## Step 4️⃣: `Deploy the multi-service app using Docker Compose` :

`Docker Compose` is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration. To learn more about all the features of Compose, see the list of features.

Compose works in all environments: production, staging, development, testing, as well as CI workflows.

Using Compose is basically a three-step process:

1. Define your app’s environment with a Dockerfile so it can be reproduced anywhere. (☑️ Ready)

2. Define the services that make up your app in docker-compose.yml so they can be run together in an isolated environment. (☑️ Ready)

3. Run `docker compose up` and the Docker compose command starts and runs your entire app:

```sh
docker compose up -d
```

## Step 5️⃣: `Tesing and validating` :

List images:

```sh
docker images
```
List services:

```sh
docker ps
```

Ckeck you react app resposne using curl http request:

```sh
curl http://localhost:3000
```

Add `Security Group` inbound rule , to enable external traffic:

![Screenshot 2022-07-30 085619](https://user-images.githubusercontent.com/30344406/181876941-81d964af-c920-40e1-8d40-05372d55825f.png)

Open the app on the browser , and check if your app working properly:

![image](https://user-images.githubusercontent.com/30344406/181877162-9c1dc4b2-18b6-4d75-8b6a-1a1ce6295b05.png)


## Step 6️⃣: `submission` :
 
* Create a Diagram (using draw.io) describes the tolpology (front-end, backend ,db) you have after the deployment emphasizing port numbers for every service , use official aws & docker icons like:

![Untitled Diagram drawio](https://user-images.githubusercontent.com/30344406/181876127-4653ddb0-11e1-42e8-813e-641cb29f9446.png)
* Export your diagram as svg file and submit it on `Leemood`

* After finishing all of the steps `Stop` youe instance **(be worry! , don't terminate it)** . after your submission we will check your setup


## 📧 For Contact:

email: `fadi@analiza-college.co.il`

discord: `Fadi#5225`


# Good luck!
