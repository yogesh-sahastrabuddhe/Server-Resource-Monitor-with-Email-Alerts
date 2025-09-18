# Server-Resource-Monitor-with-Email-Alerts

> This Python script monitors your server's CPU and memory usage at regular intervals and sends email alerts when usage exceeds defined thresholds. It also logs all activities and alerts for review.

![License](https://img.shields.io/badge/license-Unlicense-green) ![Version](https://img.shields.io/badge/version-1.0.0-blue) ![Language](https://img.shields.io/badge/language-Python-yellow) ![GitHub](https://img.shields.io/badge/GitHub-yogesh-sahastrabuddhe/Server-Resource-Monitor-with-Email-Alerts/tree/main-black?logo=github) ![Build Status](https://img.shields.io/github/actions/workflow/status/yogesh-sahastrabuddhe/Server-Resource-Monitor-with-Email-Alerts/tree/main/ci.yml?branch=main)

## 📋 Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Prerequisites](#custom-1758209867853)
- [Code overview](#custom-1758209968930)
- [Troubleshooting](#custom-1758212863207)

## ℹ️ Project Information

- **👤 Author:** yogesh-sahastrabuddhe
- **📦 Version:** 1.0.0
- **📄 License:** Unlicense
- **📂 Repository:** [https://github.com/yogesh-sahastrabuddhe/Server-Resource-Monitor-with-Email-Alerts/tree/main](https://github.com/yogesh-sahastrabuddhe/Server-Resource-Monitor-with-Email-Alerts/tree/main)
- **🏷️ Keywords:** automation, python, Server monitoring, Resource monitoring, CPU usage, Memory usage, psutil, Email alerts, SMTP

## Features


- Monitors CPU and Memory usage using `psutil`
- Configurable thresholds for CPU and Memory utilization
- Sends email alerts via SMTP (supports Gmail)
- Logs monitoring activity and email alerts to a log file
- Runs continuously, checking resources every 5 minutes (configurable)


## Installation


1. Clone this repository or download the script file.

2. Install the required Python package:    pip install psutil

3.  Update the email and monitoring configuration in the script or via environment variables: EMAIL_FROM = "your_email@gmail.com"
EMAIL_TO = "recipient_email@example.com"
EMAIL_PASSWORD = "your_app_password"





## Usage

Run the script with:  python server_monitor.py



## Prerequisites


- Python 3.x installed on your machine
- Access to an SMTP email server (e.g., Gmail)
- `psutil` Python package installed

## Code overview


- `send_email(subject, body)`: Sends an email alert with the provided subject and body.
- `check_system_resources()`: Checks current CPU and memory usage and triggers email alerts if thresholds are exceeded.
- The main loop runs `check_system_resources()` every configured interval (`CHECK_INTERVAL`).


## Troubleshooting


- Ensure your Python environment has `psutil` installed.
- Verify SMTP server settings and credentials are correct.
- Check that your network allows outbound connections to the SMTP server.
- If email sending fails, review error messages in the log file `server_monitor.log`.
- Make sure to use app-specific passwords if using Gmail or similar services.
- For issues with logging or script not running continuously, confirm the script is executed in a persistent terminal or use a process manager.


