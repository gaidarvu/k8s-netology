### Задание 1. Создайте конфигурацию для подключения пользователя

Генерим сертификат и создаем пользователя

![alt text](certsgen.png)

Поднял роль и роль-биндинг

![alt text](<describe role.png>)

![alt text](<describe rolebind.png>)

Для проверки разрешений поднял простой Pod из второго вебинара. Как видно, что нужно - разрешено, что не нужно - запрещено.

![alt text](forbidden.png)

Для поднятия роли и пода пришлось в kubectl переключаться между админом и пользователем

Манифесты [Role](role.yaml), [RoleBinding](rolebinding.yaml), [Pod](pod-netology-web.yaml)
