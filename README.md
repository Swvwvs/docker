# Установил docker
``` 
apt-get update
apt-get install docker-engine
```
# Активировал docker
```
systemctl enable --now docker
```
# Скачал образ 'hello-world'
```
docker pull hello-world
```
# Запустил образ
```
docker run hello-world
```
# Удалил образ 
```
docker image rm -f hello-world:latest
```

# Установил и запустил NGINX с портом 80
```
docker run -p 80:80 nginx
```
# Проверил работу в браузере по IP сервера
```
10.12.24.4:80
```
