# Запланированное на сегодня:
```dataview
TASK
FROM #задачи4
WHERE Дата = date({{Title}})
WHERE !completed
GROUP BY list(file.link, сложность) as abs
SORT abs asc
```
# Выполненные за сегодня:
```dataview
TASK
FROM #задачи4
WHERE completion = date({{Title}})
WHERE completed
GROUP BY list(file.link, сложность) as abs
SORT abs asc
```