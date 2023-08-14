# Explanation for Kubernetes Deployment

## Choice of Kubernetes Objects

In this project, I opted to use a combination of Kubernetes Deployment, Service, and PersistentVolumeClaim objects to deploy my application components. Deployments are suitable for stateless applications like the client and backend, providing ease of scaling and recovery. I chose not to use StatefulSets for my database (MongoDB) due to the nature of my application's requirements and the potential complexity of managing stateful workloads.

## Exposing Pods to Internet Traffic

To expose my application to internet traffic, I used a Kubernetes LoadBalancer Service for the frontend (client) application. This allows external users to access the application via the LoadBalancer's external IP address. For the backend API, I chose a ClusterIP Service to restrict access to within the cluster, as it does not need direct internet exposure.

## Use of Persistent Storage

I incorporated persistent storage for the MongoDB database using a PersistentVolumeClaim (PVC). This ensures that data stored in the database persists even if the pod is restarted or rescheduled. It enhances data reliability and availability, which is crucial for my application's data integrity.

## Successful Running of the Application

The application has been successfully deployed to Google Kubernetes Engine (GKE). The deployment manifests and configuration files have been included in the repository, allowing for easy replication of the environment. The application is accessible via the URLs provided in the repository's README file.

## Docker Image Tag Naming Standards

For Docker images, I followed a clear and consistent naming convention. Images were tagged with version numbers (e.g., v1.0.0) to indicate their release and provide a way to track and manage changes over time. Descriptive tags facilitate easy identification and differentiation of images.
