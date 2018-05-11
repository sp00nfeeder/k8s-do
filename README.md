

# k8s-do

This uses kubespray to deploy to a set of DigitalOcean nodes: 

```
git clone https://github.com/sp00nfeeder/k8s-do
git submodule init;  git submodule update

# deploy DigitalOcean nodes and set DNSMadeEasy DNS records
terraform apply

ansible-playbook -i ./inventory/hosts ./prep.yml

# deploy k8s via kubespray
ansible-playbook -i ./inventory/hosts ./kubespray/cluster.yml
```

