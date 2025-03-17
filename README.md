<h1 align="center">
  <img src="./assets/bb-1.png" alt="BBLogo" width="250" /></br></br>
  <strong style="font-size:60px;">GCP Privilege Escalation Script</strong>
</h1></br>

# Description
Privilege Escalation Scanner for Google Cloud Projects
The scripts in this file are experamental scripts for scanning your project permissions to check against known privilege escalations. This script is a modified and improved script based on the rhino labs script. Changes I have made are improvements based on work I have done in my Google environments. 

# Usage
1. Enumerate permissions in the project
`python3 enumerate_member_permissions.py --project-id test-project-12345`
2. Scan the enumerated permissions for privilege escalation vulnerabilities
`python3 check_for_privesc.py`
3. Review the results
member_privileges.json – All members and their associated privileges
privilege_escalation_methods.md – All detected privilege escalation methods
setIamPolicy_methods.md – All detected setIamPolicy methods