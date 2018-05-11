

# k8s-do

This uses kubespray to deploy to a set of DigitalOcean nodes:

```
terraform apply
ansible-playbook -i ./inventory/hosts ./prep.yml
ansible-playbook -i ./inventory/hosts ./kubespray/cluster.yml
```

