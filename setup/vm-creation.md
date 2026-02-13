The goal here was to create a lightweight VM to host a simple web server for training purposes.

Region:
I chose Norway East because it was in the list of allowed regions for the Azure Student subscription, and it offered the size options I wanted.

Size:
Standard B2als v2
2 vCPUs
4 GiB RAM
Cost efficient (about 35$ a month) and powerful enough for my purpose here

Authentication:
The VM uses SSH key‑based authentication.
Authentication type: SSH public key
Key format: RSA
A new key pair was generated during deployment
The private key was securely stored locally

Networking:
Public IP address to allow HTTP and SSH access
Network Security Group (NSG) with the following inbound rules:
  Allow SSH (22) from a trusted IP only (mine)
  Allow HTTP (80) from anywhere
  Deny all other inbound traffic
