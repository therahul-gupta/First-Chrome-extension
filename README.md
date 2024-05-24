
# How to Create a Chrome Extension

Welcome to the "How to Create a Chrome Extension" guide! This repository will help you get started with developing your own Chrome extension. Follow the steps below to create a basic but functional Chrome extension.

## Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Project Structure](#project-structure)
4. [Step-by-Step Guide](#step-by-step-guide)
   - [1. Set Up Your Project](#1-set-up-your-project)
   - [2. Create the Manifest File](#2-create-the-manifest-file)
   - [3. Create the Popup HTML File](#3-create-the-popup-html-file)
   - [4. Create the JavaScript File](#4-create-the-javascript-file)
   - [5. Add Icons](#5-add-icons)
   - [6. Load Your Extension in Chrome](#6-load-your-extension-in-chrome)
   - [7. Test Your Extension](#7-test-your-extension)
5. [Additional Resources](#additional-resources)
6. [Contributing](#contributing)
7. [License](#license)

## Introduction

This guide walks you through the process of creating a simple Chrome extension. You'll learn how to set up your development environment, write the necessary code, and test your extension in the Chrome browser.

## Prerequisites

Before you start, make sure you have the following:

- Basic knowledge of HTML, CSS, and JavaScript
- A code editor (e.g., VS Code, Sublime Text)
- Google Chrome browser installed

## Project Structure

Your project directory should look like this:

```
my-chrome-extension/
│
├── manifest.json
├── popup.html
├── popup.js
├── icon16.png
├── icon48.png
└── icon128.png
```

## Step-by-Step Guide

### 1. Set Up Your Project

Create a new directory for your Chrome extension:

```bash
mkdir my-chrome-extension
cd my-chrome-extension
```

### 2. Create the Manifest File

The `manifest.json` file contains metadata about your extension. Create a `manifest.json` file in your project directory with the following content:

```json
{
  "manifest_version": 3,
  "name": "My Chrome Extension",
  "version": "1.0",
  "description": "A basic example Chrome extension.",
  "action": {
    "default_popup": "popup.html",
    "default_icon": {
      "16": "icon16.png",
      "48": "icon48.png",
      "128": "icon128.png"
    }
  },
  "permissions": [
    "storage",
    "activeTab"
  ]
}
```

### 3. Create the Popup HTML File

Create a `popup.html` file with the following content:

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Chrome Extension</title>
  <style>
    body { font-family: Arial, sans-serif; }
    #content { padding: 20px; }
  </style>
</head>
<body>
  <div id="content">
    <h1>Hello, world!</h1>
    <button id="myButton">Click me</button>
  </div>
  <script src="popup.js"></script>
</body>
</html>
```

### 4. Create the JavaScript File

Create a `popup.js` file with the following content:

```javascript
document.getElementById('myButton').addEventListener('click', () => {
  alert('Button clicked!');
});
```

### 5. Add Icons

Add icons for your extension in the following sizes: 16x16, 48x48, and 128x128 pixels. Name them `icon16.png`, `icon48.png`, and `icon128.png` respectively, and place them in the project directory.

### 6. Load Your Extension in Chrome

1. Open Chrome and navigate to `chrome://extensions/`.
2. Enable "Developer mode" using the toggle switch in the top right.
3. Click "Load unpacked" and select your extension's root directory.

### 7. Test Your Extension

Your extension should now be loaded in Chrome. Click on the extension icon in the toolbar to open the popup and test the functionality.

## Additional Resources

- [Chrome Extension Documentation](https://developer.chrome.com/docs/extensions/mv3/getstarted/)
- [Chrome Extensions Samples](https://github.com/GoogleChrome/chrome-extensions-samples)
- [MDN Web Docs: Getting started with Chrome Extensions](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue.
