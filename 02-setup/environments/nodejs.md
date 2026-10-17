---
title: "Node.js Setup"
created: 2026-10-17
updated: 2026-10-17
tags: [setup, nodejs]
project: ""
environment: "Windows 11"
---
# Setup: Node.js
## Overview
Cài Node.js + npm để phát triển frontend và backend JS.
## Prerequisites
- Windows 11
- Quyền admin
## Installation
1. Tải Node.js LTS từ https://nodejs.org
2. Cài đặt, chọn "Add to PATH"
3. Kiểm tra:
```bash
node -v
npm -v
```

## Configuration

- Đổi npm registry nếu cần: `npm config set registry https://registry.npmjs.org/`
- Cài pnpm: `npm install -g pnpm`
## Verification

```bash
node -v    # v22.x
npm -v     # 10.x
```
## Common Issues

- **'node' is not recognized:** chưa thêm vào PATH, cài lại và chọn "Add to PATH".
    

## Related Notes

- [[python]]
    
- [[vscode-setup]]