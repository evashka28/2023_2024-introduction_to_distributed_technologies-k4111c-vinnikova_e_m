<p> University: [ITMO University](https://itmo.ru/ru/)
<p> Faculty: [FICT](https://fict.itmo.ru)
<p> Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies) <p>
<p> Year: 2023/2024
<p> Group: K4411c
<p> Author: Vinnikova Eva Mikhailovna
<p> Lab: Lab1
<p> Date of create: 17.10.2023
<p> Date of finished: 27.10.2023

<h4>Отчёт о выполнении лабораторной работы</h4>

1. Первым шагом были установлены Docker и minikube. После установки был развернут minikube cluster с помощью команды minikube start

2. Далее был написан манифест для развертывания пода HashiCorp Vault (см. Рисунок 1). Манифест был применен с помощью команды kubectl apply . Далее был создан сервис для доступа к поду vault при подключении к порту 8200. Для доступа к контейнеру с локального компьютера был прокинут порт компьютера в контейнер.(см. Рисунок 2)
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab1/img/1.png">
Рисунок 1 - Манифест
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab1/img/2.png">
Рисунок 2 - Работа с подом

3. Для авторизации в Vault был найден токен, который отображается в логах при запуске приложения с помощью команды kubectl logs vault. (см. Рисунок 3).
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab1/img/3.png">
Рисунок 3 - Токен

4. Была выполнена успешная авторизация с помощью токена (см. Рисунок 4).
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab1/img/4.png">
Рисунок 4 - Успешная авторизация

5. Была создана новая схема организации контейеров и сервисов
<image src="https://github.com/evashka28/2023_2024-introduction_to_distributed_technologies-k4111c-vinnikova_e_m/blob/main/lab1/img/5.png">
Рисунок 5 - Схема организации контейеров и сервисов



**Выводы**: В В ходе выполнения лабораторной работы в контейнере докер был запущен кластер kubernetes, состоящий из одной ноды. Также был написан манифест для создания пода и сервис, позволяющий получить к поду доступ с локального компьютера.
