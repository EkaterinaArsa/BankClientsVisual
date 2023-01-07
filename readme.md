# Проект 1. Анализ  и визуализация данных по уходящим и лояльным клиентам банка

## Оглавление
[1. Описание проекта](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

[2. Какой кейс решаем?](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

[3. Краткая информация о данных](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

[4. Этапы работы над проектом](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

[5. Результат](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

[6. Выводы](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

### Описание проекта
На основе использования метода визуализации результатов анализа данных об оттоке клиентов некоторого банка нужно установить, чем ушедшие клиенты отличаются от лояльных и как между собой связаны различные признаки, определяющие клиентов. 

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)


### Какой кейс решаем?
Нужно написать программу, которая анализирует данных об оттоке клиентов некоторого банка и обеспечевает наглядную визуализацию, позволяющую установить, чем ушедшие клиенты отличаются от лояльных и как между собой связаны различные признаки, определяющие клиентов. 

**Условия выполнения**
- Анализ происходит по заданному алгоритму, формулирующему задачи.
- Выбор метода визуализации и формулировка выводов - персональная (индивидуальная) работа.

**Метрика качества**
Выбор метода визуализации должен быть максимально информативным для решения поставленной задачи, выводы - убедительны и основаны на результатах визуализации.

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

### Краткая информация о данных

**Признаки, имеющиеся в заданном DataFrame**
- RowNumber — номер строки таблицы (это лишняя информация, поэтому можете сразу от неё избавиться
- CustomerId — идентификатор клиента
- Surname — фамилия клиента
- CreditScore — кредитный рейтинг клиента (чем он выше, тем больше клиент брал кредитов и возвращал их)
- Geography — страна клиента (банк международный)
- Gender — пол клиента
- Age — возраст клиента
- Tenure — сколько лет клиент пользуется услугами банка
- Balance — баланс на счетах клиента в банке
- NumOfProducts — количество услуг банка, которые приобрёл клиент
- HasCrCard — есть ли у клиента кредитная карта (1 — да, 0 — нет)
- IsActiveMember — есть ли у клиента статус активного клиента банка (1 — да, 0 — нет)
- EstimatedSalary — предполагаемая заработная плата клиента
- Exited — статус лояльности (1 — ушедший клиент, 0 — лояльный клиент)

Для визуализации в проекте преимущественно использованы plotly.express и seaborn

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)


### Этапы работы над проектом

* На первом этапе преобразуем данные DataFrame в удобный формат и создадим несколько "удобных" признаков

* На втором этапе проводились выбор метода визуализации, его реализация и оценка результата в соответствии с поставлененными задачами: 

1. Определить соотношение ушедших и лояльных клиентов.
2. Оценить распределение баланса пользователей, у которых на счету больше 2 500 долларов.
3. Оценить расределение баланса клиента в разрезе признака оттока. 
4. Оценить расределение возраста клиентов в разрезе признака оттока.
5. Определить взаимосвязь кредитного рейтинга клиента и его предполагаемой зарплаты.
6. Определить, кто чаще уходит, мужчины или женщины.
7. Определить, как отток клиентов зависит от числа приобретённых у банка услуг.
8. Определить, как влияет наличие статуса активного клиента на отток клиентов.
9. Определить, в какой стране доля ушедших клиентов больше.
10. Оценить степень оттока клиентов по уровню их кредитного рейтинга


:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)


### Результат

Для решения поставленных задач реализовано 16 графиков различного типа (круговые, столбчатые, иерархические диаграммы, гистограммы, "коробки с усами", тепловые карты, тепловая картограмма)

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

### Выводы

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B01.png> </center>
1. Количество ушедших клиентов чуть более 20%.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%202.1.png> </center>
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%202.2.png> </center>
2. Распределение баланса клиентов похоже на нормальное. Сумма вклада среди клиентов (со вкладом более 2500 долларов) преимущественно в пределах 100000-140000 долларов.  Среднее значение составляет около 120000 (медиана=119839). Максимальный вклад составил порядка 251000 долларов.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%203.1.png> </center>
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%203.2.png> </center>
3. Наблюдается большое смещение лояльных клиентов к нулевому балансу, это вызвано большим количеством клиентов с нулевым балансом. Стоит отдельно рассмотреть клиентов с нулевым балансом. Также, судя по разбросу значений баланса и уровню медианы, среди ушедших клиентов уровень баланса был выше. Данный аспект может указывать на менее "приятные" и выгодные условия для крупных вкладов, чем для вкладов с небольшим уровнем средств. В то же время, превалирование среди лояльных и не лояльных клиентов лиц с балансом до 10000 не позволяет однозначно сказать о лучших условиях для лиц с по небольшим вкладам.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%204.1.png> </center>
4. Cреди ушедших клиентов большинство люди старше 40 лет (38-51 год, медиана = 45), среди лояльных большинство - лица молодого возраста(30-40 лет, медиана - 36). В группе лояльных клиентов наблюдаются потенциальные выбросы среди лиц - старше 56 лет. Следовательно, для уменьшения оттока клиентов банку необходимо сконцентрировать внимание на лицах среднего и старшего возраста.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%205.1.png> </center>
5. Не отмечается прямой зависимости кредитного рейтинга клиента и его предполагаемой зарплаты. Зависимости кредитного рейтинга клиента от степени его лояльности не наблюдается. Следует отметить, что только у ушедших клиентов есть рейтинг ниже 400.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%206.1.png> </center>
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%206.2.png> </center>
6. Среди клиентов банка женщин меньше, чем мужчин, но они чаще становятся нелояльными клиентам, в среднем на 9%. Следует отметить, что среди ушедших клиентов женщин в 1.5 раза больше чем мужчин.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%207.1.png> </center>
7. Количество ушедших клиентов обратно пропорционально количеству услуг приобретенных клиентом у банка. Самое большое количество ушедших клиентов воспользовались только одним продуктом банка. Довольно печальная картина с клиентами, которые воспользовались 3 и 4 продуктами, там доля ушедших клиентов намного превышает лояльных, а с 4-мя продуктами так вообще составляет 100%.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%208.1.png> </center>
8. Среди неактивных клиентов, чаще встречаются нелояльные (ушедшие), чем среди активных. Следовательно, для уменьшения оттока, необходимо  повышать активность клиентов.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%209.1.png> </center>
9. Высокого отток клиентов наблюдается во Франции и Германии. С учетом ранее полученных данных, для вывода о вероятных причинах  необходимо уточнить возрастной и половой состав клиентской базы в данных странах, степень их активности и количество приобретенных ими услуг. И, в тоже время, возможны причины, данных о которых нам не предоставленно (политическая и экономическая ситуация в стране), поэтому хорошо бы увидеть картину по данным страннам в других банках.

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%2010.1.png> </center><center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%2010.2.png> </center><center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%2010.3.png> </center>
10. Наибольший отток наблюдается среди клиентов с минимальным кредитным рейтингом ('Very_Poor', брали и возвращали мало кредитов), и длительностью пользования услугами банка менее 1 года и 10 лет.Если не учитывать клиентов с нулевым балансом, то среди клиентов с отличным ("Exelent")кредитным рейтингом и длительностью пользования услугами банка до года, 6 лет и более 9 лет также наблюдается достаточно высокий отток.

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)