# -Data_analysis_Advertisements
Даны данные взаимодействий с рекламными объявлениями на некоторой площадке за 6 дней, а также таблица с характеристиками рекламных клиентов (тех, кто разместил эти объявления).

### Описание данных
ads_clients_data.csv – характеристики рекламных клиентов date – дата client_union_id – id рекламного кабинета community_id – id сообщества create_date – дата создания рекламного клиента

ads_data.rar (необходимо разархивировать) – данные взаимодействий с рекламными объявлениями date – дата time – время event – действие (просмотр/клик) platform – платформа ad_id – id объявления client_union_id – id рекламного кабинета campaign_union_id – id рекламной кампании ad_cost_type – тип оплаты ad_cost – цена has_video – есть ли видео target_audience_count – размер аудитории

### Необходимо провести анализ данных по следующим вопросам:
1.Посчитать среднее количество показов и среднее количество кликов на объявления за весь период
2.Нарисовать график распределения показов на объявление за весь период
3.Посчитать скользящее среднее показов с окном 2
4. Определить в какой день наблюдается наибольшая разница по модулю между арифметическим средним и скользящим средним
5. Найти среднее количество дней от даты создания рекламного клиента и первым запуском рекламного объявления этим клиентом
6. Вычислить конверсию из создания рекламного клиента в запуск первой рекламы в течение не более 365 дней
7. Разбить клиентов по промежуткам от создания рекламного кабинета до запуска первого рекламного объявления
8. Построить интерактивный барплот категорий с количеством уникальных клиентов в них
### Выводы:
1. Для разных типов контекстной рекламы, собственно как и для разных вариантов размещения, нормальная кликабельность может отличаться. Этот показатель также зависит и от ниши, уровня конкуренции, времени показов, дней недели, сезонности и т.д. Для текущих данных CTR=12%, что является хорошим показателем.
2. Часто по данных показов по объявлениям встречается следующая картина: много объявлений с малым количеством просмотров, и единичные объявления с большим количеством просмотров. Чтобы понять форму графика распределения числа показов применяется логарифмирование данных.
3. Часто для поиска аномалий в данных используется скользящее среднее. При нанесении на один график значения просто среднего количества показов по дням и скользящего среднего можно определить дни, в которые наблюдается наибольшая разница между этими двумя показателями.
![2023-02-01_22-58-50](https://user-images.githubusercontent.com/122619433/216150233-4603a960-1463-428c-9afb-e4f601538088.png)
4. Среднее количество дней от даты создания рекламного клиента и первым запуском рекламного объявления этим клиентом составляет 124 дня, что говорит о возможных проблемах у клиентов с работой кабинета
5. Конверсия из создания рекламного клиента в запуск первой рекламы равна 0.69%. Показатель меньше 1% свидетельствует о проблемах в работе личного кабинета либо оплат.
6. При сегментировании клиентов по периодам от создания рекламного кабинета до запуска первого рекламного объявления видим, что большинство клиентов запускает первую рекламу на 3-6 месяц.
![2023-02-01_22-55-12](https://user-images.githubusercontent.com/122619433/216149513-e24b5044-9787-482c-a444-19190262a9a3.png)
