# WebServDash

**Frontend dashboard and CGI test scripts (PHP, Python, Bash) for the WebServer project.**

This repository serves as the **content layer** for the main C++ WebServer. It separates the server logic from the static assets and dynamic scripts used to verify HTTP compliance and CGI execution.

---

## 📂 Repository Contents

This repository is divided into two main components:

### 1. 📊 The Dashboard (Static Content)
A responsive web interface designed to test the server's ability to handle:
* **HTML/CSS/JS** serving.
* **Media files** (Images, Favicons).
* **Client-side logic** via JavaScript.
* **File Uploads** (POST requests).

### 2. ⚙️ CGI Test Suite (Dynamic Content)
A collection of scripts designed to stress-test the server's CGI implementation (Common Gateway Interface).
* **🐍 Python:** Scripts dealing with environment variables and infinite loops (timeout testing).
* **🐘 PHP:** Session management, cookies, and form processing.
* **🐚 Bash:** Simple shell script execution and system status reporting.

---

## 🚀 Integration

**Note:** This repository is designed to be a submodule or a cloned dependency of the main **WebServer** project.

### Automatic Installation (Recommended)
If you are running the main WebServer, this repository should be fetched automatically via the `Makefile` rule:

```bash
make
# or specifically
make repo

```

### Manual InstallationIf you need to download this repository standalone for inspection:

```bash
git clone git clone https://github.com/ABDE-LKADER/WebServDash.git

```

---

### 📁 Suggested Directory StructureWhen cloned into the main project, the structure usually looks like this:

```text
WebServer/               # Main C++ Project
├── src/                 # Server Source Code
├── conf/                # The Server Configuration 
├                               ...
├── Makefile
├                        # This Repository
├── www/                 # CSS, JS, Images
├── errors/              # Static Error Pages
└── bin/                 # Server-side scripts
    ├── script.py
    ├── script.php
    └── script.sh
```

---

### 🧪 Testing GuideOnce the server is running and this repo is linked:

1. **Dashboard:** Navigate to `http://localhost:PORT/` to view the UI.
2. **CGI Python:** Navigate to `http://localhost:PORT/bin/script.py` to test Python execution.
3. **CGI PHP:** Navigate to `http://localhost:PORT/bin/script.php` to test PHP parsing.
4. **Uploads:** Use the Dashboard form to upload a file and verify it appears in the `uploads/` directory.

---
