### Задание 1. Создать Deployment приложения, состоящего из двух контейнеров и обменивающихся данными.

Вывод файла с busybox

![alt text](busybox.png)

Вывод файла с multitool

![alt text](multitool.png)

Манифест [Deployment](deployment_multitool_busybox.yaml)

### Задание 2. Создать DaemonSet приложения, которое может прочитать логи ноды.

Чтение файла из ноды яндекс-клауд

![alt text](from_yc.png)

Чтение файла изнутри пода 

![alt text](from_container.png)

Манифест [DaemonSet](daemonset_multitool.yaml)