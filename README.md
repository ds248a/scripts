# scripts

## Соглашение о использовании
```
./bin/{app-name} - запускаемый сервис  
./configs/{app-name}.toml - конфигурвционный файл сервиса  
./logs/{app-name}.log - StdOut|StdErr сервиса  
```

## Имитация сервисного режима
```
./scripts/service {start|stop|restart|status} {app-name}  
```
start - выполняет 'go build -o {/bin/app-name}' с дальнейшим запуском  
stop - выполняет 'kill' по основному и дочерним процессам  
restart - 'stop' + 'start'




