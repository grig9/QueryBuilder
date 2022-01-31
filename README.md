# QueryBuilder

Простой построитель запросов

## Использование

необходимо подлючить зависимость, создаем объект PDO
```php
$pdo = new PDO(...);
```

создаем объект QueryBuilder
```php 
$query = new QueryBuilder($pdo);
```
получить все элементы

```php
$query->getAll('tableName');
```

получить один элемент по ID
```php
$query->getOne('tableName', 'ID');
```

создать новую запись
```php
// передать ассоциативный массив вида: array = ['key' => 'value', 'key2' => 'value2']
$query->create('tableName', 'array');
```

обновить запись по ID
```php
// передать ассоциативный массив вида: array = ['key' => 'value', 'key2' => 'value2']
$query->update('tableName', 'array', 'ID');
```
удалить запись по ID
```php
$query->delete('tableName', 'ID');
```

удалить все записи
```php
$query-deleteAll('tableName');
```
