### Задание 1. Создать Deployment и обеспечить доступ к контейнерам приложения по разным портам из другого Pod внутри кластера

Pod multitool и запрос curl с него

На 9001

![alt text](9001.png)

На 9002

![alt text](9002.png)

Манифесты [deployment_nginx_multitool.yaml](deployment_nginx_multitool.yaml), [Pod multitool for curl](pod_multitool.yaml)

### Задание 2. Создать Service и обеспечить доступ к приложениям снаружи кластера

Запрос с браузера

![alt text](30001.png)

![alt text](30002.png)

Запрос curl с консоли

![alt text](image.png)

Манифест [Service](service_for_nginx_external.yaml)