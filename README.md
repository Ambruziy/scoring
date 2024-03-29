# Прмер решения скоринговой задачи

Данные взяты из старого турнира от Тинькофф Банк
## Описание метрик
-  TCS_CUSTOMER_ID    Идентификатор клиента
+  BUREAU_CD          Код бюро, из которого получен счет
+  BKI_REQUEST_DATE 	 Дата, в которую был сделан запрос в бюро
+  CURRENCY	          Валюта договора (ISO буквенный код валюты)
+  RELATIONSHIP     	 Тип отношения к договору
  + 1 — Физическое лицо
  + 2 — Дополнительная карта/Авторизованный пользователь
  + 4 — Совместный
  + 5 — Поручитель
  + 9 — Юридическое лицо
+  OPEN_DATE	         Дата открытия договора
+  FINAL_PMT_DATE	    Дата финального платежа (плановая)
+  TYPE	              Код типа договора
  + 1 – Кредит на автомобиль
  + 4 – Лизинг
  + 6 – Ипотека
  + 7 – Кредитная карта
  + 9 – Потребительский кредит
  + 10 – Кредит на развитие бизнеса
  + 11 – Кредит на пополнение оборотных средств
  + 12 – Кредит на покупку оборудования
  + 13 – Кредит на строительство недвижимости
  + 14 – Кредит на покупку акций (например, маржинальное кредитование)
  + 99 – Другой
+ PMT_STRING_84M	     Дисциплина (своевременность) платежей. Строка составляется из кодов состояний счета на моменты передачи банком данных по счету в бюро, первый символ — состояние на дату PMT_STRING_START, далее последовательно в порядке убывания дат.
  + 0 – Новый, оценка невозможна
  + X – Нет информации
  + 1 – Оплата без просрочек
  + A – Просрочка от 1 до 29 дней
  + 2 – Просрочка от 30 до 59 дней
  + 3 – Просрочка от 60 до 89 дней
  + 4 – Просрочка от 90 до 119 дней
  + 5 – Просрочка более 120 дней
  + 7 – Регулярные консолидированные платежи
  + 8 – Погашение по кредиту с использованием залога
  + 9 – Безнадёжный долг/ передано на взыскание/ пропущенный платеж
+ STATUS	            Статус договора
  + 00 – Активный
  + 12 – Оплачен за счет обеспечения
  + 13 – Счет закрыт
  + 14 – Передан на обслуживание в другой банк
  + 21 – Спор
  + 52 – Просрочен
  + 61 – Проблемы с возвратом
+ OUTSTANDING   	    Оставшаяся непогашенная задолженность. Сумма в рублях по курсу ЦБ РФ
+ NEXT_PMT           Размер следующего платежа. Сумма в рублях по курсу ЦБ РФ
+ INF_CONFIRM_DATE	  Дата подтверждения информации по счету
+ FACT_CLOSE_DATE    Дата закрытия счета (фактическая)
+ TTL_DELQ_5         Количество просрочек до 5 дней
+ TTL_DELQ_5_29      Количество просрочек от 5 до 29 дней
+ TTL_DELQ_30_59     Количество просрочек от 30 до 59 дней
+ TTL_DELQ_60_89     Количество просрочек от 60 до 89 дней
+ TTL_DELQ_30        Количество просрочек до 30 дней
+ TTL_DELQ_90_PLUS   Количество просрочек 90+ дней
+ PMT_FREQ           Код частоты платежей
  + 1 – Еженедельно
  + 2 – Раз в две недели
  + 3 – Ежемесячно
  + A — Раз в 2 месяца
  + 4 – Поквартально
  + B — Раз в 4 месяца
  + 5 – Раз в полгода
  + 6 — Ежегодно
  + 7 – Другое
+ CREDIT_LIMIT       Кредитный лимит. Сумма в рублях по курсу ЦБ РФ
+ DELQ_BALANCE       Текущая просроченная задолженность. Сумма в рублях по курсу ЦБ РФ
+ MAX_DELQ_BALANCE   Максимальный объем просроченной задолженности. Сумма в рублях по курсу ЦБ РФ
+ CURRENT_DELQ       Текущее количество дней просрочки
+ PMT_STRING_START   Дата начала строки PMT_STRING_84M
+ INTEREST_RATE      Процентная ставка по кредиту
+ CURR_BALANCE_AMT   Общая выплаченная сумма, включая сумму основного долга, проценты, пени и штрафы. Сумма в рублях по курсу ЦБ РФ
