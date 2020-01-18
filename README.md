# lunalu
Ansible playbook to quickly bootstrap a complete frontend cache server on Ubuntu 19.10

## contains

- nginx
- varnish
- prometheus node_exporter
- prometheus varnish_exporter
- sane UFW defaults, limiting access to exporters

## deploy

```bash
ansible-playbook -i hosts site.yml \ 
--private-key ~/.ssh/key \
--extra-vars="ssl_certificate=cert.pem ssl_private_key=key.pem ssl_dh_param=dhparams.pem"
```