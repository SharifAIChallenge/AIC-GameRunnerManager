# AIC Game Runner Manager
DevOps tool to deploy [AIC-GameRunner](https://github.com/SharifAIChallenge/AIC-GameRunner)

## Deploy

copy and configure hosts template
```
cp hosts.sample.yml hosts.yml
```

Configure master node:
```
ansible-plabook master.yml
```

Push/Update images in registry on master node:
```
ansible-playbook update_images.yml
```

Configure worker nodes:
```
ansible-plabook worker.yml
```

Note: Don't configure same worker twice.

## Roles
`role` directory contains defined roles with game runner project dependencies.