@startuml order

autonumber
Actor "Заказчик" as Customer order 10
queue "Руководитель проекта" as Project.manager order 20
participant "Руководитель команды" as Team.lead order 30
participant "Технический писатель" as Technical.writer order 40
 
Customer -> Project.manager: Постановка требуемой задачи
Project.manager -> Team.lead: Передача в команду разработки
Team.lead -> Technical.writer: Делигирование задачи на исполнителя
Technical.writer -> Technical.writer: Инициализация задачи
Technical.writer -> Technical.writer: Планирование необходимых шагов для разработки пакета документов
Technical.writer -> Technical.writer: Написание документов
Technical.writer -> Team.lead: Передача на контроль качества (публикация версии на сервер)
Team.lead -> Technical.writer: Отправка на внесение изменений
Technical.writer -> Customer: Согласование пакета документов
@enduml
