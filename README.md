<h1 align="center">
  <img src="./assets/bb-1.png" alt="BBLogo" width="250" /></br></br>
  <strong style="font-size:60px;">GCP Privilege Escalation Script</strong>
</h1></br>

# Description
Privilege Escalation Scanner for Google Cloud Projects
The scripts in this file are experamental scripts for scanning your project permissions to check against known privilege escalations. This script is a modified and improved script based on the rhino labs script. Changes I have made are improvements based on work I have done in my Google environments. 

# Usage
1. Enumerate permissions in the project
`python3 enumerate-permissions.py --project-id test-project-12345`
2. Scan the enumerated permissions for privilege escalation vulnerabilities
`python3 privilege-escalation-scanner.py`
3. Review the results
member-privileges.md – All members and their associated privileges
privilege-escalation-methods.md – All detected privilege escalation methods
setIamPolicy-methods.md – All detected setIamPolicy methods

# Current Privilege Escalation Methods
cloudbuilds.builds.create
deploymentmanager.deployments.create
iam.roles.update
iam.serviceAccounts.getAccessToken
iam.serviceAccountKeys.create
iam.serviceAccounts.implicitDelegation
iam.serviceAccounts.signBlob
iam.serviceAccounts.signJwt
cloudfunctions.functions.create
cloudfunctions.functions.update
compute.instances.create
run.services.create
cloudscheduler.jobs.create
orgpolicy.policy.set
storage.hmacKeys.create
serviceusage.apiKeys.create
serviceusage.apiKeys.list