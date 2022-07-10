Task 3.3 – Налаштування маршрутизації

Нехай в результаті поділу магістральної мережі (Рис.1) на підмережі були призначені адреси інтерфейсам маршрутизаторів
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/zavdannya.png"></ul>

1. Налаштувати таблиці маршрутизації на маршрутизаторах ISP1, ISP2 та ISP3. В таблиці маршрутизації слід вносити тільки віддалені мережі. Наприклад, на Router ISP2 необхідно вказати маршрути тільки до мереж 10.99.25.0/ та 4.25.99.0/24.

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/1_ISP_2.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/1_ISP_3.png"></ul>

2. Налаштувати маршрутизацію на бездротовому маршрутизаторі Home Router, для чого додати Default маршрут на Router ISP2,

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/2_Home_Route.png"></ul>

3. Перевірити працездатність мережі за допомогою команди ping та tracert.

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/3_ping_tracer.png"></ul>

5. На маршрутизаторах ISP1, ISP2 та ISP3 налаштувати протокол RIP, для чого вказати перелік безпосередньо приєднаних мереж у класовому форматі.

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/5_ISP_2.png"></ul>

6. Для перевірки працездатності повторити ping та tracert

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/6_Client.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1a96d9597ffc1f04e6bac1a3f4bc9d1f72af9a1d/m3/task3.3/scrin/6_DNS_Server.png"></ul>

