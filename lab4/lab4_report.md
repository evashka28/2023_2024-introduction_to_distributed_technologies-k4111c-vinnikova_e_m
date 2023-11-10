<p> University: [ITMO University](https://itmo.ru/ru/)
<p> Faculty: [FICT](https://fict.itmo.ru)
<p> Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <p>
<p> Year: 2023/2024
<p> Group: K4411c
<p> Author: Vinnikova Eva Mikhailovna
<p> Lab: Lab4
<p> Date of create: 17.10.2023
<p> Date of finished: 10.11.2023

<h4>Отчёт о выполнении лабораторной работы</h4>

1. Первым шагом были установлены установите плагин CNI=calico и режим работы Multi-Node Clusters одновеременно (см. Рисунок 1), были развернуты 2 ноды (см. Рисунок 2).    
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/1.png">
Рисунок 1 - Запуск
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/2.png">
Рисунок 2 - Ноды

2. Далее была проверена работа CNI плагина Calico (см. Рисунок 3)
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/3.png">
Рисунок 3 - Calico

3. Были созданы собственные ippool и были добавлены label к нодам (см. Рисунок 4).
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/4.png">
Рисунок 4 - Ipool

4. Был создан манифест deployment с 2 репликами контейнера ifilyaninitmo/itdt-contained-frontend:master и в него были переданы переменные REACT_APP_USERNAME и REACT_APP_COMPANY_NAME (см. Рисунок 5).
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/5.png">
Рисунок 5 - Deployment

5.  Далее был создан сервис для доступа к depl при подключении к порту 3000. Для доступа к контейнеру с локального компьютера был прокинут порт компьютера в контейнер.(см. Рисунок 2)
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/6.png">
Рисунок 6 - Работа с deployment

6.  Было выполнено подключение к контейнерам через веб браузер. На странице в веб браузере показаны переменные REACT_APP_USERNAME, REACT_APP_COMPANY_NAME и Container name(см. Рисунок 3). Переменные, заданные при создании подов, являются неизменяемыми. Но мя контейнера может быть изменено, так как в deployment содержится два равноправных пода, которые могут обрабатывать запросы.
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/7.png">
Рисунок 7 - Страница в браузере

7. С помощью kubectl exec были пропингованы "поды" используя FQDN имя соседенего "пода"(см. Рисунок 8)
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/8.png">
Рисунок 8 - Ping 

8. Была создана новая схема организации контейнеров и сервисов (см. Рисунок 9)
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab4/img/9.png">
Рисунок 9 - Схема организации контейнеров и сервисов


**Выводы**: В В ходе выполнения лабораторной работы были изучены CNI Calico, IPAM Plugin и CoreDNS.
