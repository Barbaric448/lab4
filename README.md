# Лабораторная работа №4

Я создал Dockerfile. Его содержание:
```
FROM ubuntu:latest
RUN apt-get update && apt-get install libaa-bin iputils-ping
```

Создал образ aafire-image:
```
docker build -t aafire-image .
```

Cоздал container1 и container2:
```
docker run -it --name container1 aafire-image
docker run -it --name container2 aafire-image
```

Запустил aafire в двух терминлах. Создал сеть и присоеденил к ней контейнеры. Проверил пинг между ними:
<img width="1278" alt="Снимок экрана 2024-11-22 в 16 45 15" src="https://github.com/user-attachments/assets/dde9b6fb-fd47-49b0-b643-776bddc72575">
<img width="1278" alt="Снимок экрана 2024-11-22 в 16 45 03" src="https://github.com/user-attachments/assets/c2583674-c5ae-4205-ad78-dd44da8b5fca">
