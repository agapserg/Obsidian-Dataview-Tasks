# Запланированное на сегодня:
```dataview
TASK
FROM #задачи4
WHERE Дата = date({{Title}})
WHERE !completed
```
# Выполненные за сегодня:
```dataview
TASK
FROM #задачи4
WHERE completion = date({{Title}})
WHERE completed
```