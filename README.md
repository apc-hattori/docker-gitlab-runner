## 登録

```shell
docker-compose run --rm main register --executor docker --docker-privileged=true --docker-image alpine:latest
```

起動後、対話式で入力していく

※gitlab上で参照できるURLと登録トークンが必要

```
Please enter the gitlab-ci coordinator URL (e.g. https://gitlab.com/):
(※gitlabのURL)

Please enter the gitlab-ci token for this runner:
(※gitlabの登録トークン)

Please enter the gitlab-ci description for this runner:
(登録名)

Please enter the gitlab-ci tags for this runner (comma separated):
[docker]:(エンターキー)

Please enter the default Docker image (e.g. ruby:2.1):
[alpine:latest]:(エンターキー)

# 下記のメッセージが出ればOK
Runner registered successfully. Feel free to start it, but if it's running already the config should be automatically reloaded! 
```

config下にconfig.tomlが作成されている

## 起動

```shell
docker-compose up -d
```
