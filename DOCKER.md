# Docker / Container Module Quick Reference

Template for each module entry

## Module: <module-name>
Short description: One-line summary.

Repo: https://github.com/owner/repo  
Original author/maintainer: name (email/handle)  
Status: Active / WIP / Archived / Deprecated  
Tags: docker, container, image, k8s  
Last updated: YYYY-MM-DD

Supported container environments
- Docker Engine: tested on Docker Engine 20.10+
- Kubernetes: tested on k8s v1.20+ (if applicable)
- Container runtimes: runc, containerd

Per-system prerequisites
- Docker CLI/Engine installed — `docker --version`
- docker-compose (optional) — `docker-compose --version`
- For Kubernetes: kubectl — `kubectl version --client`

Build / run (one-liners)
- Build image: `docker build -t myimage:latest .`
- Run container: `docker run --rm -p 8080:8080 myimage:latest`

Quick verification
- `docker ps` and `docker logs <container>`

Key files
- Dockerfile, docker-compose.yml, Kubernetes manifests (if present)

Known limitations
- e.g., "Requires privileged access for certain host capabilities"

Attribution
- Link to original repo
