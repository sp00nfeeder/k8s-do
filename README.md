

# k8s-do




This uses kubespray to deploy to a set of DigitalOcean nodes. There are 2 parts to this:

* deploy DigitalOcean nodes and set DNSMadeEasy DNS records
* deploy k8s via kubespray

```
terraform apply
ansible-playbook -i ./inventory/hosts ./prep.yml
ansible-playbook -i ./inventory/hosts ./kubespray/cluster.yml
```

