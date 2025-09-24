# Helm and Kubernetes Core Concepts

## What is Helm?

Helm is a **package manager for Kubernetes** (similar to apt for Ubuntu or yum for CentOS).  
It helps you define, install, and manage Kubernetes applications.

- Applications in Kubernetes often need multiple YAML files (Deployments, Services, Ingress, ConfigMaps, Secrets, etc.).
- Managing these YAMLs manually is tedious and error-prone.
- Helm solves this by packaging all Kubernetes resources into a **Helm Chart**.

### Why Helm is Useful?
1. **Simplifies Deployment**  
   - Package all manifests into a single reusable chart.
   - Easy installation: `helm install myapp ./mychart`.

2. **Version Control**  
   - Roll back to a previous release easily.
   - Manage multiple versions of the same app.

3. **Templating**  
   - Use variables instead of hardcoding values.
   - Example: Environment-specific configs (dev, staging, prod).

4. **Reusability**  
   - Share charts across teams or use prebuilt charts from [Artifact Hub](https://artifacthub.io/).

---

## Kubernetes Core Concepts (Health Checks and More)

### 1. Liveness Probe
- **Purpose**: Checks if the container is still running.  
- If it fails, Kubernetes **restarts the container**.  
- Example: Detects when an app is stuck in a deadlock.

```yaml
livenessProbe:
  httpGet:
    path: /healthz
    port: 8080
  initialDelaySeconds: 5
  periodSeconds: 10
```

---

### 2. Readiness Probe
- **Purpose**: Checks if the container is **ready to serve traffic**.  
- If it fails, Kubernetes **removes the pod from the Service load balancer**.  
- Example: During startup when app needs time to initialize.

```yaml
readinessProbe:
  httpGet:
    path: /ready
    port: 8080
  initialDelaySeconds: 10
  periodSeconds: 5
```

---

### 3. Startup Probe
- **Purpose**: For apps that take a long time to start.  
- Kubernetes uses this probe to decide when to start checking **liveness** and **readiness**.  
- Example: Legacy Java apps with long bootstrap times.

```yaml
startupProbe:
  httpGet:
    path: /startup
    port: 8080
  failureThreshold: 30
  periodSeconds: 10
```

---

## Summary

- **Helm**: A package manager for Kubernetes that simplifies application deployment, management, and rollback.
- **Liveness Probe**: Restarts unhealthy containers.
- **Readiness Probe**: Ensures only healthy pods receive traffic.
- **Startup Probe**: Handles slow-starting applications.

These concepts together ensure your application is **resilient, reliable, and easy to manage** in Kubernetes.
---
