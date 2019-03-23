# docker
记录
#谷歌镜像翻墙pull
新建文本
sudo vim /etc/systemd/system/docker.service.d/http-proxy.conf
[Service]
Environment="ALL_PROXY=socks5://127.0.0.1:1080"
保存
root@:~# systemctl daemon-reload
root@:~# systemctl restart docker
查看设置是否成功
root@:~#systemctl show --property=Environment docker
如果显示Environment=ALL_PROXY=socks5://192.168.0.103:1080就可以拉谷歌等镜像了
