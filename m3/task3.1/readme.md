<ul><center>Task 3.1 - Створення мереж Home Office, Enterprise, Data Center</center></ul>


1. Створити мережі, як показано на рисунку. Рекомендовані моделі комутаторів Catalyst 2960, безпровідний маршрутизатор – WRT300N. В мережі Data Center підключити сервери до портів


<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/3d95ef6e01a7306a530c524d4a096a6bc985ddf7/m3/task3.1/scrin/zavdannya.png"></ul>

2. В мережі Enterprise призначити статичні адреси, сформовані за таким правилом: Адреса мережі 10.Y.D.0/24, де Y – дві останні цифри з вашого року народження, D – дата народження. Хостова частина адреси Client 1 – 10, Client 2 – 20, DHCP Server – 100. Наприклад, якщо ви народились 25-го квітня 1999 р., то адреса мережі буде 10.99.25.0/24, а адреса Client 1- 10.99.25.10/24

<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/aa45a75fc5bfeefd44503fc51a07772feb36c511/m3/task3.1/scrin/2.1.png"></ul>
<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/aa45a75fc5bfeefd44503fc51a07772feb36c511/m3/task3.1/scrin/2.2.png"></ul>
<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/aa45a75fc5bfeefd44503fc51a07772feb36c511/m3/task3.1/scrin/2.3.png"></ul>

3. Перевірити зв'язок за допомогою команди ping 

<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/7d6fdfe03ec22b9e02316432eeff9861dc529bcf/m3/task3.1/scrin/2_ping_1.png"></ul>
<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/7d6fdfe03ec22b9e02316432eeff9861dc529bcf/m3/task3.1/scrin/2_ping_2.png"></ul>
<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/7d6fdfe03ec22b9e02316432eeff9861dc529bcf/m3/task3.1/scrin/2_ping_dhcp.png"></ul>

4. В мережі Data Center призначити статичні адреси, сформовані за таким правилом: M.D.Y.0/24, де М – номер місяця народження, D і Y аналогічно попередньому. Хостова частина Web Server 1 – 50, Web Server 2 – 100, DNS Server – 150.

<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4ba821ae017704093dc5ce77e2ab9c1f28e2103d/m3/task3.1/scrin/4_dns_server.png"></ul>
<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4ba821ae017704093dc5ce77e2ab9c1f28e2103d/m3/task3.1/scrin/4_web_server_1.png"></ul>
<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4ba821ae017704093dc5ce77e2ab9c1f28e2103d/m3/task3.1/scrin/4_web_server_2.png"></ul>

5. Перевірити зв'язок за допомогою команди ping

<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4ba821ae017704093dc5ce77e2ab9c1f28e2103d/m3/task3.1/scrin/4_ping_1.png"></ul>
<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/4ba821ae017704093dc5ce77e2ab9c1f28e2103d/m3/task3.1/scrin/4_ping_dns.png"></ul>

7. Призначити Сlient3 статичну адресу 192.168.0.(D+10).

<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/95ea07a9e0f6890724f0babca14e7db32d855c98/m3/task3.1/scrin/7_client_3.png"></ul>

8. Перевірити зв'язок з маршрутизатором за допомогою команди ping 192.168.0.1

<img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/95ea07a9e0f6890724f0babca14e7db32d855c98/m3/task3.1/scrin/8_ping.png"></ul>
