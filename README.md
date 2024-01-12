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

## config

### redis

預設啟動redis是沒有密碼的

如果需要設定redis連線時的密碼

step1. 在`.env`檔案中的REDIS_PASS輸入要設定的密碼

sep2. 取消docker-composer.yml中redis中command `#`註解

```yml
command: redis-server --requirepass ${REDIS_PASS}
```
