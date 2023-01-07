# Проект 1. Анализ  и визуализация данных по уходящим и лояльным клиентам банка

## Оглавление
[1. Описание проекта](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)

[2. Какой кейс решаем?](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BA%D0%B0%D0%BA%D0%BE%D0%B9-%D0%BA%D0%B5%D0%B9%D1%81-%D1%80%D0%B5%D1%88%D0%B0%D0%B5%D0%BC)

[3. Краткая информация о данных](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BA%D1%80%D0%B0%D1%82%D0%BA%D0%B0%D1%8F-%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D1%8F-%D0%BE-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)

[4. Этапы работы над проектом](https://github.com/EkaterinaArsa/BankClientsVisual#%D1%8D%D1%82%D0%B0%D0%BF%D1%8B-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B-%D0%BD%D0%B0%D0%B4-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%BE%D0%BC)

[5. Результаты и предварительные выводы](https://github.com/EkaterinaArsa/BankClientsVisual#%D1%80%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82)

[6. Общий вывод](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4%D1%8B)

### Описание проекта
На основе использования метода визуализации результатов анализа данных об оттоке клиентов некоторого банка нужно установить, чем ушедшие клиенты отличаются от лояльных и как между собой связаны различные признаки, определяющие клиентов. 

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)


### Какой кейс решаем?
Нужно написать программу, которая анализирует данных об оттоке клиентов некоторого банка и обеспечевает наглядную визуализацию, позволяющую установить, чем ушедшие клиенты отличаются от лояльных и как между собой связаны различные признаки, определяющие клиентов. 

**Условия выполнения**
- Анализ происходит по заданному алгоритму, формулирующему задачи.
- Выбор метода визуализации и формулировка выводов - персональная (индивидуальная) работа.

**Метрика качества**
Выбор метода визуализации должен быть максимально информативным для решения поставленной задачи, выводы - убедительны и основаны на результатах визуализации.

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)

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

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)


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


:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)


### Результаты и предварительные выводы
<strong> 1 этап. Провели преобразование данных и импорт необходимых библиотек </strong>

```
import seaborn as sns
import plotly.express as px
import pandas as pd

churn_data = pd.read_csv('data/churn.csv')
# для преобразований используем копию исходной таблицы
client_df = churn_data.copy()

# преобразуем числовые признаки в категориальные и создадим таблицу с указанным значением 
# по лояльным/ушедшим  и активным/неактивным клиентам (для удобства постоения диаграмм)
client_df.loc[(client_df['Exited'] == 0), 'Exited_type'] =  'лояльные клиенты'
client_df.loc[(client_df['Exited'] == 1), 'Exited_type'] = 'ушедшие клиенты'
client_df.loc[(client_df['IsActiveMember'] == 1), 'IsActiveMember_type'] = 'активные клиенты'
client_df.loc[(client_df['IsActiveMember'] == 0), 'IsActiveMember_type'] = 'неактивные клиенты'
```

<strong>2 этап. Для решения поставленных задач реализовано 16 графиков различного типа (круговые, столбчатые, иерархические диаграммы, гистограммы, "коробки с усами", тепловые карты, тепловая картограмма)</strong> [код](https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/clients_of_bank_HW.ipynb)

1. Определить соотношение ушедших и лояльных клиентов.

```
exited_df = client_df['Exited_type'].value_counts()

fig = px.pie(data_frame=exited_df, 
             values=exited_df.values, 
             names=exited_df.index, 
             title='Соотношение ушедших и лояльных клиентов')

fig.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B01.png> </center>

### Вывод: Количество ушедших клиентов чуть более 20%.

2. Оценить распределение баланса пользователей, у которых на счету больше 2 500 долларов.
```
balance_box = client_df[client_df['Balance'] > 2500]
box = px.box(data_frame=balance_box,
             x='Balance',
             height=400,
             width=1000,
             title='Распределение баланса клиентов (при балансе более 2500 долларов)')

# для изучения распределения постороим гистограмму
hist = px.histogram(data_frame=balance_box,
                    x='Balance',
                    height=400,
                    width=1000,
                    title='Распределение баланса клиентов (при балансе более 2500 долларов)')

box.show()
hist.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%202.1.png> </center>
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%202.2.png> </center>

