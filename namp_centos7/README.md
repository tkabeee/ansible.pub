# Nginx + Apache + MySQL + PHP for CentOS7.3

## Dockerコンテナのプロビジョニング

```
ansible-playbook -i hosts/docker docker.yml
```

Check Mode (Dry Run)

```
ansible-playbook --check -i hosts/docker docker.yml
```
