# Запланированное на сегодня:
```dataview
TASK
FROM #задачи3
WHERE Дата = date({{Title}})
WHERE !completed
GROUP BY list(file.link, сложность) as abs
SORT abs asc
```
# Выполненные за сегодня:
```dataview
TASK
FROM #задачи3
WHERE completion = date({{Title}})
WHERE completed
GROUP BY list(file.link, сложность) as abs
SORT abs asc
```