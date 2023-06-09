Отток клиентов
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.
Необходимо спрогнозировать, уйдёт клиент из банка в ближайшее время или нет.
Нам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.
Наша задача построить модель с предельно большим значением F1-меры, но не ниже 0.59 на тестовой выборке.
Дополнительно необходимо измерить AUC-ROC, сравнивая её значение с F1-мерой.
Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

В рамках проекта:
- на этапе подготовки данных удалены нерелевантные признаки и часть объектов с пропусками,
- перед обучением моделей выполнено прямое кодирование категориальных признаков и масштабирование числовых признаков,
- для решения задачи применено несколько моделей (логистической регрессии, на основе решающего дерева и на основе случайного леса), а также различные способы борьбы с дисбалансом классов (взвешивание классов, уменьшение выборки, увеличение выборки),
- при выборе наилучшей модели дополнительно определялась метрика AUC-ROC,
- для наилучшей модели построена ROC-кривая,
- удалось добиться целевого значения метрики качества F1-мера на тестовой выборке (достигнутое значение 0,6),
- выполнено сравнение выбранной модели с константной. Показатель качества F1-мера константной модели (0,32) существенно ниже, чем у выбранной модели,
- полученная модель на тестовой выборке корректно определила более 64% клиентов на отток.