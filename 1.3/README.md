### Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod

Во избежание ошибки сразу-же посадил multitool на порт 8080. Тем не менее, пока не добавил sleep infinity во внутрь контейнера, он падал с ошибкой.

Pod без масштабирования

![alt text](deployment.png)

Pod с масштабированием

![alt text](deployment_replicas.png)

IP адреса реплик

![alt text](deployment_replicas_ip.png)

Созданный service

![alt text](service.png)

Service подключен к репликам

![alt text](service2.png)

Созданный Pod multitool и запрос curl с него

![alt text](curl_from_multitool.png)

Манифесты [Deployment Nginx+Multitool](deployment_nginx_multitool.yaml), [Service](service_for_replicas.yaml), [Pod multitool for curl](pod_multitool.yaml)

### Задание 2. Создать Deployment и обеспечить старт основного контейнера при выполнении условий

Ожидание сервиса, после которого должен стартовать nginx было реализовано через проверку локального домена (nginx-service.default.svc.cluster.local) в default namespace, чтобы отсечь лишние домены от яндекса

Ожидание сервиса

![alt text](wait_for_nginx_2.png)

![alt text](wait_for_nginx.png)

После старта сервиса

![alt text](start_nginx.png)

![alt text](start_nginx_2.png)

Манифесты [Deployment Nginx with BusyBox](deployment_nginx_busybox.yaml), [Service](service_for_replicas.yaml)