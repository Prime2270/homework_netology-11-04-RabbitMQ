# Домашнее задание к занятию "`Очереди RabbitMQ`" - `Яковлев Константин`

### ВНИМАНИЕ 

`IP адресса на скриншотах будут отличаться потому что во время выполнений дз `
`пришлось с нуля поднимать все сервисы на локльном сервере`

### Задание 1 Установка RabbitMQ

`Используя Vagrant или VirtualBox, создайте виртуальную машину и установите RabbitMQ.`
`Добавьте management plug-in и зайдите в веб-интерфейс.`
`Итогом выполнения домашнего задания будет приложенный скриншот веб-интерфейса RabbitMQ.`

![job2.2](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job2.2.png)

### Задание 2 Отправка и получение сообщений

`Используя приложенные скрипты, проведите тестовую отправку и получение сообщения.`
`Для отправки сообщений необходимо запустить скрипт producer.py.`
`Для работы скриптов вам необходимо установить Python версии 3 и библиотеку Pika.`
`Также в скриптах нужно указать IP-адрес машины, на которой запущен RabbitMQ, заменив localhost на нужный IP.`

`Зайдите в веб-интерфейс, найдите очередь под названием hello и сделайте скриншот.`
`После чего запустите второй скрипт consumer.py и сделайте скриншот результата выполнения скрипта`
`В качестве решения домашнего задания приложите оба скриншота, сделанных на этапе выполнения.`
`Для закрепления материала можете попробовать модифицировать скрипты,`
`чтобы поменять название очереди и отправляемое сообщение.`

![job2](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job2.png)

![job2.1](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job2.1.png)

![job2.2](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job2.2.png)

### Задание 3 Подготовка HA кластера

`Используя Vagrant или VirtualBox, создайте вторую виртуальную машину и установите RabbitMQ.`
`Добавьте в файл hosts название и IP-адрес каждой машины, чтобы машины могли видеть друг друга по имени.`

`После этого ваши машины могут пинговаться по имени.`
`Затем объедините две машины в кластер и создайте политику ha-all на все очереди.`
`В качестве решения домашнего задания приложите скриншоты из веб-интерфейса`
`с информацией о доступных нодах в кластере и включённой политикой.`

![job3](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job3.png)

![job3.1](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job3.1.png)

![job3.2](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job3.2.png)

![job3.3](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job3.3.png)

![job3.4](https://github.com/Prime2270/homework_netology-11-04-RabbitMQ/blob/main/screenshots/job3.4.png)


### Доработка

`Для создания политик использовал следующие команды`

	- rabbitmqctl set_policy ha-all "" '{"ha-mode":"all","ha-sync-mode":"automatic"}'
	- sudo rabbitmqctl set_policy HA ".*" '{"ha-mode": "all"}'

![job4]()

![job4.1]()
