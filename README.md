# Домашнее задание к занятию «2.6. База данных и хранение данных»

## 1.запрос(ы) для вставки данных минимум о двух книгах в коллекцию books

### Вставка одной книги

```
db.books.insertOne({
title = "title",
description = "description",
_id: UUID(),
authors = "authors",
favorite = "favorite",
fileCover = "fileCover",
fileName = "fileName",
fileBook = "fileBook"
})
```

### Вставка нескольких книг

```
db.books.insertMany([
{
title = "title",
description = "description",
_id: UUID(),
authors = "authors",
favorite = "favorite",
fileCover = "fileCover",
fileName = "fileName",
fileBook = "fileBook"
},
{
title = "title2",
description = "description2",
_id: UUID(),
authors = "authors2",
favorite = "favorite2",
fileCover = "fileCover2",
fileName = "fileName2",
fileBook = "fileBook2"
}
])
```

## 2. запрос для поиска полей документов коллекции books по полю title

`db.books.find({ title: "title" })`

## 3. запрос для редактирования полей: description и authors коллекции books по \_id записи.

### Обновление поля description и authors

```
db.books.updateOne(
{ \_id: "uuid" },
    [
        { $set: { description: "description_new" } },
        { $set: { authors: "authors_new"} }
    ]
)
```
