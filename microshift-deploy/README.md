A collection of playbooks that I use to deploy my Microshift node as well as install my basic applications:

Start with the microshift-deploy.ansible.yaml playbook. After it is completed it will automatically go to the next playbook in the sequence.

Current Sequence: microshift-deploy -> kasten-deploy 

Applications:

Kasten - Application aware backup for Kubernetes. kasten.io

boxes.py - https://github.com/florianfesti/boxes
  - Build the Dockerfile first, then deploy.
