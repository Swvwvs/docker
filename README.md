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
# Создал 'dockerfile' папку для него, зашёл в него для редоктирования
```
mkdir mynginx
cd mynginx
touch dockerfile
vim dockerfile
```
# Отредактировал 
```
FROM nginx
RUN echo '<h1>zaza</h1>' > /usr/share/nginx/html/index.html
```
- FROM - определяет, что будет использоваться в качестве базового образа
- RUN - определят, что будет отображаться на экране
# Вышел из каталога и построил образ в каталоге 'mynginx'
```
cd
docker build -t nginx:v2 mynginx/
```
# Посмотрел сохранился ли образ
```
docker images
```
