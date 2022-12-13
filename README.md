# learn-kub_LAMP
Описательная часть лабораторной работы по развертыванию сайта WordPress (LAMP) через Jenkins используя Kubernetes (minikube).
Для лабораторной работы потребуется:
1.	виртуальная машина с развернутым minikube (Debian).
2.	виртуальная машина с Jenkins (Debian).

К master node Jenkins была подключена вирт. машина slave node c minikube. Jenkins настроен на выполнение job на slave node по метке (label) от пользователя не root (в моем случае «user»).
Далее были созданы два манифеста. Один для БД MySQL, второй для Wordpress с Apache. Был написан jenkinsfile. Все три файла загружены в Github.

Jenkins при выполнении job подключается к репозиторию Github, откуда он скачивает все файлы и исполняет инструкции прописанные в jenkinsfile.

![изображение](https://user-images.githubusercontent.com/109180164/207438139-d97d993a-84a8-451b-bca9-15d4449eafdf.png)

![изображение](https://user-images.githubusercontent.com/109180164/207438164-a6873aeb-8356-4ede-9612-390cc1591827.png)

![изображение](https://user-images.githubusercontent.com/109180164/207438190-50a5817b-5856-47c4-8c09-79f29cbb75af.png)
