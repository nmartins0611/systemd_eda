
Event Driven automation Concept - 

Using Systemd Path Units to monitor for file/folder changes on the FS

The playbook : create_systemd.yml creates the path and service units for systemd on the desired node. This uses the path.j2 and service.j2 templates. 

Roles:

compliance_check: Basic sample playbook to check desired states of services - Example http firewalld running etc...

job_counter: Checks the host's Job summury via API call to count the number of remediations that have triggerd on the host, this guides the automation to further remediation.

raise_ticket: Sample playbook to log tickets on ServiceNow as a remediation step based on a count of the job_counter

rescue_accounts: This is a playbook to restore the default passwd/shadow files - and used in the example of a file watcher to /etc/passwd. 

Playbook:

rescue_accounts.yml: This is the main playbook which is triggered in a Callback from the service path on systemd. This is done with Callback provisioning on Ansible Controller. 

