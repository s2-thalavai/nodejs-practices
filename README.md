# nodejs-practices

## What is Node.js?

Node.js is a **JavaScript runtime environment** built on Chrome's V8 engine. 
It enables developers to run JavaScript outside the browser—primarily for backend services, APIs, and real-time applications.

### Key Features
- **Event-driven, non-blocking I/O** for high concurrency
- **Cross-platform**: Windows, macOS, Linux
- **npm ecosystem**: Thousands of reusable packages
- **Ideal for**: Microservices, REST APIs, CLI tools, streaming apps

---

## Installation Steps

### Windows

1. **Download Installer**  
   Visit [https://nodejs.org/en/download](https://nodejs.org/en/download) and download the **LTS version** (.msi).

2. **Run Installer**  
   - Accept license agreement  
   - Choose installation path  
   - Optionally install additional tools (e.g., Chocolatey, Python)

3. **Verify Installation**
   ```bash
   node -v
   npm -v

    Optionally install tools for native modules
    
    Verify Installation Open Command Prompt and run:

      node -v
      npm -v

### Linux (Debian/Ubuntu)

1. **Update System** 
    
        sudo apt update && sudo apt upgrade -y
   
3. **Install Node.js and npm**
    
        sudo apt install nodejs npm -y

3. **Verify Installation**
   
        node -v
        npm -v


## Use NVM (Node Version Manager)

Recommended for managing multiple Node.js versions.

### Install NVM

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

### Install Node.js via NVM

    nvm install --lts
    nvm use --lts

### Node.js Post-Installation Checklist

After installing Node.js (via installer, package manager, or NVM), use the following checklist to verify your setup and initialize a basic project.

| Task                  | Command           | Expected Output           |
|-----------------------|-------------------|----------------------------|
| Verify Node.js version | `node -v`         | e.g., `v18.17.1`           |
| Verify npm version     | `npm -v`          | e.g., `9.6.7`              |
| Create test project    | `npm init -y`     | Generates `package.json`   |
| Run sample script      | `node index.js`   | Executes JS file           |

> Tip: To test your setup, create a simple `index.js` file:
> ```javascript
> console.log("Node.js is working!");
> ```

---

For multi-version management, consider using [NVM](https://github.com/nvm-sh/nvm) to switch between Node.js versions easily.

### Node.js Version Switchers

Managing multiple versions of Node.js is essential for testing, compatibility, and project isolation. Below are the most widely used tools for switching Node.js versions across platforms.

---

1. Platform: Windows, macOS, Linux Usage:
   
         nvs add lts
         nvs use lts
         nvs link lts

2. Install (Linux/macOS):

         export NVS_HOME="$HOME/.nvs"
         git clone https://github.com/jasongin/nvs "$NVS_HOME"
         . "$NVS_HOME/nvs.sh"
   
## Node.js Version Switcher Comparison

Managing multiple Node.js versions is essential for testing, compatibility, and project isolation. Below is a comparison of popular version switchers across platforms.

| Tool         | Platforms      | Highlights                          | Best For                    |
|--------------|----------------|--------------------------------------|-----------------------------|
| **NVM**       | macOS, Linux   | Simple CLI, widely adopted           | Unix-like systems           |
| **nvm-windows** | Windows       | GUI installer, NVM-compatible        | Windows users               |
| **NVS**       | All            | Fork support, CI-friendly            | Advanced version control    |
| **Volta**     | All            | Project-level pinning, fast          | Teams with per-project needs |

---

## Notes

- **NVM** is ideal for developers working in Linux or macOS environments who need quick version switching.
- **nvm-windows** brings similar functionality to Windows with a user-friendly installer.
- **NVS** supports switching between Node.js forks and is well-suited for CI/CD pipelines.
- **Volta** automatically pins versions per project and integrates well with team workflows.

> 🔗 For installation guides and usage examples, refer to:
> - [NVM](https://github.com/nvm)


