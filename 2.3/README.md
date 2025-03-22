### Задание 1. Создать Deployment приложения и решить возникшую проблему с помощью ConfigMap. Добавить веб-страницу

Поды поднялись

![alt text](applyed.png)

Доступ к страничке через консоль

![alt text](<via console.png>)

Доступ к страничке через web с проброшенным портом

![alt text](<via web.png>)

index.html в смонтированной директории

![alt text](<mount page.png>)

Манифесты [Deployment](deployment_multitool_nginx.yaml), [Service](service.yaml), [ConfigMaps](configmap.yaml)

### Задание 2. Создать приложение с вашей веб-страницей, доступной по HTTPS

Поды поднялись

![alt text](applyed2.png)

Генерим самоподписанный сертификат

![alt text](ssl1.png)

![alt text](ssl2.png)

Доступ по https из service

![alt text](https_access.png)

Манифесты [Deployment](deployment_nginx.yaml), [Service](service_nginx.yaml), [ConfigMaps](configmap_nginx.yaml), [Ingress](ingress.yaml)