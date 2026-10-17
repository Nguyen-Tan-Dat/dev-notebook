---
title: "Node: Port already in use (EADDRINUSE)"
created: 2026-10-17
updated: 2026-10-17
tags: [experience, nodejs, troubleshooting]
---

# Node: Port already in use (EADDRINUSE)

## Symptom

Chạy `npm run dev` báo:
Error: listen EADDRINUSE: address already in use :::3000
## Cause
Port 3000 đang bị process khác chiếm.
## Solution
**Linux/macOS:**
```bash
lsof -i :3000
kill -9 <PID>
```

**Windows:**

```bash

netstat -ano | findstr :3000
taskkill /PID <PID> /F
```
Hoặc đổi port:
```bash
PORT=3001 npm run dev
```
## Lesson Learned

- Kiểm tra port trước khi chạy dev server.
- Ghi lại port mặc định của từng dự án trong `overview.md`.
## Related Notes

- [[nodejs]]
    
- [[project-a-overview]]