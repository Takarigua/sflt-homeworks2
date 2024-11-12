# Домашнее задание к занятию "`Кластеризация и балансировка нагрузки`" - `Марченко Вячеслав Игоревич`

---

### Задание 1

Запустите два simple python сервера на своей виртуальной машине на разных портах
Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
Настройте балансировку Round-robin на 4 уровне.
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

Ответ:
1. Сделал всё по лекции Nginx и HAProxy Кластеризация и балансировка нагрузки, все конфигурационные файлы брал из материалов для лекции/домашнего задания (https://github.com/netology-code/sflt-homeworks/tree/main/2), поэтому не знаю, есть ли смысл их прикладывать, ибо они совпадают на 100%. Все завелось как и в лекции (прикладываю скриншот)
2. ![HAProxy](https://github.com/Takarigua/sflt-homeworks2/blob/39dbe638b3ebc6952034d69bc2e8b9f4b7559830/img/Haproxy.png)

---

### Задание 2

Запустите три simple python сервера на своей виртуальной машине на разных портах
Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

Ответ:
1. Вот скриншоты того, что он распределяет ![weight host](https://github.com/Takarigua/sflt-homeworks2/blob/c7bde29606330521908ac263d772e28103a33e84/img/Weight.png)
2. Скриншот без хоста и с ним ![balance](https://github.com/Takarigua/sflt-homeworks2/blob/c7bde29606330521908ac263d772e28103a33e84/img/Balance.png)
3. Вот файл haproxy.cfg, где дописано про балансировку ![haproxy config](https://github.com/Takarigua/sflt-homeworks2/blob/main/img/HAProxy%20config.png)
4. И сам файл: https://github.com/Takarigua/sflt-homeworks2/blob/221e14a0bd25c44cfdfe466d3130d3fb664ca5ad/haproxy.cfg
