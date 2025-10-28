---
title: Создание ПН - TimeLiner
description: 
published: true
date: 2025-09-21T12:25:53.978Z
tags: 
editor: markdown
dateCreated: 2025-06-27T11:34:46.147Z
---

### **TimeLiner**

Инструмент по данным из стандартного TimeLiner Navisworks разбивает модель на элементы до и после выбранной даты, создавая поисковые наборы Before, After и Null. Благодаря этому можно посмотреть, какие элементы должны быть уже выполнены по плану на выбранную дату, и какие элементы по плану предстоит выполнить. Также инструмент создает поисковые наборы Planned по данным вкладки “Планируемое завершение” из стандартного TimeLiner Navisworks, благодаря чему данную модель можно подгрузить в карточки “План-Факт” модуля DASHBOARD как модель с плановыми работами.

1\. Нажмите на вкладке SIGNAL PRO на панели Создание ПН ➤ TimeLiner

![image-1684485091353.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeFEqU30KYs5oP0F9Lq6qhPjkbBhKg4ovL2s055J8OewUMHsIqdTp6L8aiRI7UYB70sKE3BonPPmDTrd8HJTEwQTE0G5QSKh9czbcRxRHIBQ6I1O3z7mlN-r9CK8iy0jwPXznCF8P_7dkEV5kUL?key=mI66xCFlfAM6WWW1dluW4A)

2\. Выберите дату

![image-1684485104374.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXCIzIS_C-S3SpN2yw_ZpYABIzw-KYkHWAhrLg4rUaoVDHXtY99WuvMpKXFMML2P_tBF4uYaLNXJp9cNGnXaTdThp3k5L2zPL5goaozD-PDw7xvozqKMfkpI7TrcxQw2RuR2dynAcg4pbiI-c4lw?key=mI66xCFlfAM6WWW1dluW4A)

3\. Во всех элементах модели в свойствах во вкладке “SIGNAL” будет создано свойство TimeLiner с одним из значений before (элемент выполнен до выбранной даты), after (элемент будет выполнен после выбранной даты) или null (элемент не содержит информации, когда он будет выполнен). По этому свойству в панели “Наборы” будут созданы соответствующие поисковые наборы со значениями before, after и null.

![image-1689239072260.png](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdEIsKLudyojJUchRVlwMzh-unSTzWvppV_8plzmPZeFVpAdp7tnc1NJqkb5I7UJTDAce183aQ_3SYNdVirfhfgwiA-NjJ4qlCRAp53JXFlCwBYnTY5blhUSRoL_3f5DD1ZzBcvUURGPgsqVOdx9w?key=mI66xCFlfAM6WWW1dluW4A)

Также в элементах во вкладке “SIGNAL” будет создано свойство Planned. По этому свойству в панели “Наборы” будут созданы соответствующие поисковые наборы с плановыми датами. Данную модель можно будет использовать как плановую модель для карточек [_“План-Факт”_](https://wiki.sgnl.pro/app/page/1ErP71qjy4Y9wAoVm4zRSbJFNPTNxMfsCQDs24KN-kWw) модуля DASHBOARD.