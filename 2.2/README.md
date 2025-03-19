### Задание 1. Создать Deployment приложения, использующего локальный PV, созданный вручную.

Чтение файла с multitool, в который пишет busybox

![alt text](<Screenshot 2025-03-19 174047.png>)

После удаления Deployment и PVC, PV будет в состоянии Released. У PV есть reclaimPolicy, который определяет, что делать с хранилищем после удаления PVC.

Если reclaimPolicy: Retain, Kubernetes не удаляет данные, а оставляет PV в состоянии Released.

![alt text](<after del.png>)

Файл должен быть доступен, потому что PV использует локальную директорию на хосте, и данные сохраняются на этом диске.

![alt text](<file is saved.png>)

После удаления PV файл на локальном диске останется, потому что PV не управляет удалением данных на локальной папке (hostPath).

![alt text](<Screenshot 2025-03-19 175902.png>)

Манифест [Deployment](deployment_multitool_busybox.yaml)

### Задание 2. Создать Deployment приложения, которое может хранить файлы на NFS с динамическим созданием PV.

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