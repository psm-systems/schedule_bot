## schedule_bot
# Телеграмм бот. Отправляет опросы по расписанию, проверяет отпуска и дни рождения членов команды.

Бот реализован на библиотеке telebot

Дни рождения и отпуска вносятся в файл team.csv согласно шаблона

Бот запускается с помощью watchdog supervisor.

Необходимые библиотеки собраны в файле requirements.txt

# Установка
Установка осуществляется копированием репозитория

`https://github.com/psm-systems/schedule_bot`

и установкой всех зависимостей

`pip install -r requirements.txt`

Далее для корректной работы вашего телеграмм бота требуется заменить token в модуле telegram.py в качестве строки,
ID владельца бота, ID чата и ID треда чата, если он разделен на ветки. Если чат не разделен, то аргумент с тредом следует удалить.

Следующим шагом будет установка watchdog - Supervisor: A Process Control System. Supervisor полностью реализован на python3, поэтому не требует дополнительных программ и может быть установлен с помощь команды

`pip install supervisor`

Конфигурация находится в файле supervisor.conf. В ней необходимо поправить путь, имя пользователя и размер файла логирования.

Далее для запуска необходимо ввести команду

`supervisord -c supervisor.conf &`
