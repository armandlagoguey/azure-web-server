The objective of this hardening was to reduce the attack surface and have secure access controls.

1. SSH-key only authentication
  The SSH key pair was created during the VM deployment
  The private key is stored securely on my PC

2. Disabling PasswordAuthentication
   The SSH configuration file (/etc/ssh/sshd_config) was updated to change "PasswordAuthentication" from "yes" to "no"
   The SSH service was restarted to apply the change.

3. UFW Firewall Rules
   Rules Applied:Allow OpenSSH Allow, Nginx HTTP, Deny all other inbound traffic

4. Azure NSG Restrictions
  Inbound Rules: Allow SSH (22) from a single trusted IP address (mine), Allow HTTP (80) from any source, Deny for all other inbound traffic
