# Nginx + Apache + MySQL + PHP for CentOS7.3

## Dockerコンテナのプロビジョニング

```
ansible-playbook -i hosts/docker docker.yml
```

Check Mode (Dry Run)

```
ansible-playbook --check -i hosts/docker docker.yml
```

特定のHOST・タスクを実行

```
ansible-playbook -i hosts/docker -l ansible-namp-centos7 --step docker.yml
ansible-playbook -i hosts/docker -l ansible-namp-centos7 --start-at='httpd start' --step docker.yml
```

タグ指定でタスクを実行

```
ansible-playbook -i hosts/docker -l ansible-namp-centos7 --tags 'php70' docker.yml
```