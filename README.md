[![Logo](https://raw.githubusercontent.com/ogycode/SQLFromZero/master/merch/logo.jpg)](https://github.com/ogycode/CPPFromZero)

# SQL from Zero
**I study the technology and this is my "note-book"**

1. [Create DB](#create)
2. 

## <a name="create"></a>A Heading in this SO entry!:
### *Системные базы данных, которые нужны для работы SQL Server'a:*
 - **master** - главная БД, без нее не будет работать сервер
 - **model** - шаблон для создания других БД
 - **msdb** - хранит информацию о планировщике и бэкапах
 - **tempdb** - хранилище для воеменных обьектов, пересоздается при каждом запуске сервера

 ### *Ключевые слова при создании БД:*
 - **Logical Name** - имя файла БД
 - **File Type** - тип файлов БД, ROWS Data, LOG
 - **Filegroup** - группа файлов, используется для разбиения БД на части
 - **Initial Size** - размер БД при старте
 - **Autogrowth/Maxsize** - размер, в мегабайтах или процентах, на который будет увеличиватся БД
 - **Path** - путь, где будут хранится БД
 - **File Name** - непосредственно имя БД

### *Ключевые слова при создание таблицы:*
 - **Column Name** - имя столбца
 - **Data Type** - тип данных в столбце
 - **Allow Nulls** - может ли значение в ячейке == NULL

Перед созданием необходимо создать столбец с ID и устоновить для него *Primary Key*.

### Пример запроса к БД:
`SELECT * FROM [Имя БД].[Схема].[Имя таблицы]`

 > *Пример:*
 > 
 > `SELECT * FROM bdName.dbo.Users`

Этот запрос выведет все записи из таблици Users (Выбрать ВСЕ из БД). Если необходимо выполнить несколько запросов к одной таблице:

`USE [Имя БД]`

`SELECT * FROM [Имя таблицы]`

> *Пример:*
 > 
 > `USE bdName`
 >
 > `SELECT * FROM Users`