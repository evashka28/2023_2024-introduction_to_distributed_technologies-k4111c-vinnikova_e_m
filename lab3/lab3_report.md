<p> University: [ITMO University](https://itmo.ru/ru/)
<p> Faculty: [FICT](https://fict.itmo.ru)
<p> Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <p>
<p> Year: 2023/2024
<p> Group: K4411c
<p> Author: Vinnikova Eva Mikhailovna
<p> Lab: Lab1
<p> Date of create: 17.10.2023
<p> Date of finished: 03.11.2023

<h4>Отчёт о выполнении лабораторной работы</h4>

1.  Был создан configMap с переменными: REACT_APP_USERNAME, REACT_APP_COMPANY_NAME (см. Рисунок 1). Данные переменные передаются в ReplicaSet
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab3/img/1.png">
Рисунок 1 - configMap

2.  Далее был создан replicaSet с 2 репликами контейнера ifilyaninitmo/itdt-contained-frontend:master, в него были переданы переменные REACT_APP_USERNAME, REACT_APP_COMPANY_NAME с помощью configMap .(см. Рисунок 2)
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab3/img/2.png
Рисунок 2 - ReplicaSet

3. С помощью OpenSSL был сгенерирован TLS сертификат. (см. Рисунок 3).
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab3/img/3.png">
Рисунок 3 - Генерация сертификата

4. Был создан Secret для хранения данных о сертификате (см. Рисунок 4).
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab3/img/4.png">
Рисунок 4 - Secret

5. Был создан ingress, где указан ранее импортированный сертификат, FQDN  и имя сервиса (см. Рисунок 5).
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab3/img/5.png">
Рисунок 5 - Ingress

6. Была создана новая схема организации контейеров и сервисов (см. Рисунок 6)
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab3/img/6.png">
Рисунок 6 - Схема организации контейеров и сервисов



**Выводы**: В В ходе выполнения лабораторной работы были изучены сертификатамы и "секреты" в Minikube, правила безопасного хранения данных в Minikube.
