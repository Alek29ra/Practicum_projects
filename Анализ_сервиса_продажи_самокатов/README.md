# Анализ сервиса продажи самокатов
В данных содержится информация о пользователях из нескольких городов, а также об их поездках.
Чтобы совершать поездки по городу, пользователи сервиса GoFast пользуются мобильным приложением. Сервисом можно пользоваться:
- без подписки
 - абонентская плата отсутствует;
 - стоимость одной минуты поездки — 8 рублей;
 - стоимость старта (начала поездки) — 50 рублей;
- с подпиской Ultra
 - абонентская плата — 199 рублей в месяц;
 - стоимость одной минуты поездки — 6 рублей;
 - стоимость старта — бесплатно.

**Цель:** Проанализировать данные и проверить некоторые гипотезы.

**Этапы:**
 - Загрузка файлов и считывание данных.
 - Проверка данных на наличие несоответствия типов данных и дубликатов.
 - Описание и визуализация информации о поездках
 - Обьединение датафреймов
 - Подсчет выручки
 - Проверка гипотез
 - Общий вывод

**Описание данных**

В основных данных есть информация о пользователях, их поездках и подписках.

Пользователи — users_go.csv:
 * user_id - уникальный идентификатор пользователя
 * name - имя пользователя
 * age - возраст
 * city - город
 * subscription_type - тип подписки (free, ultra)
 
Поездки — rides_go.csv:
 * user_id - уникальный идентификатор пользователя
 * distance - расстояние, которое пользователь проехал в текущей сессии (в метрах)
 * duration - продолжительность сессии (в минутах) — время с того момента, как пользователь нажал кнопку «Начать поездку» до момента, как он нажал кнопку «Завершить поездку»
 * date - дата совершения поездки

Подписки — subscriptions_go.csv:
 * subscription_type - тип подписки
 * minute_price - стоимость одной минуты поездки по данной подписке
 * start_ride_price - стоимость начала поездки
 * subscription_fee - стоимость ежемесячного платежа
