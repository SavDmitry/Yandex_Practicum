# Анализ поведения пользователей мобильного приложения

**Описание задачи**

В данной работе представлены результаты проведения А/А/В-теста пользователей мобильного приложения для продажи продуктов питания за период с 25 июля по 7 августа 2019 года. Тестирование проводилось для оценки изменений, связанных с изменением шрифта в приложении. Пользователи были разделены на три группы: 246 и 247 — контрольные группы со старым шрифтом в приложении, а 248 — экспериментальная группа с новым шрифтом в приложении.
***
**План работы**

1. Предобработка данных
- переименование столбцов
- поиск явных/неявных дубликатов
- добавление новых столбцов

2. Изучение и проверка данных

3. Изучение воронки событий

4. Изучение результатов эксперимента

- Расчёт статистической значимости различий в конверсии пользователей между 2 контрольными группами со старыми шрифтами
- Расчёт статистической значимости различий в конверсии пользователей между каждой контрольной группой со старыми шрифтами и группой с новыми шрифтами
- Расчёт статистической значимости различий в конверсии пользователей между объеденёнными контрольными группыми со старыми шрифтами и группой с новыми шрифтами
5. Подготовка общего вывода
***
**Описание данных**

logs_exp.csv - логи действий пользователей, где:
- EventName — название события
- DeviceIDHash — уникальный идентификатор пользователя
- EventTimestamp — время события
- ExpId — номер эксперимента: 246 и 247 — контрольные группы, а 248 — экспериментальная
***
**Навыки и инструменты**

A/B-тестирование, Python, Pandas, Matplotlib, Seaborn, Событийная аналитика, Продуктовые метрики, Plotly, Проверка статистичесих гипотез, Визуализация данных
***
# Общий вывод
В процессе предобработки данных были удалены дубликаты. Из датасета было удалено 0.2% данных. В датасете не было обнаружено пропусков. В таблице были добавлены столбцы с датой.
В датасете присутствуют 5 событий - MainScreenAppear, OffersScreenAppear, CartScreenAppear, PaymentScreenSuccessful, Tutorial. Наиболее популярным является MainScreenAppear, наименее популярным Tutorial
Было определено, что наибольшее количество пользователей теряется на шаге перехода с главной страницы на страницу с предложениями. От первого события до оплаты примерно половина пользователей
Оценка результатов А/А/В-теста

При расчёте статистической значимости было определено, что нет оснований считать контрольные группы разными.
Нет статистически значимого различия по конверсии пользователей между объеденённой контрольной группой со старым шрифтом и группой с изменённым шрифтом.
Результаты теста не показали улучшение метрик (конверсия в целевые действия). Изменение шрифтов никак не повлияло на поведение пользователей.

**Рекомендации:**

Для увеличения конверсии в просмотр страницы с предложениями можно выполнить следующие действия:

1. Сделать кнопку с переходом на экран с предложениями более заметной
2. Добавить всплывающее окно, показывающее текущие акции и предложения
