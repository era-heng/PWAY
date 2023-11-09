# PWAY:redis5-php8.1

- 合二为一
  - redis:5.0-alpine3.16
    - 官方镜像1 1b24e5253e86 https://hub.docker.com/_/redis/tags?page=1&name=5.0-alpine
    - 官方镜像2 1b24e5253e86 https://hub.docker.com/_/redis/tags?page=1&name=5.0-alpine3.16
  - php:8.1-alpine3.16
    - 官方镜像1 8f5ce1bab880 https://hub.docker.com/_/php/tags?page=1&name=8.1-alpine3.16
    - 官方镜像2 8f5ce1bab880 https://hub.docker.com/_/php/tags?page=1&name=8.1-cli-alpine3.16
    - 官方镜像设计图 https://github.com/docker-library/php/blob/master/8.1/alpine3.16/cli/Dockerfile

# 验证测试

```sh
docker run --name PWAY -p9529:6379 \
 -v /bigdata/SITES:/www \
 -d a2fc241c1a14

docker exec PWAY php -m
docker exec PWAY redis-cli info
```
