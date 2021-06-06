> This project based on https://github.com/BytemarkHosting/docker-webdav , more documents please view the source project.

## Usage

```shell
docker run --restart always -v {MOUNT_PATH}:/var/lib/dav -e AUTH_TYPE=Digest -e USERNAME={USERNAME} -e PASSWORD={PASSWORD} --publish {MOUNT_PORT}:80 --name {ALIAS} -d weizai/webdav
```

* such as
```shell
docker run --restart always -v /root/webdav:/var/lib/dav -e AUTH_TYPE=Digest -e USERNAME=admin -e PASSWORD=123456 --publish 65535:80 --name webdav -d weizai/webdav
# means:
#     url: http://xxx.xxx.xxx.xxx:65535
#     username: admin
#     password: 123456
#     storage path: /root/webdav
#     docker process alias: webdav
```
