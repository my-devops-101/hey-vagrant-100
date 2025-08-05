# Boxes

|本期版本| 上期版本
|:---:|:---:
`Sun Jul 21 11:43:14 CST 2024` | -

## Tools

> `macOS`

```bash
brew install curl jq
```

> `Ubuntu`

```bash
apt-get install -y curl jq
```

## Ubuntu

> `22.04 LTS x64`

```bash
vagrant box add ubuntu/jammy64
```

```bash
curl -fsSL https://app.vagrantup.com/ubuntu/boxes/jammy64 | jq '.versions[0].providers[0].url'
```

> `20.04 LTS x64`

```bash
vagrant box add ubuntu/focal64
```

```bash
curl -fsSL https://app.vagrantup.com/ubuntu/boxes/focal64 | jq '.versions[0].providers[0].url'
```

> `16.04 LTS x86`

```bash
vagrant box add ubuntu/xenial32
```

```bash
curl -fsSL https://app.vagrantup.com/ubuntu/boxes/xenial32| jq '.versions[0].providers[0].url'
```


## Ref

* [http://cloud-images.ubuntu.com](http://cloud-images.ubuntu.com) / [清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/ubuntu-cloud-images/)
* [https://cloud.centos.org/](https://cloud.centos.org/) / [https://mirrors.ustc.edu.cn/centos-cloud/](https://mirrors.ustc.edu.cn/centos-cloud/)