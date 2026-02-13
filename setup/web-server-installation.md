<h1>Web Server Installation</h1>

<h2>1. Installing Nginx</h2>
<pre><code>sudo apt update
sudo apt -y install nginx
</code></pre>

<hr>

<h2>2. Enabling and starting the service</h2>
<pre><code>sudo systemctl start nginx
sudo systemctl enable nginx
</code></pre>

<p>Service status verified using:</p>

<pre><code>sudo systemctl status nginx
</code></pre>

<hr>

<h2>3. Local service verification</h2>
<pre><code>curl -I http://localhost
</code></pre>

<p>Expected output:</p>

<pre><code>200 OK -> Working
</code></pre>

<hr>

<h2>4. Replacing the default web page with a custom index.html</h2>
<pre><code>echo "&lt;h1&gt;Azure Web Server demo&lt;/h1&gt;&lt;p&gt;by Armand Lagoguey&lt;/p&gt;" &gt; /var/www/html/index.html
</code></pre>

<hr>

<h2>Screenshot</h2>
![Custom index page](../screenshots/customindex.png)
