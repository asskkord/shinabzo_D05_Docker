## Готовый докер

Загрузка образа nginx через команду `docker pull`

![docker_pull](pictures/1-1.png)

Проверка наличия образа через команду `docker images`

![docekr_images](pictures/1-2.png)

Запуск образа через комнаду `docker run`

![docker_run](pictures/1-3.png)

Проверка наличия процесса через команду `docker ps`

![docker_ps](pictures/1-4.png)

Просмотр информации о контейнере через команду 
`docker inspect %container_id%`

![docker_inspect](pictures/1-5.png)

Размер докер образа

![docker_shmsize](pictures/1-6.png)

Его IP

![docker_ip](pictures/1-7.png)

Замапленый порт

![docker_port](pictures/1-8.png)

Остановка докер образа и проверка его остановки

![docker_stop](pictures/1-9.png)
![docker_stop](pictures/1-10.png)

Запуск образа с замапленными портами

![docker_map](pictures/1-11.png)

Проверка работы сервера

![docker_localhost](pictures/1-12.png)

Перезагрузка докер образа и проверка наличия процесса

![docker_restart](pictures/1-13.png)
![docker_restart](pictures/1-14.png)
![docker_restart](pictures/1-15.png)



## Операции с контейнером

Вывод содержимого файла nginx.conf

![docker_exec](pictures/2-1.png)

Создание файла nginx.conf и астройка в нем по пути /status отдачу страницы статуса сервера

![docker_nginx_conf](pictures/2-3.png)

Коприование nginx.conf внутрь докер образа, перезагрузка nginx, проверка статуса сервера

![docker_nginx_conf_cp](pictures/2-4.png)
![docker_nginx_conf_cp](pictures/2-5.png)
![docker_nginx_conf_cp](pictures/2-6.png)

Экспорт докер контейнера в файл, остановка контейнера

![docker_export](pictures/2-7.png)

Удаление докер образа и удаление остановленного контейнера

![docker_rmi](pictures/2-8.png)

Импорт сохраненного контейнера, его запуск и проверка работоспособности
![docker_import](pictures/2-9.png)
![docker_import](pictures/2-10.png)
![docker_import](pictures/2-11.png)
