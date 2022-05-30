# event-compliance

 Systemd - put the accounts-mon.service and accounts-mon.path in /etc/systemd/system
 start the accounts-mon.service

accounts-rescue.sh = triggers callback provisioning back to controller to trigger a the accounts rescue playbook.

rescue accounts playbook just restores the correct version of passwd.

rescue accounts token playbook restores the passwd but also creates a file to increment the number of remediations controller has had to run - This is with the idea that after a certain threshold controller will log a service now ticket for human intervention and/or isolate the host on the network.


