### Задание 1. Создать Deployment приложения, использующего локальный PV, созданный вручную.

Чтение файла с multitool, в который пишет busybox

![alt text](busybox.png)

После удаления Deployment и PVC, PV будет в состоянии Released, потому что persistentVolumeReclaimPolicy установлено в Retain

![alt text](multitool.png)

Файл должен быть доступен, потому что PV использует локальную директорию на хосте, и данные сохраняются на этом диске.

После удаления PV файл на локальном диске останется, потому что данные не были удалены автоматически (PV имеет Retain policy).

Манифест [Deployment](deployment_multitool_busybox.yaml)

### Задание 2. Создать Deployment приложения, которое может хранить файлы на NFS с динамическим созданием PV.

Чтение и запись файла изнутри пода

![alt text](from_yc.png)

Манифест [Deployment](deployment_multitool_busybox.yaml)