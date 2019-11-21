## Code

```
@startuml

title "Отображение календаря занятий для пользователей"

actor Пользователь as User
boundary "Приложение" as GUI
entity Сервер as Backend

User -> GUI: открытие меню и выбор календаря
GUI -> Backend:  Получение данных о всех занятях пользователя
Backend -> Backend: Обработка запроса
Backend -> GUI: Данные о занятиях
GUI -> GUI: Составление календаря
GUI -> User: Отображение календаря

@enduml
```
