# SSSL-PR-1 Rublev Vladimir Sergeevich
# BBMO-02-23

1. Создаем 2 виртуальные машины на базе ОС Debian 12 и обеспечиваем между ними сетевой обмен

   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/1.jpg)

   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/2.jpg)

   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/3%201.jpg)
   
2. Включаем на 1-ой (сервере) из ВМ передачу логов по протоколу rsyslog на 2-ую ВМ (клиент)
   
   **Устанавливаем и настраиваем rsyslog на сервере и клиенте**

   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/4%201.jpg)

   **Включаем UDP и TCP соединение**

   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/5%201.jpg)

   **Устанавливаем правила на сервере**
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/7%201.jpg)


   **Проверяем получения логов на сервере**
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/8.jpg)

   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/8%201.jpg)

3. Устанавливаем и настраиваем получение логов на сервере с использованием Loki
   
   **Установливаем и редактируем compose-файл на сервере**
 
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/11%201.png)
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/11%202.png)

   
   **Запускаем Loki**
 
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/12%201.png)
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/12%202.png)

   
   **Редактируем promtail на клиенте**
 
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/13%201.png)

   **Редактируем compose-файл для promtail**
 
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/13%202.png)
  
   **Запускаем promtail на клиенте**
 
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/14%201.png)

   **Просматриваем логи клиента в Grafana**
 
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/15%201.png)

   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/15%202.png)
 
 5. Устанавливаем и настроиваем получение логов на сервере с использованием Signoz

   _Установка Signoz по инструкции с сайта: https://signoz.io/docs/install/docker/#install-signoz-using-docker-compose_

   **Запускаем Signoz**
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/16%201.png)
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/16%202.jpg)
   
   
   **Редактируем конфигурации на клиенте для отправки данных в Signoz**
   
   _Установка приложения sample-nodejs-app согласно инструкции с сайта: https://github.com/SigNoz/sample-nodejs-app/_
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/17%201.png)
   
   **Проверяем получение логов в Signoz**
   
   ![image](https://github.com/vladimirrublev/ssslpr1/blob/main/screenshot/17%202.jpg)
   
