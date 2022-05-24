# scripts

## Соглашение о использовании
Реализована следующая структура
```sh
./bin/{app-name}          # запускаемый сервис  
./configs/{app-name}.toml # конфигурвционный файл сервиса  
./logs/{app-name}.log     # StdOut|StdErr сервиса  
```

## Имитация сервисного режима
```sh
./scripts/service {start|stop|restart|status} {app-name}  
```
start - выполняет ```go build -o {/bin/app-name}``` с дальнейшим запуском  
stop - выполняет ```kill``` по основному и дочерним процессам  
restart - последовантельно выполняет ```stop``` & ```start```  

## Openssl Key
Создание пары ключей ```rsa:2048``` в каталоге ```./certs```
```sh
./scripts/key 
```
