# 🐳 Docker 이미지 빌드 가이드

OpenWebUI 기반 프론트를 Docker 환경에서 실행하는 과정을 운영체제별로 정리했습니다.

---

## 📦 사전 준비 공통 사항

| 항목 | 설명 |
| --- | --- |
| 프로젝트 루트 | `submodules/8dobibim` `->` `open-webui` 로 이동 |
| 주요 파일 | `Dockerfile`, `.dockerignore`, `nginx/default.conf` |
| 결과 포트 | 기본적으로 `localhost:3000` (포트는 자유 설정 가능) |

---

## 🪟 Windows

### 📥 1. Docker Desktop 설치

- 공식 설치 페이지: https://www.docker.com/products/docker-desktop/
- WSL2 백엔드 권장 (설치 시 자동 안내됨)
- 설치 후 Docker 실행 여부 확인
```powershell
docker --version
```

### ⚙️ 2. 프로젝트 디렉토리 이동 (Git Bash 또는 PowerShell)

```bash
cd path/to/8dobibim_front
```

### 🧱 3. Docker 이미지 빌드

```bash
docker build -t 8dobibim-front 
```

### ▶️ 4. 실행

```bash
docker run -d -p 3000:80 --name 8dobibim-front 8dobibim-front
```

### 🖥️ 5. 접속

```
http://localhost:3000
```

---

## 🍎 macOS

### 📥 1. Docker Desktop 설치

- 공식 설치 페이지: https://www.docker.com/products/docker-desktop/
- 설치 후 `Terminal`에서 확인: docker --version

### ⚙️ 2. 터미널에서 실행

```bash
cd /path/to/8dobibim_front
docker build -t 8dobibim-front .
docker run -d -p 3000:80 --name 8dobibim-front 8dobibim-front
```

> macOS는 localhost:3000 바로 접속 가능 (Chrome/Safari 등)


---

## 🐧 Ubuntu / Linux

### 📥 1. Docker & Docker Compose 설치
```bash
sudo apt update
sudo apt install docker.io docker-compose -y
```
추가로 Docker 권한 없이 실행하려면:
```bash
sudo usermod -aG docker $USER
newgrp docker
```

### ⚙️ 2. 프로젝트 디렉토리로 이동
```bash
cd ~/projects/8dobibim_front
```

### 🧱 3. Docker 이미지 빌드
```bash
docker build -t 8dobibim-front .
```

### ▶️ 4. 실행
```bash
docker run -d -p 3000:80 --name 8dobibim-front 8dobibim-front
```

### 🖥️ 5. 접속
```bash
로컬 브라우저: http://localhost:3000
외부 접속 시: http://<서버 IP>:3000
```
