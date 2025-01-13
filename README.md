# Angular Helm Chart

This Helm chart is designed to deploy an Angular application on a Kubernetes cluster. It provides configurations for Deployment, Service, and Ingress resources.

## Chart Details

- **Name**: `angular-chart`
- **Version**: `1.0.0`
- **App Version**: `1.0.0`

## Prerequisites

- Kubernetes cluster
- Helm
- NGINX Ingress Controller installed in the cluster

## Files Overview

- **`deployment.yaml`**: Manages the Deployment configuration.
- **`service.yml`**: Configures the Service for the frontend.
- **`ingress.yml`**: Sets up Ingress for routing traffic to the application.
- **`chart.yaml`**: Defines metadata for the Helm chart.
- **`values.yml`**: Allows customizable configurations.

## Usage

1. Clone the repository or copy the chart to your local setup.
2. Update the `values.yml` file with your specific configurations:
   - Namespace
   - Image name and tag
   - Target and service ports
   - Ingress host and annotations
3. Deploy the chart using Helm:
   ```bash
   helm install <release-name> chart-directory -n <namespace>

## Accessing the Application
Once deployed, the application will be accessible via the specified Ingress host. Ensure the DNS is correctly pointed to the LoadBalancer IP of the NGINX Ingress Controller.
   
