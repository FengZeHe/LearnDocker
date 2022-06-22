### Docker学习笔记

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
 
```

```shell
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

设置镜像加速

```json
在/etc/docker/下创建daemon.json文件，并写入
{"registry-mirrors":["https://reg-mirror.qiniu.com/"]}

//sudo systemctl daemon-reload
//sudo systemctl restart docker
// docker info
```