### Вывод: Распределение баланса клиентов похоже на нормальное. Сумма вклада среди клиентов (со вкладом более 2500 долларов) преимущественно в пределах 100000-140000 долларов.  Среднее значение составляет около 120000 (медиана=119839). Максимальный вклад составил порядка 251000 долларов.

3. Оценить расределение баланса клиента в разрезе признака оттока. 
```
box_exited = px.box(data_frame=client_df,
                    y='Exited_type',
                    x='Balance',
                    color='Exited',
                    width=1000,
                    height=400,
                    title='Распределение баланса среди ушедших и лояльных клиентов'
)

box_exited.show()

```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%203.1.png> </center>

```
# добавим гистограмму по лояльным клиентам (посмотрим рапределение в районе нулевого баланса)
hist_balance = px.histogram(data_frame=client_df,
                            x='Balance',
                            color='Exited_type',
                            nbins=25,
                            width=800,
                            height=400,
                            title='Распределение баланса среди ушедших и лояльных клипентов'
)

hist_balance.update_layout(barmode = 'group') 
hist_balance.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%203.2.png> </center>

### Выводд: Наблюдается большое смещение лояльных клиентов к нулевому балансу, это вызвано большим количеством клиентов с нулевым балансом. Стоит отдельно рассмотреть клиентов с нулевым балансом. Также, судя по разбросу значений баланса и уровню медианы, среди ушедших клиентов уровень баланса был выше. Данный аспект может указывать на менее "приятные" и выгодные условия для крупных вкладов, чем для вкладов с небольшим уровнем средств. В то же время, превалирование среди лояльных и не лояльных клиентов лиц с балансом до 10000 не позволяет однозначно сказать о лучших условиях для лиц с по небольшим вкладам.


4. Оценить расределение возраста клиентов в разрезе признака оттока.
```
box_exited_age = px.box(data_frame=client_df,
                    y='Exited_type',
                    x='Age',
                    width=900,
                    height=400,
                    title='Возрастной состав среди ушедших и лояльных клипентов'
)

box_exited_age.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%204.1.png> </center>


### Вывод: Cреди ушедших клиентов большинство люди старше 40 лет (38-51 год, медиана = 45), среди лояльных большинство - лица молодого возраста(30-40 лет, медиана - 36). В группе лояльных клиентов наблюдаются потенциальные выбросы среди лиц - старше 56 лет. Следовательно, для уменьшения оттока клиентов банку необходимо сконцентрировать внимание на лицах среднего и старшего возраста.

5. Определить взаимосвязь кредитного рейтинга клиента и его предполагаемой зарплаты.
```
scatter_reiting = px.scatter(data_frame=client_df,
                    y='CreditScore',
                    x='EstimatedSalary',
                    color='Exited_type',
                    width=800,
                    height=400,
                    title='Зависимость кредитного рейтинга клиентов от их предполагаемой зарплаты'
)

scatter_reiting.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%205.1.png> </center>

### Вывод: Не отмечается прямой зависимости кредитного рейтинга клиента и его предполагаемой зарплаты. Зависимости кредитного рейтинга клиента от степени его лояльности не наблюдается. Следует отметить, что только у ушедших клиентов есть рейтинг ниже 400.

6. Определить, кто чаще уходит, мужчины или женщины.
```
gender_exited = client_df.groupby(by ='Gender')['Exited'].mean().round(2) * 100

bar_gender_exited = px.bar(data_frame=gender_exited,
                 x=gender_exited.values,
                 color=gender_exited.index,
                 height=500,
                 width=800,
                 title='Количество нелояльных(ушедших) клиентов в разных гендерных группах (в %)'
)
bar_gender_exited.show()

```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%206.1.png> </center>

``` 
# дополним информацию по гендерному составу среди ушедших клиентов
pie_gend = px.pie(data_frame=gender_exited, 
             values=gender_exited.values, 
             names=gender_exited.index, 
             title='Гендерный состав в группе ушедших клиентов')

pie_gend.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%206.2.png> </center>

```
treemap_gender_exit = px.treemap(data_frame=client_df,
                                path=['Gender', 'Exited_type'],
                                height=500,
                                width=800,
                                title ='Соотношение ушедших и лояльных клиентов по гендерному признаку'
)

treemap_gender_exit.show()
```

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%206.3.png> </center>

