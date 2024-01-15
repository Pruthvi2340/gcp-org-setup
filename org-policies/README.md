# Access management policies

**1. Domain restricted contacts**
Prevents adding users to Essential Contacts outside your specified domains. This limits Essential Contacts to only allow managed user identities in your selected domains to receive platform notifications.

**2. Domain restricted sharing**
Prevents adding users to IAM policies outside your specified domains. This limits IAM policies to only allow managed user identities in your selected domains to access resources inside this organization.

**3. Public access prevention**
Prevents Cloud Storage buckets from being exposed to the public. This ensures that a developer can't configure Cloud Storage buckets to have unauthenticated internet access.

**4. Uniform bucket level access**
Prevents object-level access control lists (ACLs) in Cloud Storage buckets. This simplifies your access management by applying IAM policies consistently across all objects in Cloud Storage buckets.

**5. Require OS login**
VMs created in new projects will have OS Login enabled. This lets you manage SSH access to your instances using IAM without needing to create and manage individual SSH keys.

# Additional security policies for service accounts

**6. Disable automatic IAM grants**
Prevents the default App Engine and Compute Engine service accounts from automatically being granted the Editor IAM role on a project at creation. This ensures service accounts don't receive overly-permissive IAM roles upon creation.

**7. Disable service account key creation**
Prevents the creation of public service account keys. This helps reduce the risk of exposing persistent credentials.

**8. Disable service account key upload**
Prevents the uploading of public service account keys. This helps reduce the risk of leaked or reused key material.

# Secure VPC network configuration policies

**9. Define allowed external IPs for VM instances**
Prevents the creation of Compute instances with a public IP, which can expose them to internet traffic.

**10. Disable VM nested virtualization**
Prevents the creation of nested VMs on Compute Engine VMs. This decreases the security risk of having unmonitored nested VMs.

**11. Disable VM serial port**
Prevents serial port access to Compute Engine VMs. This prevents input to a server’s serial port using the Compute Engine API.

**12. Restrict authorized networks on Cloud SQL instances**
Prevents public or non-internal network ranges from accessing your Cloud SQL databases.

**13. Restrict Protocol Forwarding Based on type of IP Address**
Prevents VM protocol forwarding for external IP addresses.

**14. Restrict Public IP access on Cloud SQL instances**
Prevents the creation of Cloud SQL instances with a public IP, which can expose them to internet traffic.

**15. Restrict shared VPC project lien removal**
Prevents the accidental deletion of Shared VPC host projects.

**16. Sets the internal DNS setting for new projects to Zonal DNS Only**
Prevents the use of a legacy DNS setting that has reduced service availability.

**17. Skip default network creation**
Prevents automatic creation of the default VPC network and related resources. This avoids overly-permissive default firewall rules.

**18. Disable VPC External IPv6 usage**
Prevents the creation of external IPv6 subnets, which can be exposed to unauthorized internet access.
