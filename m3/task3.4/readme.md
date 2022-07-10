Task 3.4 – Налаштування DHCP, DNS, NAT

1. Налаштувати DHCP Server в Enterprise мережі (рис.1). Для цього увійти в налаштування DHCP Server

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/1.png"></ul>

2. Зробити налаштування DHCP Pool, вказавши початкову адресу 10.Y.D.10 та адресу Default Gateway – адресу інтерфейсу GE0/0 Router ISP1. Зберегти налаштування (кнопка Save) та увімкнути DHCP сервіс

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/2.1.png"></ul>

3. Перевірити працездатність сервісу, поставивши в налаштуваннях Client 1 та Client 2 DHCP.

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/3.1.png"></ul>
<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/3.2.png"></ul>

9. Додати в мережу Home Office Home Server та призначити йому статичну адресу

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/9.1.png"></ul>

10. На Home Server для HTTP сервісу відкоригувати index.html

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/10.1.png"></ul>

11. Налаштувати Port Forwarding на Home Router

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/11.png"></ul>

12. Додати на DNS Server запис для Home Server

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/12.png"></ul>

13. Перевірити працездатність шляхом уведення на Client1 у Desktop/Web Browser - domain3.com

<ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4afc20fb854b72d800622673354e73e9f0fc1f5a/m3/task3.4/scrin/13.png"></ul>
