## Issue Encountered

The API VM was deployed with:

- No Public IP
- No NAT Gateway

Result:

- Azure Bastion connectivity worked successfully.
- DNS resolution worked.
- Outbound Internet connectivity was unavailable.

Lesson Learned:

Private Azure VMs may require an explicit outbound connectivity solution such as a NAT Gateway or Azure Firewall.