### Вывод: Среди клиентов банка женщин меньше, чем мужчин, но они чаще становятся нелояльными клиентам, в среднем на 9%. Следует отметить, что среди ушедших клиентов женщин в 1.5 раза больше чем мужчин.

 
7. Определить, как отток клиентов зависит от числа приобретённых у банка услуг.
```
exite_num_bar = client_df.groupby(['NumOfProducts','Exited_type'], 
                                         as_index=False).count()[['NumOfProducts','Exited_type','RowNumber']]
bar_num = px.bar(data_frame=exite_num_bar,
                 x='NumOfProducts',
                 y='RowNumber',
                 color='Exited_type',
                 height=500,
                 width=800,
                 title='Зависимость уровня оттока клиентов от числа приобретенных услуг'
)
bar_num.update_layout(barmode = 'group') 
bar_num.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%207.1.png> </center>

### Вывод: Количество ушедших клиентов обратно пропорционально количеству услуг приобретенных клиентом у банка. Самое большое количество ушедших клиентов воспользовались только одним продуктом банка. Но, при изучении отдельно по группам, складывается довольно печальная картина с клиентами, которые воспользовались 3 и 4 продуктами, там доля ушедших клиентов намного превышает лояльных, а с 4-мя продуктами так вообще составляет 100%.

8. Определить, как влияет наличие статуса активного клиента на отток клиентов.
```
# Создадим DataFrame со статусом активные и неактивные клиенты, для диаграм

activ_exit_df= client_df.groupby(by=['Exited_type', 'IsActiveMember_type'], 
                                 as_index=False).count()[['IsActiveMember_type','Exited_type','RowNumber']]
treemap_activ_exit = px.treemap(data_frame=activ_exit_df,
                                path=['IsActiveMember_type', 'Exited_type'],
                                values='RowNumber',
                                height=500,
                                width=800
)

treemap_activ_exit.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%208.1.png> </center>

### Вывод: Среди неактивных клиентов, чаще встречаются нелояльные (ушедшие), чем среди активных. Следовательно, для уменьшения оттока, необходимо  повышать активность клиентов.

9. Определить, в какой стране доля ушедших клиентов больше.
```
# создали две таблицы: в первой подсчитали значения количество клиентов из страны, 
# во второй - количество лояльных и не лояльных клиентов в стране
country_df = client_df.groupby(by='Geography', as_index=False)['Exited'].mean()
country_exited_df = client_df.groupby(by=['Geography','Exited'], as_index=False)['Exited'].mean()
country_exited_df['Exited_type'] = client_df['Exited_type']

# для подсчета процентного значени объединили их в одну таблицу
country_exited_df = country_exited_df.merge(country_df,on='Geography', how= 'left')

# подсчитали процент
country_exited_df['Exited_perc'] = country_exited_df['Exited_x']/country_exited_df['Exited_y'] * 100

# выделили информацию только по ушедшим клиентам
country_exited = country_exited_df[country_exited_df['Exited_type']=='ушедшие клиенты']

choropleth_country = px.choropleth(data_frame=country_exited,
              locations='Geography',
              color='Exited_perc',
              locationmode='country names',
              scope='europe',
              width=800,
              height=500,
              title='Показатель нелояльности (доля ушедших) клиентов по странам (в процентах)'
              )
choropleth_country.show()
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%209.1.png> </center>

### Вывод: Высокого отток клиентов наблюдается во Франции и Германии. С учетом ранее полученных данных, для вывода о вероятных причинах  необходимо уточнить возрастной и половой состав клиентской базы в данных странах, степень их активности и количество приобретенных ими услуг. И, в тоже время, возможны причины, данных о которых нам не предоставленно (политическая и экономическая ситуация в стране), поэтому хорошо бы увидеть картину по данным страннам в других банках.

10. Оценить степень оттока клиентов по уровню их кредитного рейтинга
```
# Построим сводную таблицу, строками которой являются категории кредитного рейтинга 
# (CreditScoreCat), а столбцами — количество лет, в течение которых клиент пользуется услугами 
# банка (Tenure). В ячейках сводной таблицы должно находиться среднее по признаку оттока (Exited)

