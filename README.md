This project is an orchestration of a web survey application using Kubernetes. It uses Kubernetes to manage containerized applications in a scalable and automatic way. Traefik is used as a reverse proxy and load balancer.
Application components

    Poll: A Flask Python web application to collect votes and send them to a Redis queue.
    Redis: A Redis queue to store votes waiting to be processed by the Worker.
    Worker: A Java application to consume votes from the Redis queue and store them in a PostgreSQL database.
    PostgreSQL: A database to persistently store votes.
    Result: A Node.js web application to display the results.

**Environment requirements**

    You need at least 1 Kubernetes master and 2 nodes (workers).
    Although you can run the project locally, we strongly recommend using a "Kubernetes as a Service" platform, such as Amazon EKS, Google GKE or Digital Ocean.
    Installing a complete Kubernetes cluster locally is complex. Minikube is not suitable for multi-node clusters, which is required for this project.
