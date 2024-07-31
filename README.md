

echo "# kubu_python" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/lalithbarani/kubu_python.git
git push -u origin main


# Build the Docker image
       docker build -t your-dockerhub-username/hello-world-python:latest .

# Log in to Docker Hub (if you haven't already)
       docker login

# Push the Docker image
       docker push your-dockerhub-username/hello-world-python:latest


4. Create Kubernetes Deployment
Create a Kubernetes deployment YAML file to deploy your Docker image:

     hello-world-deployment.yaml

5. Apply Deployment in Kubernetes
Apply the deployment YAML file to your Kubernetes cluster:

     kubectl apply -f hello-world-deployment.yaml

6. Verify Deployment
Check the status of your deployment:

     kubectl get deployments
     kubectl get pods

7. Check Logs
To see the output of your Python application:

    kubectl logs <pod-name>

   

