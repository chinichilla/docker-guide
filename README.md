
#### What is Docker?


#### What is Kubernetes? (quoted from [Deploying to Kubernetes](https://docs.docker.com/get-started/part3/))
* All containers in Kubernetes are scheduled as pods, which are groups of co-located containers that share some resources.
* For the most part, workloads are scheduled as deployments, scalable groups of pods maintained automatically by Kubernetes. 
* Kubernetes objects are described in manifests called Kubernetes YAML files

#### What is Swarm?

### Using the Tools

#### [Setting up Docker, Kubernetes, and Swarm](https://docs.docker.com/get-started/part1/)
1. Install docker using [Mac](https://docs.docker.com/docker-for-mac/install/) or [Windows](https://docs.docker.com/docker-for-windows/install/) link. 
2. Enable Kubernetes and test that a yaml file works.
3. Initialize swarm with similar commands.

#### [Docker: Build and Test Image](https://docs.docker.com/get-started/part2/)

0. git clone repo and `npm install`. 
1. Inside the directory, build the image using: `docker image build -t [image-name] .`. The message `Successfully tagged [image-name]` should appear. 
2. Start the container based on the new image: `docker container run --publish 8000:8080 --detach --name [alias-in-yaml] [image-name]`.

**Helpful Docker Commands for Troubleshooting:** `docker ps`(or `docker container ls`?), `docker stop [container-id]`, `docker start [container-id]`, `docker rm [container-id]`

#### [Kubernetes: Deploy and Check the Application](https://docs.docker.com/get-started/part3/)

1. Create a `[alias-in-yaml].yaml` file. (Note: )
2. Login to docker: `docker login`. (?)
3. Navigate to the root of the repo, and deploy the application to Kubernetes: `kubectl apply -f [alias-in-yaml].yaml`. (Note: Click this sections link to see desired output.)
4. Check the listed deployments using `kubectl get deployments` and the services using `kubectl get services`.
5. Visit the application in the browser at [http://localhost:30001/](http://localhost:30001/).

**Helpful Kubernetes Commands for Troubleshooting:** `kubectl describe pod [pod-name]`, docker container rm --force [pod-name], kubectl delete -f [alias-in-yaml].yaml





