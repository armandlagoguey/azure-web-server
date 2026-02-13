1. Installing Nginx
   sudo apt update
   sudo apt -y install nginx

2. Enabling and starting the service
   sudo systemctl start nginx
   sudo systemctl enable nginx
   Service status verified using:
   sudo systemctl status nginx

3. Local service verification
   curl -I http://localhost
   200 OK -> Working

4. Replacing the default web page with a custom index.html
   echo "<h1>Azure Web Server demo</h1><p>by Armand Lagoguey</p>" > /var/www/html/index.html
