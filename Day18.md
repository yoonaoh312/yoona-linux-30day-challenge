
# Day 18: Create a Local Web Server – Install NGINX and Serve a Static Page

## 🗓️ Date
2025-08-18

## ✅ Goal
Set up a local web server using NGINX and serve a static HTML page.

## 🗂️ Key Commands and Their Purpose
| Command / Syntax                                   | Description                                      |
|---------------------------------------------------|-------------------------------------------------|
| `sudo apt update && sudo apt install nginx -y`    | Install NGINX web server                        |
| `sudo systemctl start nginx`                      | Start NGINX service                             |
| `sudo systemctl enable nginx`                     | Enable NGINX to start on boot                   |
| `sudo systemctl status nginx`                     | Check NGINX service status                      |
| `sudo ufw allow 'Nginx HTTP'`                     | Allow HTTP traffic through firewall             |
| `sudo nano /var/www/html/index.html`              | Create or edit a static HTML page               |
| `sudo chown -R $USER:$USER /var/www/html/`       | Set proper ownership for HTML files             |
| `curl http://localhost`                           | Test that NGINX serves the page locally         |
| `chmod +x script.sh`                              | Make a script executable                        |
| `./script.sh`                                     | Run a script                                    |

## 🔍 What I Did Today
- Installed NGINX on the local machine.
- Started the NGINX service and enabled it to run on boot.
- Configured firewall to allow HTTP traffic.
- Created a simple static HTML page in /var/www/html.
- Verified the page loads correctly using a browser and curl.

#!/bin/bash

# Install NGINX
sudo apt update && sudo apt install nginx -y

# Start and enable NGINX
sudo systemctl start nginx
sudo systemctl enable nginx

# Allow HTTP traffic through firewall
sudo ufw allow 'Nginx HTTP'

# Create a sample static page
sudo tee /var/www/html/index.html > /dev/null <<EOL
<!DOCTYPE html>
<html>
<head>
    <title>My Local Web Server</title>
</head>
<body>
    <h1>Welcome to NGINX!</h1>
    <p>This is a static page served locally.</p>
</body>
</html>
EOL

# Set ownership
sudo chown -R $USER:$USER /var/www/html

# Test the page
curl http://localhost

## 🧠 Notes
- NGINX is lightweight and easy to set up for static websites.
- ufw allow 'Nginx HTTP' ensures the page is accessible from the network.
- Always check service status with systemctl status nginx.
- Ownership and permissions of /var/www/html matter for editing pages.