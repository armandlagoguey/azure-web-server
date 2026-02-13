# Web Server Installation

## 1. Installing Nginx
\`\`\`bash
sudo apt update
sudo apt -y install nginx
\`\`\`

---

## 2. Enabling and starting the service
\`\`\`bash
sudo systemctl start nginx
sudo systemctl enable nginx
\`\`\`

Service status verified using:

\`\`\`bash
sudo systemctl status nginx
\`\`\`

---

## 3. Local service verification
\`\`\`bash
curl -I http://localhost
\`\`\`

Expected output:

\`\`\`
200 OK -> Working
\`\`\`

---

## 4. Replacing the default web page with a custom index.html
\`\`\`bash
echo "<h1>Azure Web Server demo</h1><p>by Armand Lagoguey</p>" > /var/www/html/index.html
\`\`\`

---

## Screenshots
- ../screenshots/customindex.png

