# RESTful API service для обрабоки последовательности чисел

## Реализовано:  
1. REST API для обработки последовательности чисел.  
2. Изменение формата возвращаемых данных (добавлением header).  
3. Добавлено описание API, с помощью Swagger (http://localhost:8080/swagger-ui/index.html#/).  
4. Кэширование файлов и результатов.  
  
## Примеры запросов и ответов:  
### 1. Запрос на http://localhost:8080/api/value  
```json
{
    "filePath" : "10m.txt",
    "operation" : "GET_MAX_VALUE"
}
```
Ответ:   
```json
{
    "max_value": "49999978"
}
```

### 2. Запрос на http://localhost:8080/api/value c header - accept:application/xml  
```json
{
    "filePath" : "10m.txt",
    "operation" : "GET_MEDIAN_VALUE"
}
```
Ответ:  
```xml
<Map>
    <median_value>25216.0</median_value>
</Map>
```

### 3. Запрос на http://localhost:8080/api/GET_MIN_VALUE  
```json
{
    "filePath" : "10m.txt"
}
```

Ответ:  
```json
{
    "min_value": "-49999996"
}
```

## Все найденные значения из текстового файла 10m.txt:  
Максимальное значение: 49999978  
Минимальное значение: -49999996  
Медиана: 25216.0  
Среднее арифметическое: 62.97330929733093  
Возрастающая последовательность: [-48190694, -47725447, -43038241, -20190291, -17190728, -6172572, 8475960, 25205909, 48332507, 48676185]  
Убывающая последовательность: [47689379, 42381213, 30043880, 12102356, -4774057, -5157723, -11217378, -23005285, -23016933, -39209115, -49148762]  
