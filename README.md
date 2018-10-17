# Этот файл может содержать больше деталей в других ветках.
# Issues:
Задачи могут быть помечены метками, который определяют характер задачи и то как она должна выполняться

# Labels:
- Story - Задача на разработку функциональности
- Bug - задача на устранения несоответсвия реальной функциональности и заявленой функциональности в Story. В баге всегода указывается Story для которой заводиться этот баг.
- Controller - (MVC) Задача на разработку кода реализующий логику ПО
- Model - (MVC) Задача на разработку кода организуюший хранение данных
- View - (MVC) Задача на разработку кода реализующий графический интерфейс
- Functional test - Задача затрагивает функциональное тестирование
- Unit test - Задача затрагивает модульное тестирпование
- Auto test - Задача затрагивает автоматические тесты
- Regression - Выполнение тестовых сценариев
- Script - Задача на написание сценариев

# Projects:
Реализуют бизнес-модель.
- Code Development - Сюда попадают задачи на разработку функционала или исправления багов
- Code review - Сюда попадают новые запросы на pull request c предыдущего проекта
- Writing test scripts - Сюда попадают задачи на разработку сценариев тестирования
- Review test scenarios - Сюда попадают задачи на проверку тестовых сцериев, переносом с предыдущего проекта
- Writing automatic tests - Сюда попадают задачи на автоматизацию тестовых сценариев
- Review automatic tests - Сюда попадают задачи на проверку автоматизированных тестовых сценариев
- Regression - Сюда попадают задачи на выполнение тестовых сценариев
- Review Regression - Сюда попадают задачи на проверку результатов выполнения тестовых сценариев, переносом с предыдущего проекта

# Branches:
- Master - Основная ветка, содержащая стабильную версию разрабатываемого ПО
- Release - Ветка в которую выполняется мерж из ветки Testing когда завершен этап разработки.
- Testing - Ветка в которую выполняется мерж всех issue
- issue-*** - Ветка для реализации задачи.

# Столбцы в таблице тестовых сценариев:
## Test ID
(обязательный) Формируется по шаблону issue-9-1 где 
* 9 это номер задачи описывающий автоматизируемый функционал
* 1 это порядковый номер тестового сценария
## Test title
(обязательный) Короткое название теста, например: 
* Появление горизонтального скролла для таблицы Преподаватели
* Исчезновение вертикального скролла для таблцы Преподаватели
## Description
(обязавтельный) Более детальное описание Test title, например:
* Появление горизонтального скролла, при добавлении длинных значений в ячейке
* Появление горизонтального скролла, при изменении значения в ячейке на длинное
* Исчезновение вертикального скролла, при удалении неотображаемых строк
* Исчезновение вертикального скролла, при наложении фильтрации
## Pre-condition
(необязательный) Набор действий приводящих систему в необходимое состояние. Может ссылаться на другой сценарий, который приводит систему в необходимое состояние
## Test Data
(необязательный) может содержать SQL запросы, перечень объектов которые потребуются для тестирования и.д.
## Steps
(обязательный) Нумерованный перечень действий пользователей:
1. Перейти к списку преподавателей
2. Нажать на столбец "Имя"
## Expected Result
(обязательный) Описывает ожидаемый результат для указанного действия:
Step 2: Столбец "Имя" отсортирован в алфавитном порядке
## Automated
(обязательный) Указывается статуст автоматизации этого теста:
* No - Если автоматизировать невозможно
* To be - Если автоматизация сценария запланирована
* In Progress - Если сценарий находится в процессе автоматизации
* Yes - Если сценарий автоматизирован
## Mapping with matrix
(необязательный) Путь к файлу в котором храняться автоматические тесты, заполняется по завершению автоматизации
## Automation status
(необязательный) Может выполняться после автоматизации сценария или выполнения автоматических тестов и может принимать значения:
* PASSED - если сценарий не выявил сбоев
* FAILED - если сценарий выявил сбой
* BLOCKED - если невозможно выполнить сценарий
## Manual status
(необязательный) Может выполняться после написания сценария и может принимать значения:
* PASSED - если сценарий не выявил сбоев
* FAILED - если сценарий выявил сбой
* BLOCKED - если невозможно выполнить сценарий
## Comment/Related bugs
(необязательный) Содержит номера и ссылки на баг(и) или причину невозможности выполнить или автоматизировать сценарий.
