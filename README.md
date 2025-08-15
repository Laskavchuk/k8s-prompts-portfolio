# Kubernetes Prompt Portfolio

This repository contains prompt engineering examples for generating Kubernetes manifests.  
Each row includes the prompt, its description, and a link to the resulting YAML manifest.

| NAME                 | PROMPT                                                                                              | DESCRIPTION                                                                 | EXAMPLE                                     |
|----------------------|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------|
| app                  | "Generate a simple Kubernetes Deployment with one container running `go-demo-app` on port 8080."   | Basic application deployment                                                | [app.yaml](yaml/app.yaml)                   |
| app-livenessProbe    | "Add a livenessProbe to the Deployment that checks `/healthz` on port 8080 every 10 seconds."       | Deployment with liveness probe                                              | [app-livenessProbe.yaml](yaml/app-livenessProbe.yaml) |
| app-readinessProbe   | "Extend the Deployment with a readinessProbe checking `/ready` endpoint on port 8080."              | Deployment with readiness probe                                             | [app-readinessProbe.yaml](yaml/app-readinessProbe.yaml) |
| app-volumeMounts     | "Mount a ConfigMap volume named `app-config` at `/etc/config` inside the container."                | Deployment with volume and volumeMount                                      | [app-volumeMounts.yaml](yaml/app-volumeMounts.yaml)   |
| app-cronjob          | "Create a Kubernetes CronJob that runs `go-demo-app` every 5 minutes."                             | CronJob manifest                                                            | [app-cronjob.yaml](yaml/app-cronjob.yaml)   |
| app-job              | "Create a Kubernetes Job that runs a one-time batch process using `go-demo-app`."                   | Job manifest                                                                | [app-job.yaml](yaml/app-job.yaml)           |
| app-multicontainer   | "Generate a Pod with two containers: `go-demo-app` and a sidecar container `busybox`."              | Multi-container Pod                                                         | [app-multicontainer.yaml](yaml/app-multicontainer.yaml) |
| app-resources        | "Set CPU requests to 100m and memory requests to 128Mi with limits 200m/256Mi for the container."   | Resource requests and limits                                                | [app-resources.yaml](yaml/app-resources.yaml) |
| app-secret-env       | "Inject a secret named `db-secret` with key `DB_PASSWORD` into container environment variables."    | Using secrets in environment variables                                      | [app-secret-env.yaml](yaml/app-secret-env.yaml) |
