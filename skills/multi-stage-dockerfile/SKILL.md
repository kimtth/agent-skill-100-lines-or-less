---
name: multi-stage-dockerfile
description: "Use when: create or review optimized multi-stage Dockerfiles for smaller, safer, reproducible application images."
---

Goal: produce a Dockerfile with separate build and runtime concerns.

Use for:
- new Dockerfiles
- reducing image size
- removing build tools or secrets from runtime images
- improving layer cache and reproducibility

Workflow:
1. Detect language, package manager, build command, test command, and runtime port.
2. Use a builder stage for dependencies, compilation, and tests.
3. Use a runtime stage with only required artifacts and runtime deps.
4. Pin base image versions and keep layers cache-friendly.
5. Add `.dockerignore`, non-root user, and healthcheck when appropriate.
6. Build and smoke test the image.

Best practices:
- name stages with `AS builder`, `AS runtime`, etc.
- copy lockfiles before source for dependency caching
- avoid secrets in `ARG`, `ENV`, layers, or final image
- use minimal official or distroless images when compatible

Rules:
- do not use `latest` tags for reproducible builds
- do not run as root unless required
- do not copy the whole build context blindly
- verify the runtime image starts
