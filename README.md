# lab_ansible_basisb №4
1. Производим клонирование ВМ и пробрасываем порты на 10.0.2.10 - 22>22 И 10.0.2.16 - 80>80
   
   <img width="781" height="438" alt="image" src="https://github.com/user-attachments/assets/3ea76921-e6d0-4333-97e6-a35044dd0c01" />

2. Настроили общую сеть на "Сеть NAT" и уже далее локально изменяем параметры внутри каждой из ВМ
   
  ВМ 10.0.2.10 <img width="827" height="632" alt="image" src="https://github.com/user-attachments/assets/031f36ff-7e9e-4d92-9874-e837bef437d4" />

  ВМ 10.0.2.16 <img width="831" height="642" alt="image" src="https://github.com/user-attachments/assets/3a40759f-5456-4b6b-9a19-d9f69dfa1302" />

3. Далее пошли танцы с бубном:

   а) Пропал в принципе интернет на обеих ВМ, скорее всего проблема была в пробросе портов изначально (затем в дальнейших лабораторных я это скорректировала).
   Поэтому в дальнейшем у клонированной ВМ ip-адрес станет 10.0.2.11
   
   б) Потом пользователь не хотел выполнять какие-либо действия с системой, поэтому было решено снести всю ВМ и проделать предыдущие шаги заново.
   Итог: мы наконец-то добились подключения по пользователю runner с ВМ 10.0.2.10 на клонированную уже 10.0.2.11
   
   <img width="887" height="619" alt="image" src="https://github.com/user-attachments/assets/90d632bc-5a09-4f41-856e-a1ac838e63c3" />

4. Установка ansible и проверка версии
   
   <img width="852" height="315" alt="image" src="https://github.com/user-attachments/assets/80237ce7-20fa-40fd-a931-1ca1ec4b3a24" />

5. На основной машине выполняем заготовки для плейбука и файл inventory.ini, содержащий адрес, к которому будем обращаться как к web-серверу
   
    <img width="522" height="110" alt="image" src="https://github.com/user-attachments/assets/6abd232f-ba94-41d5-ac56-9e9d5c9f6716" />

    <img width="618" height="165" alt="image" src="https://github.com/user-attachments/assets/dd5b6fc7-7dbd-41c7-9318-5d24a41d7c7c" />
    
    Сам плейбук с подключением пользователем runner

    <img width="563" height="387" alt="image" src="https://github.com/user-attachments/assets/d4a7e1b5-d671-40c8-8c41-b157b11035ec" />

6. Тестовый и "боевой" прогоны плейбука

    <img width="823" height="326" alt="image" src="https://github.com/user-attachments/assets/0ac99a4c-2fcd-4814-bff4-812a56e27a81" />

    <img width="827" height="309" alt="image" src="https://github.com/user-attachments/assets/6544c392-f754-429e-a8cf-011da4a4fcbd" />

7. Заготовка файла index.html

    <img width="524" height="191" alt="image" src="https://github.com/user-attachments/assets/ef468b1f-a290-4207-85ec-c62f498c9f20" />

8. Дописываем плейбук и прогоняем его

   <img width="547" height="534" alt="image" src="https://github.com/user-attachments/assets/d32268bc-1a4a-4e33-bddf-deb260c7f889" />
   
   <img width="818" height="370" alt="image" src="https://github.com/user-attachments/assets/239d2490-8970-44f4-8f78-4a5d8691fb1e" />

9. Обращаемся к curl и к новому web-серверу

    <img width="574" height="144" alt="image" src="https://github.com/user-attachments/assets/ed1076d1-83ad-4066-8c5d-783714b7c25e" />

    <img width="686" height="332" alt="image" src="https://github.com/user-attachments/assets/8a956517-0c70-4c70-9e70-6243f2f0b151" />

   
   
