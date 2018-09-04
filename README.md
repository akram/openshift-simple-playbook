# Simple OpenShift Installation

Install the required ansible-galaxy modules
```
ansible-galaxy install -r requirements.yaml

```


Get your IP address and your domain name and replace it in the following command lines:
```
sed s/@@ip/$IP/g hosts.yaml > /tmp/hosts.yaml
ansible-playbook -i /tmp/hosts.yaml install.yaml -e public_hostname=console.cloud-archi.com -e routing_suffix=apps.cloud-archi.com
```

