# notes

```
ss -lntp | grep 10250
```

```
ALL            ALL = (ALL) NOPASSWD: ALL
```

```
  config.vm.define "web" do |web|
    web.vm.box = "apache"
  end
```

ansible_default_ipv4.address

config.vm.network "forwarded_port", guest: 443, host: 443

https://askubuntu.com/questions/170348/how-to-create-a-local-apt-repository

```
https://www.nginx.com/resources/wiki/start/topics/examples/likeapache/
```

Download all my github repositories

```
curl -s https://api.github.com/users/samsquire/repos?page=2 | jq -r ".[].ssh_url" | xargs -L1 git clone
```
