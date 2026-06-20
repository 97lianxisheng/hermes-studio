---
title: Hermes Studio
emoji: 🤖
colorFrom: blue
colorTo: purple
sdk: docker
app_port: 7860
pinned: false
---

# Hermes Studio

Self-hosted AI chat dashboard for Hermes Agent — multi-model web UI with multi-platform integration.

This Space pulls a pre-built image from GitHub Container Registry (GHCR), published by GitHub Actions. The container listens on port **7860** (set by Hugging Face via the `PORT` environment variable).

**Important:** The GHCR package must be **public** so Hugging Face can pull it. After the first workflow run, open your GitHub profile → **Packages** → select the package → **Package settings** → **Change visibility** → **Public**.

## Configuration

Add secrets in the Space **Settings → Repository secrets** or **Variables** as needed, for example:

| Variable | Description |
|---|---|
| `AUTH_TOKEN` | Optional fixed bearer token (auto-generated on first run if unset) |
| `CORS_ORIGINS` | Optional CORS allowlist; default allows same host only |

Model API keys and Hermes profiles are configured inside the Web UI after first launch.

## Auth token

On first start, an auth token is printed in the container logs. Open **Logs** in this Space to find it, then append `?token=YOUR_TOKEN` to the Space URL.
