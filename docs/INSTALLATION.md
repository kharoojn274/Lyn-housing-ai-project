# 📖 Full Installation Guide A to Z

This guide will help you set up this project on Windows, macOS, or Linux from zero for local testing.

---

## 📋 Table of Contents

1. [🔧 Prerequisites](#-prerequisites)
2. [🖥️ Specific Setup for WIN/MAC/LINUX users](#-platform-specific-setup)
   - [🪟 Windows](#-windows)
   - [🍎 macOS](#-macos)
   - [🐧 Linux](#-linux)
3. [🚀 Useful Information](#-useful-information)

---

## 🔧 Prerequisites

| Software   | Purpose                      |
| ---------- | ---------------------------- |
| 🐍 Python  | Backend programming language |
| 📦 Node.js | Frontend runtime environment |
| 🔧 Git     | Version control system       |

---

## 🖥️ Platform-Specific Setup

<details>
<summary><strong>🪟 Windows</strong></summary>

[//]: # "###_-_-_-_-_-_-_WINDOWS-INSTALLATIONS_-_-_-_-_-_-_###"
[//]: # "###_-_-_-_-_-_-_WINDOWS-INSTALLATIONS_-_-_-_-_-_-_###"
[//]: # "###_-_-_-_-_-_-_WINDOWS-INSTALLATIONS_-_-_-_-_-_-_###"
[//]: # "###_-_-_-_-_-_-_WINDOWS-INSTALLATIONS_-_-_-_-_-_-_###"
[//]: # "###_-_-_-_-_-_-_WINDOWS-INSTALLATIONS_-_-_-_-_-_-_###"
[//]: # "###_-_-_-_-_-_-_WINDOWS-INSTALLATIONS_-_-_-_-_-_-_###"

### 1️⃣ Install Prerequisites

- **Python**: Download from [python.org](https://python.org) > Check “Add to PATH”
- **Node.js**: Download LTS from [nodejs.org](https://nodejs.org)
- **Git**: Download from [git-scm.com](https://git-scm.com)

```cmd
python --version
node --version
git --version
```

### 2️⃣ Project Setup

```cmd
cd C:\Users\%USERNAME%\Desktop

git clone https://github.com/kharoojn274/Lyn-housing-ai-project.git
cd lyn-housing-ai-app

# Backend
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend (new CMD window)
cd ..\frontend\lynapp-react
npm install
npm run dev
```

</details>

<details>
<summary><strong>🍎 macOS</strong></summary>

[//]: # "###.-.-.-.-.-.-.-.MAC-INSTALLATIONS.-.-.-.-.-.-.-.###"
[//]: # "###.-.-.-.-.-.-.-.MAC-INSTALLATIONS.-.-.-.-.-.-.-.###"
[//]: # "###.-.-.-.-.-.-.-.MAC-INSTALLATIONS.-.-.-.-.-.-.-.###"
[//]: # "###.-.-.-.-.-.-.-.MAC-INSTALLATIONS.-.-.-.-.-.-.-.###"
[//]: # "###.-.-.-.-.-.-.-.MAC-INSTALLATIONS.-.-.-.-.-.-.-.###"
[//]: # "###.-.-.-.-.-.-.-.MAC-INSTALLATIONS.-.-.-.-.-.-.-.###"

### 1️⃣ Install Prerequisites

#### Option A. Homebrew (Recommended)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install python node git
```

#### Option B. Manual

- Python: [python.org](https://python.org)
- Node.js: [nodejs.org](https://nodejs.org)
- Git: `xcode-select --install`

```bash
python3 --version
node --version
git --version
```

### 2️⃣ Project Setup

```bash
cd ~/Desktop

git clone https://github.com/kharoojn274/Lyn-housing-ai-project.git
cd lyn-housing-ai-app

# Backend
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend (new tab)
cd frontend/lynapp-react
npm install
npm run dev
```

</details>

<details>
<summary><strong>🐧 Linux</strong></summary>

[//]: # "###==============LINUX-INSTALLATIONS==============###"
[//]: # "###==============LINUX-INSTALLATIONS==============###"
[//]: # "###==============LINUX-INSTALLATIONS==============###"
[//]: # "###==============LINUX-INSTALLATIONS==============###"
[//]: # "###==============LINUX-INSTALLATIONS==============###"
[//]: # "###==============LINUX-INSTALLATIONS==============###"

### 1️⃣ Install Prerequisites

##### Ubuntu / Debian

```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv nodejs npm git
```

##### CentOS / Fedora

```bash
sudo yum install python3 python3-pip nodejs npm git   # CentOS/RHEL
sudo dnf install python3 python3-pip nodejs npm git   # Fedora
```

##### Arch

```bash
sudo pacman -S python python-pip nodejs npm git
```

### 2️⃣ Project Setup

```bash
cd ~/Desktop

git clone
cd lyn-housing-ai-app

# Backend
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend
cd frontend/lynapp-react
npm install
npm run dev
```

</details>

---

## 🚀 Useful Information

**a. Quick Check:** Run the following to verify installations whenever you need (use at the folder where the installations took place):

```bash
python3 --version    # or python --version
node --version
npm --version
git --version
```

**b. Start Server:** You can run Backend server anytime with commands once setup is done:

- Backend (Django)
  ```bash
  cd backend
  source venv/bin/activate  # Windows: venv\Scripts\activate
  python manage.py runserver
  # http://127.0.0.1:8000
  ```

or Frontend server with

- Frontend (React)
  ```bash
  cd frontend/lynapp-react
  npm run dev
  # http://localhost:5173
  ```

**c. Common URLs:**

| Component     | URL                        | Expected Result      |
| ------------- | -------------------------- | -------------------- |
| Backend API   | http://127.0.0.1:8000      | Django welcome page  |
| Frontend App  | http://localhost:5173      | React application    |
| API Endpoints | http://127.0.0.1:8000/api/ | API docs / JSON data |

**Stop Servers**: `Ctrl + C` in each terminal

**Deactivate venv**: `deactivate`

---
