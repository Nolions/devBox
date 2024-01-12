# devbox

開發環境整合

## 環境需求

1. docker
2. docker-composer

## Use

step1. 建立`.env`

執行以下命令

```shell
cp .env.example .env
```

step2. 更改你需要的設定，例如：

```shell
# 變更mysql root 密碼
MYSQL_ROOT_PASS=root
```

## run and stop

```shell
// 透過以下指令啟動所需要的服務
// docker-compose up -d <service>
// EX: 啟動mysql
docker-compose up -d paras

// 停止所有服務
docker-compose down
```
