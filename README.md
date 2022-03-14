# dcf-ansible-learning

setup a ansible-learning envirenment in docker

## prepare

- docker
- docker-compose

## setup

## start

```bash
docker-compose up -d
docker-compose exec ansible sh
ssh-copy-id host1
ssh-copy-id host2
```

## usage
```bash
# ping
ansible dev -m ping
```

## Author

yemiancheng <ymc.github@gmail.com>

## License

MIT
