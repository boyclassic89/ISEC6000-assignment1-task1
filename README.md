# ISEC6000-devops-project

## Overview
This README contains thorough instructions for setting up the initial infrastructure required for our ISEC6000 Secure DevOps project. In job 1, a Kubernetes cluster must be created on Google Kubernetes Engine (GKE), 'kubectl' must be configured for cluster management, and a private GitHub repository must be created to house project files and code.

## Prerequisites
- A valid Google Cloud Console account.
- A GitHub account

# Task 1 is divided into 3 parts which are stated below:

## Step 1:
### a. Log into your Google cloud console
- Visit the [Google Cloud Console](https://console.cloud.google.com/) and log in to your Google account

### b. Navigate to Kubernetes Engine and Create a new cluster
- In the Google Cloud Console, navigate to the "Kubernetes Engine" section using the left-hand sidebar.
- Click the "Create Cluster" button to initiate the cluster creation process.

### c. Configure cluster settings
  - Cluster name: "assignment1-cluster"
  - Location: Regional
  - Region: us-central1
  - Node: usp-central1-a

### d. Kubernetes version: 1.27.3-gke.100
    we can use the "gcloud container clusters describe assignment1-cluster --format="value(currentNodeVersion)" --zone=us-central1" to get the kubernetes version.

### e. Click on create to finish up creating your desired cluster.

## Step 2:
### Authenticate kubectl with GKE cluster
- In the Google Cloud Console, navigate to "Kubernetes Engine" > "Clusters."
- Locate your newly created cluster in the list and click on it.
- Click the "Connect" button located at the top of the cluster details page.
- Use Use "gcloud container clusters get-credentials assignment1-cluster --region us-central1 --project green-jet-398409" command to authenticate kubectl with GKE 
  cluster.

## Step 3:
### Creating and configuring a Private GitHub Repository
- Log in to your git account.
- Click on create repository.
- Here's the details of how repository has been created:
  - Name:"ISEC6000-devops-project"
  - Visibility: Public
  - Description: ISEC6000 Assignment Repository
  - Readme: You are already here
-Now pushing all these into git, use the following commands:
    -git init
    -git add .
    -git commit -m "Initial push"
    -git remote add origin https://github.com/boyclassic89/ISEC6000-devops-project
    -git push -u origin master








