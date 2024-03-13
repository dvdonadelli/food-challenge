# Food Challenge

- trigger action

## Prerequisites

Ensure you have the following installed on your local machine:

- Docker
- Java JDK

## Setting Up Your Local Environment

1. **Clone the repository:**
    First, clone the `food-challenge` repository to your local machine. You can do this by running the following command in your terminal:

    ```bash
    git clone git@github.com:dvdonadelli/food-challenge.git
    ```

    Navigate to the project directory:

    ```bash
    cd food-challenge
    ```

2. **Configure and run k8s:**
    In order to run the application locally, a few steps need to be performed:
   
   1. **Install minikube:** First, go to https://minikube.sigs.k8s.io/docs/start/ and install it according to your OS.
   2. **Start Cluster:** After correctly install run minikube to start a new k8s cluster, using the following command.
      ```bash
       minikube start
       ```
   3. **Start database:** With the cluster correctly running, start the DB pods using:
       ```bash
       kubectl apply -f ./k8s/db
       ```
   4. **Start the application:** Then, you will need to start the application by running:
       ```bash
       kubectl apply -f ./k8s/app
       ```
   5. **Expose Pods:** Since Minikube does not expose automatically the services ips, you will need to run:
      ```bash
       minikube tunnel
      ```
That's it! Your local development environment is set up, and you should be able to test our application.

## Swagger or Postman

To get a better view of the API endpoint, you can access the swagger endpoint in the following path:

    localhost:8080/swagger-ui/index.html

_or_

Use our postman collection to populate the database and perform some tests. To do that, follow the next steps:

1. **Postman collection:** First, you will need to download the following collection:


[<img src="https://run.pstmn.io/button.svg" alt="Run In Postman" style="width: 128px; height: 32px;">](https://app.getpostman.com/run-collection/8557906-a98b0740-f272-48a8-8b2b-373d6440ae9c?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D8557906-a98b0740-f272-48a8-8b2b-373d6440ae9c%26entityType%3Dcollection%26workspaceId%3Da6351687-ea84-4d74-bbd6-491183b035ed)

2.  **Run folders:** After downloading the collection, first you will need to create the products. To do that, go to the PRODUCT folder and execute the `RUN FOLDER` command.
   ![image](./imgs/run_folder.png)


3. **Run requests:** Then, select all desired products and click on the `Run food-challenge` button.
   ![image](./imgs/run_food-challenge.png)
Repeat the same process for the customer folder, selection all desired requests.


4. **Start testing:** With these information, you can start testing by creating orders, changing the status of the order, listing all orders and more.
## K8s Architecture

![image](./imgs/k8s-architecture.png)

## Kubernetes Architecture Video
The complete explanation and other details can be seen [here](https://youtu.be/I7kEGNdaUYI)

## Software Structure
The architecture implemented in our software is the Clean Architecture. Below is a drawing representing this architecture:
![img.png](imgs/img.png)