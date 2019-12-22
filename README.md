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
