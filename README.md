HW3

Подключение через 1 команду  
`ssh -J appuser@84.201.158.16 appuser@10.128.0.31`

Данные для подключения
```
bastion_IP = 84.201.158.16
someinternalhost_IP = 10.128.0.31
```

Дополнительное задание с Lets Encrypt
1) Переходим в pitunul во вкладку seting
2) В поле Lets Encrypt Domain вводим наш <ip адрес bastion>.nip.io (84.201.158.16.nip.io)
