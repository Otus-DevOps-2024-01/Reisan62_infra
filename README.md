# HW4 "Деплой тестового приложения"

### Данные для подключения
```
testapp_IP = 51.250.9.60
testapp_port = 9292
```
### Yandex Cloud CLI

```
yc compute instance create \
--name reddit-app \
--zone ru-central1-a \
--hostname reddit-app \
--memory=2 \
--platform=standard-v3 \
--cores=2 \
--core-fraction 50 \
--create-boot-disk image-folder-id=standard-images,image-family=ubuntu-1604-lts,size=8 \
--network-interface subnet-name=default-ru-central1-a,nat-ip-version=ipv4 \
--ssh-key C:/Users/baldy/AppData/Roaming/MobaXterm/home/.ssh/appuser.pub
```
### Делаем наши скрипты исполняемыми
```
git update-index --chmod=+x install_ruby.sh
git update-index --chmod=+x install_mongodb.sh
git update-index --chmod=+x deploy.sh
```
## Дополнительное задание

Создаем скрипт startup.yaml с нашими данными, после чего выполняем команды в CLI
```
yc compute instance create \
yc compute instance create `
--name reddit-app2 `
--zone ru-central1-a `
--hostname reddit-app2 `
--memory=2 `
--platform=standard-v3 `
--cores=2 `
--core-fraction 50 `
--create-boot-disk image-folder-id=standard-images,image-family=ubuntu-1604-lts,size=8 `
--network-interface subnet-name=default-ru-central1-a,nat-ip-version=ipv4 `
--metadata-from-file user-data=startup.yaml
```




# HW3 "Знакомство с облачной инфраструктурой Yandex.Cloud"

### Подключение через 1 команду
`ssh -J appuser@84.201.158.16 appuser@10.128.0.31`

### Данные для подключения
```
bastion_IP = 84.201.158.16
someinternalhost_IP = 10.128.0.31
```

### Дополнительное задание с Lets Encrypt
1) Переходим в pitunul во вкладку seting
2) В поле Lets Encrypt Domain вводим наш <ip адрес bastion>.nip.io (84.201.158.16.nip.io)
