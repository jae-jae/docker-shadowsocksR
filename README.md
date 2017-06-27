# docker-shadowsocksR
docker:shadowsocksR,https://shadowsocks.be/9.html

## Run

```shell
docker run -d -p 8388:8388 --name=ssr jaegerdocker/ss-r
```

## Config

config path:`/etc/shadowsocks.json`

```
{
"server":"0.0.0.0",
"server_ipv6": "[::]",
"local_address":"127.0.0.1",
"local_port":1080,
"port_password":{
    "8989":"password1",
    "8990":"password2",
    "8991":"password3"
},
"timeout":300,
"method":"aes-256-cfb",
"protocol": "origin",
"protocol_param": "",
"obfs": "plain",
"obfs_param": "",
"redirect": "",
"dns_ipv6": false,
"fast_open": false,
"workers": 1
}
```

After modifying the configuration file, restart the docker container

```
docker restart ssr
```