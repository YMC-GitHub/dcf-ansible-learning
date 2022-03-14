# dcf-ansible-learning

setup a ansible-learning envirenment in docker

## prepare

- docker
- docker-compose

## setup

```bash
# speed up git clone in china
GC_PROXY="https://ghproxy.com/"
GC_URL="https://github.com/YMC-GitHub/dcf-ansible-learning.git"
GC_URL="${GC_PROXY}${GC_URL}"
git clone -b main "$GC_URL"
```

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
