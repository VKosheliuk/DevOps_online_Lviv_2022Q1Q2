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

