---
title: Install Docker on Ubuntu
created: 2026-10-17
updated: 2026-10-17
tags:
  - how-to
  - Docker
  - Ubuntu
environment: Ubuntu 24.04
software_version: Docker 27.x
---

# Install Docker on Ubuntu

## Purpose

Cài Docker để chạy container cho các dự án local.
## Requirements

- Ubuntu 24.04
- Quyền sudo
## Steps

1.  Cập nhật apt:
```bash
sudo apt update
```
2. Cài Docker:
```bash
sudo apt install docker.io -y
```
3. Thêm user vào group docker:
```bash
sudo usermod -aG docker $USER
newgrp docker
```
4. Kiểm tra:
```bash
docker --version
docker run hello-world
```
## Troubleshooting

- **Permission denied:** chưa logout/login sau khi thêm group docker.
- **Cannot connect to daemon:** kiểm tra `sudo systemctl status docker`.
## Notes

- Không chạy Docker bằng `sudo` nếu không cần.
- Trên WSL2 cần bật systemd.
## References

- [https://docs.docker.com/engine/install/ubuntu/](https://docs.docker.com/engine/install/ubuntu/)
- [[install-docker-windows-wsl2]]
- [[docker-cheatsheet]]