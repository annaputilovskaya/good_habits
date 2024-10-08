**Задача:**

Реализовать бэкенд-часть SPA веб-приложения трекера полезных привычек (по мотивам книги "Атомные привычки" Джеймса Клира).
Добавить напоминания о времени выполнения полезных привычках в Telegram.

Данные проекта хранятся в БД PostgreSQL.

**Для запуска проекта:**

- клонируйте проект
- создайте файл .env по образцу. (Файл .env.sample)
- убедитесь, что на Вашем устройстве установлен Docker
- осуществите сборку образов и запуск контейнеров (docker compose up -d --build)

**Права доступа:**

Неавторизованным пользователям доступна регистрация и авторизация.

Зарегистрированный пользователь может создавать привычки, редактрировать, просматривать и удалять свои привычки.
Зарегистрированному пользователю доступен просмотр с постраничным выводом списка своих привычех и списка всех публичных привычек .

**Логика приложения:**

Привычки бывают полезными и приятными.
В книге пример полезной привычки описывается как конкретное действие, которое можно уложить в одно предложение:
Я буду [ДЕЙСТВИЕ] в [ВРЕМЯ] [МЕСТО].
За каждую полезную привычку рекомендуется себя чем-то поощрять.
В качестве поощрения может выступать вознаграждение или связанная приятная привычка, действие которой выполняется сразу после полезной привычки.
Применять в качестве поощрения одновременно и вознаграждение, и приятную привычку недопустимо.
Применять в качестве поощрения другую полезную привычку недопустимо.
У приятной привычки не може быть ни вознаграждения, ни другой связанной с ней приятной привычки.
Привычки не должны расходовать на выполнение больше двух минут.
Нельзя выполнять привычку реже, чем 1 раз в 7 дней.

Реализована работа с отложенными задачами для напоминания о том, в какое время полезные привычки необходимо выполнять.
Выполнена интегрирация с мессенджером Telegram, который занимается рассылкой уведомлений.

Настроен CORS, чтобы фронтенд мог подключаться к проекту на развернутом сервере.
