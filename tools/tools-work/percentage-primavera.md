---
title: Экспорт/Импорт - Процент Primavera
description: 
published: true
date: 2025-09-21T11:44:43.929Z
tags: 
editor: markdown
dateCreated: 2025-06-27T11:40:48.616Z
---

### **Процент Primavera**

Инструмент позволяет выгрузить процент выполнения работ в файл XML, изначально выгруженный из Primavera.

**Алгоритм использования:** экспортировав виды работ из Primavera в формате XML импортируете их в Tools for Navisworks командой “Импорт из Primavera” (см. [_Виды работ_](https://wiki.sgnl.pro/app/page/1dhz_RYu3DczaEesG4yRQP9sK60FLyuz8SEMJI7nmX-w)). Далее отмечаете через команды [_“Завершить/Принять”_](https://wiki.sgnl.pro/app/page/1zKM2m_O8NPfp5ETOf5NXd1MkKZfEhWvHyyJyEXGYUaM) даты выполнения работ. Теперь процент выполнения работ можно загрузить в тот же самый XML с помощью данной команды "Процент Primavera". И наконец, импортировать XML файл обратно в Primavera, чтобы наблюдать процент выполнения.

1\. Нажмите на вкладке SIGNAL PRO на панели Экспорт | Импорт ➤ Процент Primavera

![image-1688032533804.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcquNWaquIO7uokR6MRjGIKdfsg77MCq_BMu8Rmzj_5nhvwZRKjo3BlCPTWMqedVhW3wa0CZi3csylvQSnzr7FBT_NPdfN-CP4ABhOxJWQ1atppSrirJ5dN2geypu3GjBE2enHEjmQBmJMmaQz6Fw?key=LTk-Q5Atb8KI51pphss9TQ)

2\. Выберите статус работ и дату выполнения работ, и нажмите “ОК”.

![image-1683285550586.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXKjkeBwxQYcaIs-KYXcGg4YM-sz9zyqS3sucA3sLdCPx7Ie2vJ9GlaW6QeiIrZuKRYD9EKrEG-sn75wsudj3uNNcx7gVsdjBHRQWFxlUVsOAsHfeWfAQXW72RamkuwNqQK-RBl_enT09eBapGBQ?key=LTk-Q5Atb8KI51pphss9TQ)

-   Требуется, чтобы в панели “Наборы” был создан поисковый набор “Работы” с правильно заполненными условиями. Создать ПН можно с помощью инструмента [_“Работы”_](https://wiki.sgnl.pro/app/page/1-B8HMIqIDN4CnwWo3yZXYVBYlf7Lq4anPwmk5eLtGXw)

3\. Выберите файл формата XML, ранее выгруженный из Primavera и нажмите “Открыть”

![image-1683285577865.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeB0ZEfy5bSmTjPp5Crh3dc7GOnta7736AM2t7cWQLK2nTWzIGLfO0gJd01Zw_MCx1D87Dac8pjiAV01Eu00ryosmy2DaGmf7pHjvskY_Mg6JmXg-3aeVyphutPWopIU63XafguhoxoZeHvbSwW?key=LTk-Q5Atb8KI51pphss9TQ)

4\. Процент запишется в указанный XML файл. Теперь его можно загрузить обратно в Primavera.

![image-1683285562868.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdpMQ43D_aCGvICcX1N8K4OWmuyTjqbDUV-IwxcZ2bZQuTD-Nm6mUy8-QqMhZ6L9xT52SAZYVHvrOrRN2cBwpcPCLeZXviIlvextn_hPSjx8EgJp2yxGOysEp97jeQ5jEHY7gKfYx4-_hz8RX3Eow?key=LTk-Q5Atb8KI51pphss9TQ)