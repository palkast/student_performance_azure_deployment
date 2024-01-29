## End to end ML project using Microsoft Azure Web Apps and MLOPS
This is a project to deploy end to end ml application using ci cd pipelines and github action using container registry and Azure web apps.
## Goal of this project
a)To demonstrate the use of docker to streamline deployment of ML models by containerizing the application and help developers in developing,shipping and running and deplying applications 
b)To show how to leverage the MLOPS tools to automate deployments in production environments.GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows one to automate build, test, and deployment pipeline. One can create workflows that build and test every pull request to our repository, or deploy merged pull requests to production.
c)To use Azure Web Apps for building and hosting application on Azure cloud.
## Process 
1.Create Container registry in Azure.
2.Docker set up in local repository and push docker image to Container registry
3.Create Azure Web apps with the container that stores the docker image
4.Configure Github deployment center
## Steps :
1.Created container registry in Container Registries in Azure portal.Store the access keys of the container by saving username and password to log in while pushing docker to this container registry.
[![Picture1.png](https://i.postimg.cc/Hn78qGbb/Picture1.png)](https://postimg.cc/sGs2WN62)
2.Build docker image ,push the docker image to Azure container registry ,also  visible on docker desktop.
# Run from terminal:
docker build -t testdockerkast.azurecr.io/application:latest .
docker login testdockerkast.azurecr.io
docker push testdockerkast.azurecr.io/application:latest
[![Picture2.png](https://i.postimg.cc/d3qrTNCC/Picture2.png)](https://postimg.cc/N9z534pG)
Docker App shows the docker is created.
[![Picture3.png](https://i.postimg.cc/XN8w03Mk/Picture3.png)](https://postimg.cc/0rz6pTyz)
# Create web app , the app is hosted on Azure web app server 
[![Picture4.png](https://i.postimg.cc/qR7ph8RR/Picture4.png)](https://postimg.cc/v1CJCx5F)
Container registry is used to store docker image.
[![Picture5.png](https://i.postimg.cc/zXh8gDJn/Picture5.png)](https://postimg.cc/Yht5cHL9)
[![Picture6.png](https://i.postimg.cc/g0gWWnDP/Picture6.png)](https://postimg.cc/mc1q3ZJd)
# Enable continuous deployment through github action .
Build and deploy step completed the deployment using GitHub actions. 
[![Picture8.png](https://i.postimg.cc/R07T6HYj/Picture8.png)](https://postimg.cc/TyPbBpf9)
[![Picture9.png](https://i.postimg.cc/j256Fkjb/Picture9.png)](https://postimg.cc/zbsRL7Wt)
Automatically any change to Github repository will trigger deployment through Github actions and then it wiil go to Azure .
[![Picture10.png](https://i.postimg.cc/VvptHfTq/Picture10.png)](https://postimg.cc/V095J8zv)
[![Picture12.png](https://i.postimg.cc/Kv0wjdTn/Picture12.png)](https://postimg.cc/D8bBYpBZ)
yml file is created in Github actions to generate the workflow of jobs run.
[![Picture12.png](https://i.postimg.cc/Kv0wjdTn/Picture12.png)](https://postimg.cc/D8bBYpBZ)
