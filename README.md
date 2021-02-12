# Equipment-check
Итоговое задание курса "Расширенные возможности Javascript".
Система контроля эксплуатации оборудования

Формирование и проведение инспекций на основе чек-листов для контроля соблюдения условий эксплуатации установок. Оценка состояния 
оборудования на основе данных чек-листа и выявленных дефектов.
Перечень оборудования содержится в файле equipment.json и представляет собой массив элементов с уникальными идентификаторами и
наименованиями.
Структура элемента оборудования:
"id" - Уникальный числовой идентификатор оборудования
"name" - Текстовое наименование оборудования

Каждому виду оборудования соответствует свой чек-лист с набором требований.
Чек-листы содержатся в файле checklists.json и представляют собой массив элементов, содержащий идентификатор оборудования и перечень
требований. Каждое требование, в свою очередь, содержит уникальный идентификатор требования, описание требования и номер элемента 
нормативного правового акта.
Структура элемента чек-листа:
"equipment_id" – Числовой идентификатор оборудования
"check_list" - Массив требований
Структура элемента требования:
"id" - Уникальный числовой идентификатор требования
"requirement" – Текстовое описание требования

Основная бизнес-сущность системы – “проверка”.

Необходимо разработать веб-интерфейс для проведения проверок оборудования по чек-листам. На главной странице, пользователь (инспектор)
видит список проверок и должен уметь создать новую проверку.
Список проверок представлен в виде таблицы: Дата и время начала проверки | Оборудование | Процент выполненных требований.
При создании новой проверки, автоматически указывается дата/время создания и выбирается инспектором одно из доступных видов оборудований.
После выбора оборудования должен отобразиться соответствующий список с требованиями. Каждое требование в чек-листе может иметь состояние
“да” или “нет”. Для завершения проверки инспектор нажимает кнопку “Завершить” и результат добавляется в таблицу проверок.
Для отображения успешности проверок, можно выделить зеленым цветом строки с результатом >= 80% и красным всё, что ниже.
