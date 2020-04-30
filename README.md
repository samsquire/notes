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

./gradlew build -Dhttp.socketTimeout=60000 -Dhttp.connectionTimeout=60000

Docker GUI
```
sudo docker run --net=host --env="DISPLAY" --volume="$HOME/.Xauthority:/root/.Xauthority:rw" gui-app
```

# Creating a vagrant box

```
useradd -m vagrant
sudo -u vagrant bash
mkdir ~/.ssh/
cat <<EOF > /home/vagrant/.ssh/authorized_keys
ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEA6NF8iallvQVp22WDkTkyrtvp9eWW6A8YVr+kz4TjGYe7gHzIw+niNltGEFHzD8+v1I2YJ6oXevct1YeS0o9HZyN1Q9qgCgzUFtdOKLv6IedplqoPkcmF0aYet2PkEDo3MlTBckFXPITAMzF8dJSIFo9D8HfdOV0IAdx4O7PtixWKn5y2hMNG0zQPyUecp4pzC6kivAIhyfHilFR61RGL+GPXQ2MWZWFYbAGjyiYJnAmCP3NOTd0jMZEnDkbUvxhMmBYSdETk1rRgm+R4LOzFUGaHqHDLKLX+FIPKcF96hrucXzcWyLbIbEgE98OHlnVYCzRdK8jlqm8tehUc9c9WhQ== vagrant insecure public key
EOF
```
