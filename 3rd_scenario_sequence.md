## Code

```
@startuml

title "Отображение календаря занятий для пользователей"

actor Пользователь as User
entity "Системный календарь" as Calendar
boundary "Приложение" as GUI
entity Сервер as Backend



User -> GUI: Выбор пункта "экспорт"
GUI -> Backend: Запрос на получение ics-файла
Backend -> GUI: Сформированый ics-файл
GUI -> User: Уведомление о завершении загрузки
User -> Calendar: Открытие файла через календарь
Calendar -> Calendar: Добавление события


@enduml

```
