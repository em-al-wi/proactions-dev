# ProActions Development Environment

This repository provides a setup for training participants to edit and test their ProActions configuration files locally. Participants can use their preferred text editor (e.g., Visual Studio Code) to edit the configuration and load it into the browser via a local HTTP server.

## 📋 Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [🚀 Getting Started](#getting-started)
  - [1. Clone or Download Repository](#1-clone-or-download-the-repository)
  - [2. Install Dependencies](#2-install-dependencies)
  - [3. Start Local HTTP Server](#3-start-the-local-http-server)
  - [4. Edit Configuration File](#4-edit-your-configuration-file)
  - [5. Test Configuration](#5-test-the-configuration-in-your-browser)
- [⚠️ Troubleshooting](#troubleshooting)
- [📚 Additional Resources](#additional-resources)

## Overview

ProActions is a tool that allows you to define automated workflows and processes through YAML configuration files. This development environment helps you create, edit, and test these configuration files in a local setting before deploying them to your production environment.

## Prerequisites

- **Node.js** (version 14 or higher)
- A text editor, such as **Visual Studio Code** (recommended extensions: YAML, Better YAML Syntax, YAML Validator)
- A modern web browser (Chrome or Firefox recommended for best compatibility)
- Operating systems: Windows, macOS, or Linux are all supported

---

## Getting Started

### 1. Clone or Download the Repository

You can either clone this repository or download it as a ZIP file:

#### Clone via Git:
```bash
git clone https://github.com/em-al-wi/proactions-dev.git
cd proactions-dev
```

#### Download ZIP:
1. Click on the green **Code** button at the top of this page.
2. Select **Download ZIP**.
3. Extract the ZIP file to a folder of your choice.
4. Open a terminal and navigate to the extracted folder.

---

### 2. Install Dependencies

Run the following command in your terminal to install all required dependencies:

```bash
npm install
```

---

### 3. Start the Local HTTP Server

The repository includes an npm script to start a local HTTP server that serves your configuration files. Use one of the following methods:

#### Method 1: Using npm (Recommended)
Run this command in your terminal:
```bash
npm run start
```

#### Method 2: Using the Batch File (Windows Only)
For Windows users, a batch file (`start-dev-server.bat`) is provided for convenience:
1. Double-click on `start-dev-server.bat`.
2. The server will start automatically.

---

### 4. Edit Your Configuration File

1. Navigate to the `public/SysConfig` directory.
2. Create a new file named `pro-actions.ai-kit.yaml`.
3. Use the template provided in the same directory (`pro-actions.ai-kit.yaml.template`) as a starting point.

---

### 5. Test the Configuration in Your Browser

1. Open your browser and navigate to:
   ```
   http://localhost:8083/SysConfig/pro-actions.ai-kit.yaml
   ```
2. The configuration file will be loaded and can be used by your application.

**What success looks like:** When your configuration loads correctly, you'll see the raw YAML content in your browser or, if testing with the application, your ProActions should execute according to your configuration without errors.

---

## Troubleshooting

### Common Issues

- **Server Not Starting**:
  - Ensure Node.js is installed and that you have run `npm install` before starting the server.
  - Check if port 8083 is already in use by another application.

- **CORS Errors**:
  - If you encounter CORS issues, ensure that the HTTP server is running with CORS enabled (this is already configured in this setup).
  - Error message typically contains: "Access-Control-Allow-Origin"

- **File Not Found**:
  - Ensure `pro-actions.ai-kit.yaml` exists in the `/public/SysConfig` directory of this repository.
  - Error message typically contains: "404 Not Found"

- **YAML Parsing Errors**:
  - Check for proper indentation (YAML is sensitive to spaces)
  - Verify all quotes are properly closed
  - Use a YAML validator extension in VS Code to identify syntax issues

### Validation

To validate your YAML configuration:
1. Use the YAML Validator extension in VS Code
2. Or paste your configuration at [YAML Validator Online](https://jsonformatter.org/yaml-validator)

---

## Additional Resources

- [Official ProActions Documentation](https://confluence.eidosmedia.com/display/TEM/Swing+ProActions+Configuration)
- [ProActions Step Library](https://confluence.eidosmedia.com/display/TEM/Swing+ProActions+AI-Kit+Library)
- [YAML Tutorial](https://yaml.org/spec/1.2.2/)
- [VS Code YAML Extension](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)

---

## Additional Notes

- Changes made to `pro-actions.ai-kit.yaml` will be immediately available when reloading the browser or the Swing editor.
- This setup is designed for training purposes only and should not be used in production environments.