def get_credit_score_cat(credit_score):
    if credit_score >= 300 and credit_score < 500:
        return "Very_Poor"
    elif credit_score >= 500 and credit_score < 601:
        return "Poor"
    elif credit_score >= 601 and credit_score < 661:
        return "Fair"
    elif credit_score >= 661 and credit_score < 781:
        return "Good"
    elif credit_score >= 781 and credit_score < 851:
        return "Excellent"
    elif credit_score >= 851:
        return "Top"
    elif credit_score < 300:
        return "Deep"
    
client_df['CreditScoreCat'] = client_df['CreditScore'].agg(func=get_credit_score_cat)

pivot_credit = client_df.pivot_table(values='Exited', index='CreditScoreCat', 
                                     columns='Tenure').round(3) * 100


heatmap_pivot_credit = sns.heatmap(data=pivot_credit,
                                   annot=True,
                                   cmap='YlGnBu')

display(pivot_credit)
```
<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%2010.1.png> </center>

```
# посмотрим на ту же таблицу корреляции, но без клиентов с нулевым балансом
client_df_no_null = client_df[client_df['Balance'] != 0].copy()
client_df_no_null['CreditScoreCat'] = client_df_no_null['CreditScore'].agg(func=get_credit_score_cat)

pivot_credit_no_null = client_df_no_null.pivot_table(values='Exited', index='CreditScoreCat', 
                                     columns='Tenure').round(3) * 100


heatmap_pivot_credit_no_null = sns.heatmap(data=pivot_credit_no_null,
                                   annot=True,
                                   cmap='YlGnBu')
```

<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%2010.2.png> </center>

```
# использование pyplot.express
fig = px.density_heatmap(data_frame=client_df,
                         x='Tenure',
                         y='CreditScoreCat',
                         z='Exited',
                         # порядок отображения категорий на графике
                         category_orders=dict(CreditScoreCat=['Excellent', 'Good','Fair', 'Poor', 
                                                              'Very_Poor']),
                         labels=dict(Tenure='Продолжительность сотрудничества с банком (годы)',
                                     CreditScoreCat='Кредитный рейтинг'), # названия осей
                         color_continuous_scale='blues',  # цветовая гамма
                         histfunc='avg',  # среднее по z
                         title="Тепловая карта оттока клиентов по категориям",
                         template='none',  # тема форматирования графика
                         width=800,
                         height=600)

fig.update_layout(autosize=False,  # автоматический размер откл.
                  xaxis_dtick=1,  # шаг тиков на оси x
                  # Настройка легенды (colorbar)
                  coloraxis_colorbar=dict(title=dict(text='Интенсивность оттока', side='bottom'),
                                          orientation='h',
                                          x=0.5,
                                          y=-0.4,
                                          tickformat='.0%',
                                          ypad=20,  # отступ снизу
                                          dtick=0.1) # шаг тиков
                  )

# Настройка шаблона наведения курсора мыши
fig.update_traces(hovertemplate="Отток %{z:.0%}")
fig.show()
```


<center> <img src=https://github.com/EkaterinaArsa/BankClientsVisual/blob/master/%D0%B4%D0%B8%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%2010.3.png> </center>

### Вывод: Наибольший отток наблюдается среди клиентов с минимальным кредитным рейтингом ('Very_Poor', брали и возвращали мало кредитов), и длительностью пользования услугами банка менее 1 года и 10 лет.Если не учитывать клиентов с нулевым балансом, то среди клиентов с отличным ("Exelent")кредитным рейтингом и длительностью пользования услугами банка до года, 6 лет и более 9 лет также наблюдается достаточно высокий отток.

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)

### Вывод

Количество ушедших клиентов чуть более 20%. Cреди ушедших клиентов большинство - женщины, старше 40 лет, неактивно пользующиеся услугами банка, с минимальным кредитным рейтингом (только у ушедших клиентов есть рейтинг ниже 400) и длительностью пользования услугами банка менее 1 года и 10 лет. Количество ушедших клиентов обратно пропорционально количеству услуг приобретенных клиентом у банка, в тоже время доля ушедших клиентов увеличивается при увеличении количества используемых услуг.

:arrow_up:[к оглавлению](https://github.com/EkaterinaArsa/BankClientsVisual#%D0%BE%D0%B3%D0%BB%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5)