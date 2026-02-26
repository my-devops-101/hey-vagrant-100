# Vagrant by HashiCorp

|本期版本| 上期版本
|:---:|:---:
`Fri Oct 18 10:57:43 CST 2024` | `Sun Jul 21 11:43:32 CST 2024`

## Install

### macOS

```bash
brew tap hashicorp/tap
brew install hashicorp/tap/hashicorp-vagrant
```


## SSH Settings

> `~/.vagrant.d/insecure_private_key`

```ruby
config.ssh.insert_key = false
config.ssh.forward_x11 = true
```



## Network

```ruby
config.vm.network "public_network", bridge: "eno2", ip: "192.168.100.32"
```



## Provisioning

> `cloud-init`: <https://github.com/hashicorp/vagrant/issues/5571#issuecomment-120430700>

```bash
config.vm.provision "shell", inline: "sleep 60"
```

```bash
config.vm.provision "ansible" do |ansible|
	ansible.playbook = 'playbook.yml'
end
```

```bash
config.vm.provision "shell", inline: <<-SHELL
    export DEBIAN_FRONTEND=noninteractive
    sed -i 's@http://.*\.ubuntu\.com@https://mirrors.tuna.tsinghua.edu.cn@g' /etc/apt/sources.list
		
    apt-get update
    apt-get install -y build-essential
    apt-get install -y net-tools
  SHELL
```


## Ref

* <https://www.vagrantup.com/>
* [Vagrant Cookbook - Second Edition](https://leanpub.com/vagrantcookbook) 、[Vagrant Cookbook - First Edition](https://1lib.us/book/2610987/b56779?id=2610987&secret=b56779&dsource=recommend)
* [熟练使用vagrant](https://www.junmajinlong.com/virtual/index/#vagrant)
* <https://raw.githubusercontent.com/mitchellh/vagrant/master/keys/vagrant.pub>
* <https://documentation.ubuntu.com/public-images/public-images-explanation/vagrant/>