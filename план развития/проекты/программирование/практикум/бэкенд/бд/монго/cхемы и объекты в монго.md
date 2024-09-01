#базаданных #монго #схема
Одна из особенностей нереляционных баз данных — отсутствие схемы. Схема — набор требований к данным: сколько полей у записи, какой длины может быть значение каждого поля, какие символы в нём допустимы.

### Создадим схему

```
import mongoose from "mongoose"; 
enum Gender { Male = 'м', Female = 'ж', Other = 'другой', } 
interface IUser { name: string; gender: Gender; about: string; } 
const userSchema = new mongoose.Schema<IUser>(
{ name: { type: String, required: true, minlength: 2, maxlength: 30, }, 
  gender: { type: String, // гендер — это строка enum: Object.values(Gender), }, 
  about: String, });
```

Модель — это «обёртка» из методов вокруг схемы. Благодаря ей мы можем читать, добавлять, удалять и обновлять документы. В Mongoose модель создают методом `mongoose.model`.

Скопировать кодTSX

```
// models/user.ts

import mongoose from "mongoose";

interface IUser {
  name: string;
  about: string;
}

// Опишем схему:
const userSchema = new mongoose.Schema<IUser>({
  name: {
    type: String,
    required: true,
    minlength: 2,
    maxlength: 30,
  },
  about: String,
});

// создаём модель и экспортируем её
export default mongoose.model<IUser>('user', userSchema); 
```