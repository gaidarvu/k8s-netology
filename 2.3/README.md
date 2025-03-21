### Задание 1. Создать Deployment приложения и решить возникшую проблему с помощью ConfigMap. Добавить веб-страницу

Поды поднялись

![alt text](applyed.png)

Доступ к страничке через консоль

![alt text](<via console.png>)

Доступ к страничке через web с проброшенным портом

![alt text](<via web.png>)

index.html в смонтированной директории

![alt text](<mount page.png>)

### Задание 2. Создать приложение с вашей веб-страницей, доступной по HTTPS

Созданные pod, pv, pvc

![alt text](<depl start.png>)

Пробуем создать файл и записать туда информацию

![alt text](readwrite.png)

Удалось отыскать его на ноде в default-storage

![alt text](<file on node.png>)

Почему-бы не записать файл напрямую в сторадж

![alt text](<test write to storage.png>)

Идем на pod и смотрим что получилось

![alt text](<test pass.png>)

Манифест [Deployment](deployment_multitool.yaml)