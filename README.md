# Лабораторная работа №19: 

## Основная информация

**ФИО:** Боровой Роман Николаевич, Соколов Вовчик Санекович
**Группа:** ИСП-233  
**Дата:** 24.03.2026  

---

## Описание (что изучили)

В ходе лабораторной работы были изучены основы работы с объектами в JavaScript:
- Создание объектов с помощью литерала `{}`
- Добавление и удаление свойств объекта
- Создание методов объекта
- Перебор свойств объекта с помощью цикла `for...in`

---

## Структура проекта

---lab19/
├── index.html # Демонстрационная страница
├── script.js # Скрипты с примерами
└── README.md # Описание работы

## Примеры кода

### 1. Создание объекта и добавление свойств

```javascript
let user2 = {
    name: "vovchik",
    age: 20,
    isStudent: true
};

user2.age = 30;
user2.name = "Романчик";
delete user2.isStudent;
console.log(user2);
//2
let user2 = {
    name: "vovchik",
    age: 20,
    isStudent: true,
    sayHello: function() {
        console.log(`Hello, my name is ${this.name}`);
    }
};

user2.sayHello();

//3
let car = {
    brand: "Toyota",
    year: 2022,
    getInfo: function() {
        console.log(`Автомобиль: ${this.brand}, год выпуска: ${this.year}`);
    }
};

car.getInfo();
//4
let product = {
    name: "Ноутбук",
    price: 50000,
    category: "Электроника",
    inStock: true
};


product.rating = 4.8;
product.brand = "Lenovo";


for (let key in product) {
    console.log(`${key}: ${product[key]}`);
}
