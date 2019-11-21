## Code
```
@startuml

title "Получение уведомлений при изменении календаря"

entity Сервер as Backend
entity "Сервер уведомлений" as NotfBackend
boundary "Приложение" as GUI
actor Пользователь as User

Backend -> Backend:  Получение запроса на изменение события
Backend -> NotfBackend: Запрос на показ уведомления
NotfBackend -> GUI: Уведомление
GUI -> User: Отображение уведомления


@enduml
```
