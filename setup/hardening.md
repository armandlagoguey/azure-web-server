<h1>OS Hardening</h1>

<p>The objective of this hardening was to reduce the attack surface and have secure access controls.</p>

<hr>

<h2>SSH‑key only authentication</h2>
<ul>
  <li>The SSH key pair was created during the VM deployment</li>
  <li>The private key is stored securely on my PC</li>
</ul>

<hr>

<h2>Disabling PasswordAuthentication</h2>
<p>The SSH configuration file (<code>/etc/ssh/sshd_config</code>) was updated to change:</p>

<pre><code>PasswordAuthentication yes
</code></pre>

<p>to:</p>

<pre><code>PasswordAuthentication no
</code></pre>

<p>The SSH service was restarted to apply the change.</p>

<hr>

<h2>UFW Firewall Rules</h2>
<p><strong>Rules Applied:</strong></p>
<ul>
  <li>Allow OpenSSH</li>
  <li>Allow Nginx HTTP</li>
  <li>Deny all other inbound traffic</li>
</ul>

<p><strong>Screenshot:</strong></p>
<p>
  <img src="../screenshots/ufwconfig.png" alt="UFW configuration screenshot">
</p>

<hr>

<h2>Azure NSG Restrictions</h2>
<p><strong>Inbound Rules:</strong></p>
<ul>
  <li>Allow SSH (22) from a single trusted IP address (mine)</li>
  <li>Allow HTTP (80) from any source</li>
  <li>Deny all other inbound traffic</li>
</ul>
