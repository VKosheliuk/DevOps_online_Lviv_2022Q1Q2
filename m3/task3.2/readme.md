<ul>Task 3.2 - З’єднання окремих мереж за допомогою мережі Internet та налаштування VLAN</ul>

1. З’єднати створені у попередньому Taskу мережі між собою, як показано на рисунку. Для побудови мережі Internet використати маршрутизатори PT-Empty, попередньо вставивши в них 5 модулів 1CGE. Switch мережі Enterprise підключити до інтерфейсу GigabitEthernet0/0 (GE0/0) Router ISP1, Switch мережі Data Center підключити до інтерфейсу GigabitEthernet0/0 (GE0/0) Router ISP3, WAN порт Home Router мережі Home Office підключити до інтерфейсу GigabitEthernet0/0 (GE0/0). Маршрутизатори з’єднати між собою через інтерфейси, як показано на рисунку.

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/1_schema.png"></ul>

6. Перевірити зв’язок між серверами за допомогою команди ping та маршрут проходження пакета за допомогою tracert

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/6_tracer_1.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/6_tracer_2.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/6_tracer_3.png"></ul>

8. Повторити пункт 6 та зафіксувати і пояснити зміни
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/8_tracer_1.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/8_tracer_2.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/8_tracer_3.png"></ul>

16. Перевірити працездатність за допомогою команди ping з одного сервера на інший.
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/VLAN_ping_tracer_1.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/VLAN_ping_tracer_2.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/1907a8ef9f886accdf8d325ddded36e4493dc339/m3/task3.2/scrin/VLAN_ping_tracer_3.png"></ul>
