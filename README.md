# placeholder - will be overwritten if you re-run the earlier generation step


## CI/CD (GitHub Container Registry)
This repo includes a GitHub Actions workflow that builds multi-arch images and pushes to **GHCR**.

**Setup:**
1. Create a new GitHub repo and push this folder to it.
2. Go to *Settings → Actions → General* → enable workflows for the repo (if needed).
3. Push to `main` — the action will build and publish:
   - `ghcr.io/<your-org-or-user>/weather-stack:latest`
   - `ghcr.io/<your-org-or-user>/weather-stack:<git sha>`

To use **Docker Hub** instead, create repo secrets:
- `DOCKERHUB_USERNAME`
- `DOCKERHUB_TOKEN` (create a personal access token on Docker Hub)
Then uncomment the Docker Hub steps in `.github/workflows/docker-image.yml`.
