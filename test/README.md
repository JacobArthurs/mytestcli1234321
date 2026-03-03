# Testing

## Linux (Docker)

Requires Docker with QEMU support. First time only:

```bash
docker run --rm --privileged multiarch/qemu-user-static --reset -p yes
```

Run each architecture separately:

```bash
docker compose -f docker-compose.amd64.yml up --pull always --force-recreate
docker compose -f docker-compose.arm64.yml up --pull always --force-recreate
```

## Darwin (GitHub Actions)

Go to GitHub → Actions → **Test Darwin** → Run workflow.

Tests darwin/arm64 natively and darwin/amd64 via Rosetta, npm and PyPI separately.

## Windows (native)

```powershell
npm install -g <package>
<binary> --version

pip install <package>
<binary> --version
```
