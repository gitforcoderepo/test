````markdown
# 🟦 Om-Tech  
# ☸️ KUBERNETES NOTES (Student Edition)

---

## 📌 Kubernetes
Kubernetes is an open-source container orchestration technology for automating deployment, scaling, and managing containerized applications. Kubernetes was originally developed by Google and is now maintained by the Cloud Native Computing Foundation (CNCF).

---

# 🏗 Kubernetes Architecture

## 🧠 1. Master (Control Plane)

### 🔹 1. API Server
- Main management point of the cluster  
- kubectl communicates with API Server  
- Connects all components  
- Responsibilities:
  - Authentication  
  - Authorization  
- Uses watch mechanism  
- Interacts with:
  - Scheduler  
  - Controller Manager  

---

### 🔹 2. etcd
- Distributed key-value store  
- Stores cluster configuration  
- Represents cluster state:
  - Nodes
  - Pods
  - Scheduling  

**Command:**
```bash
etcdctl snapshot save <backup-file>
````

---

### 🔹 3. Scheduler

* Watches unscheduled pods
* Assigns pods to nodes
* Based on:

  * Resource availability
  * Affinity rules
  * Constraints

---

### 🔹 4. Controller Manager

* Runs control loops
* Ensures:

```
Desired State = Actual State
```

**Examples:**

* Deployment
* ReplicaSet
* StatefulSet
* DaemonSet

---

## ⚙️ 2. Worker Node Components

### 🔹 Node

* Machine where pods run

---

### 🔹 1. Container Runtime

* Runs containers
* Examples:

  * Docker
  * CRI-O
  * rktlet

---

### 🔹 2. Kubelet

* Node agent
* Ensures containers run
* Talks to API Server

---

### 🔹 3. Kube-Proxy

* Network proxy
* Handles:

  * Service exposure
  * Traffic routing
  * Load balancing

---

### 🔹 4. Pod

* Smallest deployable unit
* Can have multiple containers

---

# 📄 Manifest File Structure

## 🔹 1. apiVersion

Defines API version

Examples:

* v1
* apps/v1

Commands:

```bash
kubectl api-versions
kubectl api-resources -o wide
```

---

## 🔹 2. kind

Defines resource type

Examples:

* Pod
* Deployment

---

## 🔹 3. metadata

Contains:

* name
* namespace
* labels

---

## 🔹 4. spec

Defines desired state:

* Image
* Replicas

---

## 🔹 5. Labels & Annotations

### Labels

```yaml
labels:
  app: demo-app
```

### Annotations

```yaml
annotations:
  created-by: jenkins-ci
```

---

## 🔹 6. Selectors

### Equality-based

* =
* ==
* !=

Example:

```
app = nginx
```

---

### Set-based

* in
* notin
* exists

Example:

```
environment in (production, qa)
```

---

# 🧾 Common Commands

```bash
kubectl get nodes
kubectl apply -f file.yaml
kubectl get pods
kubectl describe pod <name>
kubectl delete pod <name>
```

---

# 🔁 Controllers

## 🔹 ReplicaSet / ReplicationController

Ensures desired number of pods

### Difference:

* ReplicaSet → set-based
* ReplicationController → equality-based

---

## 🔹 Deployment

* Manages ReplicaSets
* Supports:

  * Rollout
  * Rollback

Commands:

```bash
kubectl rollout history deployment <name>
kubectl rollout undo deployment <name>
```

---

## 🔹 DaemonSet

Runs pod on all nodes

Use cases:

* Logging
* Monitoring

---

## 🔹 StatefulSet

### Features:

* Stable identity (pod-0, pod-1)
* Ordered deployment
* Ordered deletion

Used for:

* MySQL
* PostgreSQL

---

# 🔄 Pod Lifecycle

* **Pending** → Scheduling
* **Running** → Active
* **Succeeded** → Completed
* **Failed** → Error
* **Unknown** → Node issue

---

# ❤️ Probes

## Types:

* Readiness → Ready for traffic
* Liveness → Alive check
* Startup → Slow apps

---

## Handlers

### Exec

```yaml
exec:
  command: ["cat", "/file"]
```

### TCP

```yaml
tcpSocket:
  port: 8080
```

### HTTP

```yaml
httpGet:
  path: /health
```

---

# 🌐 Services

## 🔹 ClusterIP

* Internal communication

## 🔹 NodePort

* External via node IP

## 🔹 LoadBalancer

* Cloud load balancer

## 🔹 Headless

* No IP
* Direct pod access

---

# 📍 Scheduling

## 🔹 NodeSelector

```yaml
nodeSelector:
  disktype: ssd
```

---

## 🔹 Affinity

### Node Affinity

* Required (hard)
* Preferred (soft)

---

## 🔹 Pod Affinity

* Co-locate pods

## 🔹 Pod Anti-Affinity

* Avoid pods together

---

## 🔹 Taints & Tolerations

### Taint:

```
NoSchedule
```

### Toleration:

```yaml
tolerations:
- key: "key1"
  operator: "Exists"
```

---

# 💾 Volumes

## Types:

* Ephemeral
* Persistent

---

## 🔹 Persistent Volume (PV)

Storage resource

## 🔹 Persistent Volume Claim (PVC)

Requests storage

---

## Access Modes:

* RWO
* ROX
* RWX
* RWOP

---

## Reclaim Policies:

* Retain
* Delete
* Recycle

---

# 🗂 Namespace

Default namespaces:

* default
* kube-system
* kube-public
* kube-node-lease

---

# ⚙️ ConfigMap

Stores non-sensitive data

```yaml
data:
  DBURL: value
```

---

# 🔐 Secrets

Stores sensitive data

```yaml
data:
  PASSWORD: base64
```

---

## Secret vs ConfigMap

* Secret → encrypted
* ConfigMap → plain

---

# 📊 ResourceQuota

Limits namespace usage

---

# 🔒 Security

### Best Practices:

* Enable RBAC
* Use Network Policies
* Secure API Server
* Scan containers

---

# 🔐 RBAC

## Concepts:

* Subject
* Resource
* Verb

---

## Objects:

* Role
* ClusterRole
* RoleBinding
* ClusterRoleBinding

---

# 🤖 Service Account

* Non-human identity
* Used by pods

---

# 🔗 Context

Defines:

* Cluster
* User
* Namespace

Commands:

```bash
kubectl config get-contexts
kubectl config use-context <name>
```

---

# 📁 kubeconfig File

Contains:

* clusters
* users
* contexts

---

# 📌 END OF NOTES

```
```
