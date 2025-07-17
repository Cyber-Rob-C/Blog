---
title: "Mastering kubectl: The 6 Commands I Use Most in My Home Lab"
datePublished: Thu Jul 17 2025 17:25:29 GMT+0000 (Coordinated Universal Time)
cuid: cmd7nv6o7000s02k0bjwvfp7g
slug: mastering-kubectl-6-essential-commands
tags: kubernetes-devops-kubectl-homelab-beginners

---

When I first started learning Kubernetes, `kubectl` felt like a foreign language.

There were so many commands, flags, and cryptic outputs that it was easy to get overwhelmed.

But here’s the truth: **you don’t need to know every** `kubectl` command to start building confidence.

In this post, I’ll share the 6 commands I use the most in my home lab — the ones that helped me stop guessing and start understanding what's happening in my cluster.

---

## 📌 Foundational Commands

These help me quickly understand the current state of the cluster.

### ✅ `kubectl cluster-info`

Displays the endpoints of the control plane components.  
Helpful for confirming the cluster is up and reachable.

---

### ✅ `kubectl get nodes`

Lists the worker and master nodes with their status.  
I use this to confirm nodes are Ready and not cordoned or tainted unexpectedly.

---

### ✅ `kubectl get all`

A quick way to view **everything** in the current namespace — pods, services, deployments, replicasets, etc.

This is my go-to command when I just deployed something and want a cluster-wide view.

---

## 🛠️ Troubleshooting Essentials

These commands are life-savers when pods misbehave.

### ✅ `kubectl describe pod <name>`

Outputs detailed pod information including events, volume mounts, and probes.  
I use this to investigate things like failed scheduling or readiness issues.

---

### ✅ `kubectl logs <pod-name>`

Shows logs from a specific pod.  
If your pod has multiple containers, don’t forget to add `-c <container-name>`.

I often pair this with `kubectl get pods` to find the pod name first.

---

### ✅ `kubectl get events --sort-by=.metadata.creationTimestamp`

Chronologically displays events happening across the namespace.  
Helpful for diagnosing permission issues, restarts, or node-related errors that don't show up in logs.

---

## 💡 Pro Tips

• Use the `-n <namespace>` flag to focus on a specific environment.  
• Set up command aliases in your terminal (`alias k=kubectl`, `alias kgp='kubectl get pods'`).  
• Use `kubectl explain <resource>` to understand unfamiliar fields or resource types.

---

## 🔁 Practice Builds Confidence

I didn’t memorize these.  
I *used* them — again and again — in my home lab until they stuck.

If you’re starting out with Kubernetes, focus on using just a few commands often.  
The clarity you gain will unlock the rest.

---

Have a favorite `kubectl` trick I should try in my lab?  
[Let me know on LinkedIn](https://www.linkedin.com/feed/update/urn:li:activity:7351313431565598721/) — I’d love to hear what helped *you* level up.

---

*Thanks for reading. If you're learning DevOps one command at a time like I am, consider following the blog for more hands-on posts like this.*