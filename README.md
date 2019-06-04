# Hackathon

1. Source your RC file
2. Update `overrides.yml`
3. run `ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook playbook.yml -e @overrides.yml`
4. ...
5. Profit!

# How it works...

These playbooks will deploy 1x pf9-express "deployer" VM and 3x compute VMs at the
https://lab.cs.pf9.io endpoint. Using overrides, the playbooks will run pf9-express
on the "deployer" VM against the 3 compute VMs and attach them to the specified DU

# Issues

The lab servers are a bit long in the tooth, and the 900 second timeout for convergence
causes the playbooks to fail. However, the machines will continue to converge.


