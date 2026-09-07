---
course: "Веб-програмування: Практичні"
type: практика
due: 2026-04-19
status: done
year: 2
semester: 2
period: 2025-26
---
# Практична робота 4 Розробка REST API для енергетичних даних

**Курс:** Основи Веб-програмування ТВ-43: 2-й Семестр 2025/26 навчального року
**Дедлайн:** 19 квіт.

## Вкладення

- 📎 _ОВП Практична робота 4 v_2025_11_24.pdf

## Google Classroom

[Відкрити завдання](https://classroom.google.com/u/0/c/ODE4NTM3MzA5OTg0/a/ODMyNTQ0NjgwMTI4/details)

---

## 📄 _ОВП Практична робота 4 v_2025_11_24.pdf

1 
 
МІНІСТЕРСТВО ОСВІТИ І НАУКИ УКРАЇНИ 
НАЦІОНАЛЬНИЙ ТЕХНІЧНИЙ УНІВЕРСИТЕТ УКРАЇНИ 
«КИЇВСЬКИЙ ПОЛІТЕХНІЧНИЙ ІНСТИТУТ ІМЕНІ ІГОРЯ СІКОРСЬКОГО» 
 
 
 
 
 
 
 
 
 
 
ОСНОВИ ВЕБ-ПРОГРАМУВАННЯ 
 
 
Практична робота No4 
(практичні заняття 10 - 12) 
 
 
 
 
 
 
 
 
 
Рекомендовано Методичною радою КПІ ім. Ігоря Сікорського  
як навчальний посібник для здобувачів ступеня бакалавра 
за освітньою програмою «Інженерія програмного забезпечення інтелектуальних кібер-фізичних 
систем в енергетиці» 
за спеціальністю 121 Інженерія програмного забезпечення 
 
 
 
 
 
Електронне мережеве навчальне видання 
 
 
 
КИЇВ 
КПІ ІМ. ІГОРЯ СІКОРСЬКОГО 
2025 

2 
 
ПРАКТИЧНА РОБОТА No4 (практичні заняття 10 - 12). Розробка 
REST API для енергетичних даних. 
 
ЗМІСТ 
ПРАКТИЧНА РОБОТА No4 (практичні заняття 10 - 12). Розробка REST API для енергетичних 
даних. ....................................................................................................................................................... 2 
План практичної роботи No4: Розробка REST API для енергетичних даних................................ 3 
Практичне заняття No10: проєктування REST API для енергетичних даних ............................ 3 
Практичне заняття No11: реалізація REST API для енергетичних даних .................................. 3 
Практичне заняття No12: тестування REST API для енергетичних даних ................................ 3 
Загальна інформація ........................................................................................................................... 3 
4.1. Теоретичний матеріал ................................................................................................................. 3 
4.1.1. Що таке REST API? .............................................................................................................. 3 
4.2. Базовий приклад REST API ........................................................................................................ 4 
4.2.1. Крок 1: Встановлення залежностей .................................................................................... 4 
4.2.2. Крок 2: Базова структура сервера ........................................................................................ 4 
4.2.3. Крок 3: Тестування API ........................................................................................................ 5 
4.3. Приклад повної реалізації ........................................................................................................... 6 
4.2.1. Завдання ................................................................................................................................. 6 
4.2.2. Виконання .............................................................................................................................. 7 
4.4. Структура звіту до практичної роботи .................................................................................... 14 
4.4.1. Титульна сторінка ............................................................................................................... 14 
4.4.2. Мета роботи ......................................................................................................................... 14 
4.4.3. Теоретична частина ............................................................................................................ 14 
4.4.4. Опис реалізації .................................................................................................................... 14 
4.4.5. Висновки .............................................................................................................................. 15 
4.4.6. Список використаних джерел ............................................................................................ 15 
4.4.7. Додатки ................................................................................................................................ 15 
4.5. Критерії оцінювання ................................................................................................................. 16 
4.5.1. Проєктування структури API (20 балів) ........................................................................... 16 
4.5.2. Реалізація основних endpoints (30 балів) .......................................................................... 16 
4.5.3. Валідація та обробка помилок (15 балів) .......................................................................... 16 
4.5.4. Додаткова функціональність (фільтри, пошук) (15 балів) .............................................. 16 
4.5.5. Тестування та документація (15 балів) ............................................................................. 16 
4.5.6. Якість коду та структура (5 балів) ..................................................................................... 16 
4.6. Контрольні питання ................................................................................................................... 16 
4.7. Поради для успішного виконання ............................................................................................ 16 
Список рекомендованої літератури ................................................................................................ 16 
Перелік посилань .............................................................................................................................. 17 
Корисні інструменти ........................................................................................................................ 17 
Додатки .............................................................................................................................................. 17 
Додаток А. Варіанти індивідуальних завдань ............................................................................ 17 
Додаток Б. Приклади команд curl ............................................................................................... 32 
 
 
 
 
 
 

3 
 
План практичної роботи No4: Розробка REST API для енергетичних 
даних. 
Практичне заняття No10: проєктування REST API для енергетичних даних 
Проєктування API  для  об’єкта  енергетики,  що  видає  JSON-запити/відповіді  щодо 
параметрів об’єкта (потужність, напруга тощо). 
Практичне заняття No11: реалізація REST API для енергетичних даних 
Реалізація API для об’єкта енергетики, що видає JSON-запити/відповіді щодо параметрів 
об’єкта (потужність, напруга тощо). 
Практичне заняття No12: тестування REST API для енергетичних даних 
Тестування та оформлення звіту з реалізації API для об’єкта енергетики, що видає JSON-
запити/відповіді щодо параметрів об’єкта (потужність, напруга тощо). 
Загальна інформація 
Мета: Навчитися проєктувати та розробляти REST API на Node.js + Express для обміну 
даними енергетичних об'єктів у форматі JSON. 
Завдання: 
1.  Спроєктувати REST  API  для  енергетичних  даних у  відповідності  з  індивідуальним 
варіантом завдання. 
2.  Реалізувати  REST  API  для  енергетичних  даних  у  відповідності  з  індивідуальним 
варіантом завдання 
3.  Протестувати  роботу REST  API  для  енергетичних  даних у  відповідності  з 
індивідуальним варіантом завдання 
Тривалість: 6 годин (3 заняття по 2 години) 
4.1. Теоретичний матеріал 
4.1.1. Що таке REST API? 
REST  (Representational  State  Transfer) - архітектурний стиль для створення веб-сервісів, 
що використовує HTTP-протокол для обміну даними. 
4.1.1.1. Основні принципи REST: 
- Клієнт-серверна архітектура 
- Відсутність стану (stateless) 
- Кешування 
- Єдиний інтерфейс 
- Шарова система 
4.1.1.2. HTTP методи в REST API 
Метод Призначення Приклад 
GET Отримання даних GET /api/stations - список станцій 
POST Створення нового ресурсу POST /api/stations - створити станцію 
PUT Повне оновлення ресурсу PUT /api/stations/1 - оновити станцію 
PATCH Часткове оновлення PATCH /api/stations/1 - оновити поле 
DELETE Видалення ресурсу DELETE /api/stations/1 - видалити 
4.1.1.3. Коди відповідей HTTP 
Коди відповідей HTTP 
- 200 OK - успішний запит 

4 
 
- 201 Created - ресурс створено 
- 400 Bad Request - помилка в запиті 
- 404 Not Found - ресурс не знайдено 
- 500 Internal Server Error - помилка сервера 
 
4.1.1.4. Структура REST API для енергетики 
/api/objects          - колекція об'єктів 
/api/objects/:id      - конкретний об'єкт 
/api/objects/:id/data - дані об'єкта 
4.2. Базовий приклад REST API 
4.2.1. Крок 1: Встановлення залежностей 
bash: 
npm init -y 
npm install express 
npm install --save-dev nodemon 
4.2.2. Крок 2: Базова структура сервера 
javascript: 
// server.js 
const express = require('express'); 
const app = express(); 
const PORT = 3000; 
 
// Middleware для парсингу JSON 
app.use(express.json()); 
 
// Тестові дані 
let stations = [ 
  { 
    id: 1, 
    name: "Підстанція No1", 
    type: "Трансформаторна", 
    voltage: 110, 
    power: 25, 
    status: "active" 
  } 
]; 
 
// GET - отримати всі станції 
app.get('/api/stations', (req, res) => { 
  res.json(stations); 
}); 
 
// GET - отримати станцію за ID 

5 
 
app.get('/api/stations/:id', (req, res) => { 
  const station = stations.find(s => s.id === parseInt(req.params.id)); 
  if (!station) { 
    return res.status(404).json({ error: 'Станція не знайдена' }); 
  } 
  res.json(station); 
}); 
 
// POST - створити нову станцію 
app.post('/api/stations', (req, res) => { 
  const newStation = { 
    id: stations.length + 1, 
    ...req.body 
  }; 
  stations.push(newStation); 
  res.status(201).json(newStation); 
}); 
 
// PUT - оновити станцію 
app.put('/api/stations/:id', (req, res) => { 
  const index = stations.findIndex(s => s.id === parseInt(req.params.id)); 
  if (index === -1) { 
    return res.status(404).json({ error: 'Станція не знайдена' }); 
  } 
  stations[index] = { id: parseInt(req.params.id), ...req.body }; 
  res.json(stations[index]); 
}); 
 
// DELETE - видалити станцію 
app.delete('/api/stations/:id', (req, res) => { 
  const index = stations.findIndex(s => s.id === parseInt(req.params.id)); 
  if (index === -1) { 
    return res.status(404).json({ error: 'Станція не знайдена' }); 
  } 
  stations.splice(index, 1); 
  res.json({ message: 'Станція видалена' }); 
}); 
 
app.listen(PORT, () => { 
  console.log(`Сервер запущено на http://localhost:${PORT}`); 
}); 
4.2.3. Крок 3: Тестування API 
Використовуйте Postman або curl: 
bash: 

6 
 
# GET всі станції 
curl http://localhost:3000/api/stations 
 
# GET станція за ID 
curl http://localhost:3000/api/stations/1 
 
# POST нова станція 
curl -X POST http://localhost:3000/api/stations \ 
  -H "Content-Type: application/json" \ 
  -d '{"name":"Підстанція 
No2","type":"Розподільча","voltage":35,"power":10,"status":"active"}' 
 
# PUT оновлення 
curl -X PUT http://localhost:3000/api/stations/1 \ 
  -H "Content-Type: application/json" \ 
  -d '{"name":"Підстанція No1 
(оновлена)","type":"Трансформаторна","voltage":110,"power":30,"status":"active"}' 
 
# DELETE видалення 
curl -X DELETE http://localhost:3000/api/stations/1 
4.3. Приклад повної реалізації 
4.2.1. Завдання 
Назва об'єкта: Трансформаторна підстанція 110/35/10 кВ 
Об'єкт: Трансформаторна підстанція 
Основні вимоги: 
Параметри для API: 
id - унікальний ідентифікатор 
name - назва підстанції 
voltageHigh - напруга ВН (кВ): 110 
voltageMedium - напруга СН (кВ): 35 
voltageLow - напруга НН (кВ): 10 
transformerPower - потужність трансформатора (МВА) 
load - поточне навантаження (МВт) 
temperature - температура масла (°C) 
status - статус: "active", "maintenance", "alarm" 
Endpoints: 
GET /api/substations - список всіх підстанцій 
GET /api/substations/:id - дані підстанції 
GET /api/substations/:id/parameters - поточні параметри 
POST /api/substations - додати підстанцію 
PUT /api/substations/:id - оновити дані 
DELETE /api/substations/:id - видалити підстанцію 
Технічні вимоги: 
Node.js + Express 

7 
 
JSON формат даних 
Мінімум 5 різних endpoints 
Middleware для обробки JSON 
Обробка помилок 
4.2.2. Виконання 
4.2.2.1. Повний код server.js 
javascript: 
const express = require('express'); 
const app = express(); 
const PORT = 3000; 
 
// Middleware 
app.use(express.json()); 
 
// Початкові дані підстанцій 
let substations = [ 
  { 
    id: 1, 
    name: "ТП-110/35/10 Центральна", 
    voltageHigh: 110, 
    voltageMedium: 35, 
    voltageLow: 10, 
    transformerPower: 40, 
    load: 28.5, 
    temperature: 65, 
    status: "active" 
  }, 
  { 
    id: 2, 
    name: "ТП-110/10 Промислова", 
    voltageHigh: 110, 
    voltageMedium: null, 
    voltageLow: 10, 
    transformerPower: 25, 
    load: 18.2, 
    temperature: 58, 
    status: "active" 
  } 
]; 
 
// GET - отримати всі підстанції 
app.get('/api/substations', (req, res) => { 
  const { status } = req.query; 
   

8 
 
  if (status) { 
    const filtered = substations.filter(s => s.status === status); 
    return res.json(filtered); 
  } 
   
  res.json(substations); 
}); 
 
// GET - отримати підстанцію за ID 
app.get('/api/substations/:id', (req, res) => { 
  const substation = substations.find(s => s.id === parseInt(req.params.id)); 
   
  if (!substation) { 
    return res.status(404).json({  
      error: 'Підстанцію не знайдено', 
      id: req.params.id  
    }); 
  } 
   
  res.json(substation); 
}); 
 
// GET - отримати параметри підстанції 
app.get('/api/substations/:id/parameters', (req, res) => { 
  const substation = substations.find(s => s.id === parseInt(req.params.id)); 
   
  if (!substation) { 
    return res.status(404).json({ error: 'Підстанцію не знайдено' }); 
  } 
   
  const parameters = { 
    voltages: { 
      high: substation.voltageHigh, 
      medium: substation.voltageMedium, 
      low: substation.voltageLow 
    }, 
    power: { 
      rated: substation.transformerPower, 
      current: substation.load, 
      loadFactor: (substation.load / substation.transformerPower * 100).toFixed(2) + '%' 
    }, 
    temperature: { 
      current: substation.temperature, 
      status: substation.temperature > 75 ? 'warning' : 'normal' 
    } 

9 
 
  }; 
   
  res.json(parameters); 
}); 
 
// POST - створити нову підстанцію 
app.post('/api/substations', (req, res) => { 
  const { name, voltageHigh, voltageMedium, voltageLow, transformerPower } = req.body; 
   
  // Валідація 
  if (!name || !voltageHigh || !voltageLow || !transformerPower) { 
    return res.status(400).json({  
      error: 'Відсутні обов\'язкові поля', 
      required: ['name', 'voltageHigh', 'voltageLow', 'transformerPower'] 
    }); 
  } 
   
  const newSubstation = { 
    id: substations.length > 0 ? Math.max(...substations.map(s => s.id)) + 1 : 1, 
    name, 
    voltageHigh, 
    voltageMedium: voltageMedium || null, 
    voltageLow, 
    transformerPower, 
    load: 0, 
    temperature: 25, 
    status: 'active' 
  }; 
   
  substations.push(newSubstation); 
  res.status(201).json(newSubstation); 
}); 
 
// PUT - оновити підстанцію 
app.put('/api/substations/:id', (req, res) => { 
  const index = substations.findIndex(s => s.id === parseInt(req.params.id)); 
   
  if (index === -1) { 
    return res.status(404).json({ error: 'Підстанцію не знайдено' }); 
  } 
   
  substations[index] = { 
    id: parseInt(req.params.id), 
    ...req.body 
  }; 

10 
 
   
  res.json(substations[index]); 
}); 
 
// PATCH - часткове оновлення (наприклад, лише температура або навантаження) 
app.patch('/api/substations/:id', (req, res) => { 
  const index = substations.findIndex(s => s.id === parseInt(req.params.id)); 
   
  if (index === -1) { 
    return res.status(404).json({ error: 'Підстанцію не знайдено' }); 
  } 
   
  substations[index] = { 
    ...substations[index], 
    ...req.body, 
    id: parseInt(req.params.id) // Зберігаємо ID 
  }; 
   
  res.json(substations[index]); 
}); 
 
// DELETE - видалити підстанцію 
app.delete('/api/substations/:id', (req, res) => { 
  const index = substations.findIndex(s => s.id === parseInt(req.params.id)); 
   
  if (index === -1) { 
    return res.status(404).json({ error: 'Підстанцію не знайдено' }); 
  } 
   
  const deleted = substations.splice(index, 1); 
  res.json({  
    message: 'Підстанцію видалено', 
    substation: deleted[0] 
  }); 
}); 
 
// Запуск сервера 
app.listen(PORT, () => { 
  console.log(` REST API сервер запущено на http://localhost:${PORT}`); 
  console.log(` Доступні endpoints:`); 
  console.log(`   GET    /api/substations`); 
  console.log(`   GET    /api/substations/:id`); 
  console.log(`   GET    /api/substations/:id/parameters`); 
  console.log(`   POST   /api/substations`); 

11 
 
  console.log(`   PUT    /api/substations/:id`); 
  console.log(`   PATCH  /api/substations/:id`); 
  console.log(`   DELETE /api/substations/:id`); 
}); 
4.2.2.2. Приклад використання API (test-api.js) 
javascript: 
// Тестування API з використанням fetch (Node.js 18+) 
 
const BASE_URL = 'http://localhost:3000/api'; 
 
async function testAPI() { 
  console.log('離 Тестування REST API...\n'); 
   
  try { 
    // 1. GET - всі підстанції 
    console.log('1⃣ GET /api/substations'); 
    let response = await fetch(`${BASE_URL}/substations`); 
    let data = await response.json(); 
    console.log('Відповідь:', data); 
    console.log('---\n'); 
     
    // 2. GET - підстанція за ID 
    console.log('2⃣ GET /api/substations/1'); 
    response = await fetch(`${BASE_URL}/substations/1`); 
    data = await response.json(); 
    console.log('Відповідь:', data); 
    console.log('---\n'); 
     
    // 3. POST - нова підстанція 
    console.log('3⃣ POST /api/substations'); 
    const newSubstation = { 
      name: "ТП-35/10 Нова", 
      voltageHigh: 35, 
      voltageLow: 10, 
      transformerPower: 16 
    }; 
    response = await fetch(`${BASE_URL}/substations`, { 
      method: 'POST', 
      headers: { 'Content-Type': 'application/json' }, 
      body: JSON.stringify(newSubstation) 
    }); 
    data = await response.json(); 
    console.log('Відповідь:', data); 
    const newId = data.id; 

12 
 
    console.log('---\n'); 
     
    // 4. PATCH - оновити навантаження 
    console.log(`4⃣ PATCH /api/substations/${newId}`); 
    response = await fetch(`${BASE_URL}/substations/${newId}`, { 
      method: 'PATCH', 
      headers: { 'Content-Type': 'application/json' }, 
      body: JSON.stringify({ load: 8.5, temperature: 52 }) 
    }); 
    data = await response.json(); 
    console.log('Відповідь:', data); 
    console.log('---\n'); 
     
    // 5. GET - параметри підстанції 
    console.log(`5⃣ GET /api/substations/${newId}/parameters`); 
    response = await fetch(`${BASE_URL}/substations/${newId}/parameters`); 
    data = await response.json(); 
    console.log('Відповідь:', data); 
    console.log('---\n'); 
     
    // 6. DELETE - видалити підстанцію 
    console.log(`6⃣ DELETE /api/substations/${newId}`); 
    response = await fetch(`${BASE_URL}/substations/${newId}`, { 
      method: 'DELETE' 
    }); 
    data = await response.json(); 
    console.log('Відповідь:', data); 
    console.log('---\n'); 
     
    console.log('✅ Тестування завершено успішно!'); 
     
  } catch (error) { 
    console.error('❌ Помилка:', error.message); 
  } 
} 
 
// Запуск тестів 
testAPI(); 
 
Результат демонстрації  реалізації  і  тестування  REST  API  для  енергетичних  даних 
наведено на рис.4.1. 

13 
 
 
Рис. 4.1. Результат демонстрації реалізації і тестування REST API для енергетичних даних 

14 
 
Результат заняття: Готовий код сервера з усіма CRUD операціями та прикладами 
тестування API. 
4.4. Структура звіту до практичної роботи 
4.4.1. Титульна сторінка 
- Назва університету, факультет, кафедра 
- Назва дисципліни 
- Номер та тема практичної роботи 
- Варіант 
- ПІБ студента, група 
- ПІБ викладача 
- Дата виконання 
4.4.2. Мета роботи 
Коротко описати мету практичної роботи 
4.4.3. Теоретична частина 
- REST API 
- Node.js + Express 
- формат JSON 
- Опис об'єкта автоматизації 
- Перелік вимог 
- Обґрунтування вибраних методів реалізації 
4.4.4. Опис реалізації 
4.4.4.1. Завдання 1: Проєктування API (Заняття 10) 
Для вашого варіанту виконайте: 
Аналіз предметної галузі: 
- Визначте основні сутності вашого об'єкта 
- Складіть список параметрів, які потрібно відслідковувати 
- Визначте взаємозв'язки між даними 
Проєктування структури API: 
- Розробіть схему endpoints (мінімум 5-7) 
- Визначте HTTP методи для кожного endpoint 
- Спроєктуйте структуру JSON-об'єктів 
- Визначте коди відповідей для різних ситуацій 
Документація: 
- Опишіть кожен endpoint 
- Наведіть приклади запитів та відповідей 
- Вкажіть можливі помилки 
Оформлення: Звіт у форматі Markdown з діаграмами та прикладами. 
4.4.4.2. Завдання 2: Реалізація API (Заняття 11) 
Реалізуйте REST API для вашого варіанту: 
Базова функціональність: 
- Створіть Express-сервер 
- Реалізуйте всі спроєктовані endpoints 

15 
 
- Використайте масив об'єктів для зберігання даних 
- Додайте валідацію вхідних даних 
Розширена функціональність: 
- Фільтрація даних (query parameters) 
- Пагінація для великих списків 
- Сортування результатів 
- Пошук за параметрами 
Обробка помилок: 
- Правильні HTTP коди відповідей 
- Інформативні повідомлення про помилки 
- Валідація обов'язкових полів 
Технічні вимоги: 
- Node.js + Express 
- JSON формат даних 
- Мінімум 5 різних endpoints 
- Middleware для обробки JSON 
- Обробка помилок 
4.4.4.3. Завдання 3: Тестування та документація (Заняття 12) 
Тестування: 
- Протестуйте всі endpoints за допомогою Postman або curl 
- Перевірте всі HTTP методи (GET, POST, PUT, PATCH, DELETE) 
- Протестуйте граничні випадки та помилки 
- Створіть колекцію тестів у Postman 
Додаткові функції: 
- Middleware для логування запитів 
- CORS налаштування 
- Обмеження розміру запитів 
- Статистика викликів API 
Звіт: 
- Документація API 
- Скріншоти тестування 
- Опис реалізованих функцій 
- Приклади використання 
4.4.5. Висновки 
- Що було реалізовано 
- Отримані навички 
- Можливості розвитку 
4.4.6. Список використаних джерел 
4.4.7. Додатки 
- Повний код проєкту (основні файли) 
- Додаткові скріншоти 
- Конфігураційні файли 

16 
 
4.5. Критерії оцінювання 
Максимальна оцінка: 100 балів. Отримана оцінка за контрольний захід (максимум 100 
балів)  переводиться  за  допомогою  відповідного  значення  «Вага  оцінки  в  загальному 
семестровому  рейтингу  (див.  Силабус)»  в  «Значення  оцінки  за  контрольний  захід  в  складі 
загально семестрового рейтингу» з точністю до 2-х значень після коми. 
4.5.1. Проєктування структури API (20 балів) 
4.5.2. Реалізація основних endpoints (30 балів) 
4.5.3. Валідація та обробка помилок (15 балів) 
4.5.4. Додаткова функціональність (фільтри, пошук) (15 балів) 
4.5.5. Тестування та документація (15 балів) 
4.5.6. Якість коду та структура (5 балів) 
4.6. Контрольні питання 
1. Що означає абревіатура REST? 
2. Який HTTP метод використовується для отримання даних з сервера? 
3. Який код відповіді HTTP означає успішне створення нового ресурсу? 
4.  Який  HTTP  метод  є  ідемпотентним  і  використовується  для  повного  оновлення 
ресурсу? 
5. Що таке endpoint в контексті REST API? 
6. Який код статусу HTTP повертається, коли запитуваний ресурс не знайдено? 
7. Який формат даних найчастіше використовується в REST API? 
8. Що означає принцип 'stateless' в REST архітектурі? 
9. Який HTTP метод використовується для видалення ресурсу? 
10. Що таке middleware в Express.js? 
11. Який код відповіді означає помилку на стороні сервера? 
12. Який HTTP метод використовується для часткового оновлення ресурсу? 
13. Що таке CRUD операції? 
14. Для чого використовується query parameter в URL? 
15. Який заголовок HTTP використовується для вказання типу вмісту тіла запиту?  
4.7. Поради для успішного виконання 
Почніть з простого: Спочатку реалізуйте базові GET/POST  endpoints,  потім додавайте 
складнішу функціональність 
Використовуйте nodemon: Для автоматичного перезапуску сервера при змінах коду 
Тестуйте часто: Перевіряйте кожен endpoint одразу після реалізації 
Документуйте код: Додавайте коментарі та описи для кожного endpoint 
Думайте про реальність: Ваш API має бути корисним для реальної енергетичної системи 
Обробляйте помилки: Завжди перевіряйте вхідні дані та правильно обробляйте помилки 
Список рекомендованої літератури 
1.  Head  First  HTML  and  CSS:  A  Learner's  Guide  to  Creating  Standards-Based  Web  Pages. 
O'Reilly Media. 2022. – 762 р. ISBN 978-0596159900. 
2.  HTML,  CSS,  and  JavaScript  All  in  One:  Covering  HTML5,  CSS3,  and  ES6,  Sams  Teach 
Yourself. Sams Publishing. 2021. – 800 р. ISBN 978-0672338083. 

17 
 
3. Head First. Програмування на JavaScript. Фабула. 2022. – 672 р. ISBN 978-617-522-047-
4. 
4. Head First. Python. Фабула. 2023. – 624 р. ISBN 978-617-522-019-1. 
5. Head First PHP & MySQL. O'Reilly Media. 2023. – 812 р. ISBN 978-0596006303. 
6. Duncan McGregor, Nat Pryce, Java to Kotlin: A Refactoring Guidebook, «O'Reilly Media», 
2021. – 422 р. ISBN 978-1492082279 
7. Nate Ebel, Mastering Kotlin: Learn advanced Kotlin programming techniques to build apps 
for Android, iOS, and the web, «Packt Publishing», 2021. - 434 р. ISBN 978-1838555726. 
8. Mozilla Developer Network. Електронний ресурс: https://developer.mozilla.org/en-US/ 
9. W3Schools Online Web Tutorials. Електронний ресурс: https://www.w3schools.com/ 
ресурс: https://docs.oracle.com/javase/tutorial/java/javaOO/objectcreation.html 
10.   Електронний   ресурс:   http://www.oracle.com/technetwork/java/javase/8-whats-new-
2157071.html 
Перелік посилань 
1. MDN HTTP Methods. - [Електронний   ресурс]. - Режим   доступу: 
https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods. - Назва з екрана. 
2. REST  API  Tutorial. - [Електронний ресурс]. - Режим доступу: https://restfulapi.net/. - 
Назва з екрана. 
3. Express.js Documentation. - [Електронний   ресурс]. - Режим   доступу: 
https://expressjs.com/. - Назва з екрана. 
Корисні інструменти 
1. Postman - тестування API 
2. Thunder Client - VS Code extension 
3. curl - командний рядок 
4. Insomnia - альтернатива Postman 
Додатки 
Додаток А. Варіанти індивідуальних завдань 
УВАГА!!! ВСІ ВАРІАНТИ ЗАВДАНЬ ВИГАДАНІ! БУДЬ-ЯКЕ СПІВПАДІННЯ – Є 
ВИПАДКОВИМ ЗБІГОМ!!! 
Варіант 1: Трансформаторна підстанція 110/35/10 кВ 
Об’єкт: REST  API  для  управління  даними  трансформаторних  підстанцій  високої 
напруги  з  можливістю  моніторингу  параметрів  роботи,  навантаження  та  температурного 
режиму. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор підстанції 
name   string  Назва трансформаторної підстанції 
voltageHigh  number Напруга високої сторони (кВ) 
voltageMedium number Напруга середньої сторони (кВ) 
voltageLow  number Напруга низької сторони (кВ) 
transformerPower number Номінальна потужність (МВА) 
load   number Поточне навантаження (МВт) 

18 
 
temperature  number Температура масла трансформатора (°C) 
status   string  Статус: active/maintenance/alarm 
Endpoints API: 
GET  /api/substations   Отримати список всіх підстанцій 
GET  /api/substations/:id   Отримати підстанцію за ID 
GET  /api/substations/:id/parameters Отримати поточні параметри роботи 
POST  /api/substations   Створити нову підстанцію 
PUT  /api/substations/:id   Повне оновлення даних підстанції 
PATCH /api/substations/:id   Часткове оновлення параметрів 
DELETE /api/substations/:id   Видалити підстанцію з системи 
Варіант 2: Сонячна електростанція (СЕС) 
Об’єкт: REST  API  для  моніторингу  та  управління  сонячними  електростанціями з 
відстеженням генерації, сонячної радіації та ефективності роботи панелей. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор СЕС 
name   string  Назва сонячної електростанції 
installedPower  number Встановлена потужність (кВт) 
currentPower  number Поточна потужність генерації (кВт) 
dailyGeneration number Добова генерація електроенергії (кВт·год) 
solarIrradiance number Сонячна радіація на панелях (Вт/м²) 
panelTemperature number Температура сонячних панелей (°C) 
efficiency  number Поточна ефективність системи (%) 
status   string  Статус: active/standby/maintenance 
Endpoints API: 
GET  /api/solar-plants   Отримати список всіх СЕС 
GET  /api/solar-plants/:id   Отримати дані конкретної СЕС 
GET  /api/solar-plants/:id/generation Отримати дані генерації 
POST  /api/solar-plants/:id/readings  Записати нові покази приладів 
PUT  /api/solar-plants/:id   Оновити параметри СЕС 
DELETE /api/solar-plants/:id   Видалити СЕС із системи 
Варіант 3: Вітроелектростанція (ВЕС) 
Об’єкт: REST  API  для  моніторингу вітрових  електростанцій  з  контролем  швидкості 
вітру, обертання турбін та генерованої потужності. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор ВЕС 
name   string  Назва вітроелектростанції 
turbineCount  number Загальна кількість вітрових турбін 
turbinePower  number Потужність однієї турбіни (кВт) 
currentPower  number Поточна загальна потужність (кВт) 
windSpeed  number Поточна швидкість вітру (м/с) 
windDirection  number Напрямок вітру (градуси) 
rotorSpeed  number Швидкість обертання ротора (об/хв) 

19 
 
availability  number Коефіцієнт готовності (%) 
Endpoints API: 
GET /api/wind-plants   Отримати всі ВЕС 
GET /api/wind-plants/:id   Отримати конкретну ВЕС 
GET /api/wind-plants/:id/turbines  Отримати дані всіх турбін 
GET /api/wind-plants/:id/wind-data Отримати метеодані вітру 
POST /api/wind-plants/:id/readings  Записати покази датчиків 
PUT /api/wind-plants/:id   Оновити параметри ВЕС 
Варіант 4: Гідроелектростанція (ГЕС) 
Об’єкт: REST  API  для  управління  гідроелектростанціями  з  моніторингом  рівня  води, 
витрати та роботи гідроагрегатів. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор ГЕС 
name   string  Назва гідроелектростанції 
installedPower  number Встановлена потужність (МВт) 
currentPower  number Поточна генерована потужність (МВт) 
waterLevel  number Рівень води у водосховищі (м) 
waterFlow  number Витрата води через турбіни (м³/с) 
turbineCount  number Кількість гідроагрегатів 
turbineEfficiency number Середня ефективність турбін (%) 
reservoirVolume number Об'єм водосховища (млн м³) 
Endpoints API: 
GET  /api/hydro-plants    Отримати список всіх ГЕС 
GET  /api/hydro-plants/:id    Отримати дані конкретної ГЕС 
GET  /api/hydro-plants/:id/water-data  Отримати гідрологічні дані 
POST  /api/hydro-plants/:id/turbines/:turbineId Записати дані турбіни 
PUT  /api/hydro-plants/:id    Оновити параметри ГЕС 
DELETE /api/hydro-plants/:id    Видалити ГЕС 
Варіант 5: Система накопичення енергії (BESS) 
Об’єкт: REST  API  для  управління  батарейними  системами  накопичення  енергії  з 
контролем заряду, розряду та стану батарей. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор BESS 
name   string  Назва системи накопичення 
capacity  number Загальна ємність системи (кВт·год) 
power   number Максимальна потужність (кВт) 
stateOfCharge  number Поточний рівень заряду (%) 
chargingPower number Потужність заряду (кВт) 
dischargingPower number Потужність розряду (кВт) 
cycleCount  number Загальна кількість циклів 
temperature  number Температура батарейного блоку (°C) 
mode   string  Режим: charging/discharging/idle 

20 
 
Endpoints API: 
GET  /api/energy-storage   Отримати всі системи накопичення 
GET  /api/energy-storage/:id  Отримати конкретну систему 
GET  /api/energy-storage/:id/soc  Отримати рівень заряду 
POST  /api/energy-storage/:id/command Відправити команду управління 
PUT  /api/energy-storage/:id  Оновити параметри системи 
DELETE /api/energy-storage/:id  Видалити систему 
Варіант 6: Теплоелектроцентраль (ТЕЦ) 
Об’єкт: REST  API  для  моніторингу  когенераційних  установок  з  відстеженням 
електричної та теплової потужності, витрат палива та викидів. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор ТЕЦ 
name   string  Назва теплоелектроцентралі 
electricPower  number Електрична потужність (МВт) 
thermalPower  number Теплова потужність (Гкал/год) 
fuelType  string  Тип палива: gas/coal/biomass 
fuelConsumption number Витрата палива (м³/год або т/год) 
efficiency  number Загальний ККД установки (%) 
emissions  number Викиди CO₂ (т/год) 
steamPressure  number Тиск пари в котлі (МПа) 
status   string  Статус: active/standby/maintenance 
Endpoints API: 
GET /api/chp-plants   Отримати всі ТЕЦ 
GET /api/chp-plants/:id   Отримати конкретну ТЕЦ 
GET /api/chp-plants/:id/fuel  Отримати дані про паливо 
GET /api/chp-plants/:id/emissions  Отримати дані викидів 
POST /api/chp-plants/:id/readings  Записати покази 
PUT /api/chp-plants/:id   Оновити параметри ТЕЦ 
Варіант 7: Розподільча мережа 10 кВ 
Об’єкт: REST  API  для  моніторингу  розподільних  електричних  мереж  з  контролем 
навантаження, втрат та якості електропостачання. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор мережі 
name   string  Назва фідера або мережі 
voltage   number Номінальна напруга мережі (кВ) 
length   number Загальна довжина ліній (км) 
activePower  number Активна потужність навантаження (кВт) 
reactivePower  number Реактивна потужність (кВАр) 
current   number Струм навантаження (А) 
losses   number Технологічні втрати (кВт) 
substationCount number Кількість трансформаторних підстанцій 
Endpoints API: 

21 
 
GET /api/distribution-networks   Отримати всі мережі 
GET /api/distribution-networks/:id   Отримати конкретну мережу 
GET /api/distribution-networks/:id/losses  Аналіз втрат електроенергії 
GET /api/distribution-networks/:id/substations Список ТП мережі 
POST /api/distribution-networks   Додати нову мережу 
PUT /api/distribution-networks/:id   Оновити дані мережі 
Варіант 8: Розумний електролічильник 
Об’єкт: REST API для систем автоматизованого комерційного обліку електроенергії з 
можливістю віддаленого зняття показів та контролю споживання. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор лічильника 
serialNumber  string  Серійний номер лічильника 
consumerName string  Ім'я споживача 
address  string  Адреса встановлення 
activePower  number Поточна активна потужність (кВт) 
voltage   number Напруга в мережі (В) 
current   number Струм споживання (А) 
energyConsumed number Спожита енергія за період (кВт·год) 
powerFactor  number Коефіцієнт потужності 
tariff   string  Поточний тариф: денний/нічний/пік 
Endpoints API: 
GET /api/smart-meters   Отримати всі лічильники 
GET /api/smart-meters/:id   Отримати конкретний лічильник 
GET /api/smart-meters/:id/consumption Отримати дані споживання 
GET /api/smart-meters/:id/history  Історія показів 
POST /api/smart-meters/:id/readings Записати новий показ 
PUT /api/smart-meters/:id   Оновити дані лічильника 
Варіант 9: Електрозарядна станція (ЕЗС) 
Об’єкт: REST API для управління зарядними станціями електромобілів з моніторингом 
доступності, активних сесій та виданої енергії. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор станції 
name   string  Назва зарядної станції 
location  string  Адреса розташування станції 
chargerCount  number Загальна кількість зарядних пристроїв 
maxPower  number Максимальна потужність заряду (кВт) 
availableChargers number Кількість вільних зарядних 
currentSessions number Активні зарядні сесії 
totalEnergy  number Загальна видана енергія (кВт·год) 
status   string  Статус: available/busy/maintenance 
Endpoints API: 
GET /api/charging-stations    Отримати всі ЕЗС 

22 
 
GET /api/charging-stations/:id   Отримати конкретну станцію 
GET /api/charging-stations/:id/chargers  Статус всіх зарядних 
POST /api/charging-stations/:id/start-session Почати зарядну сесію 
POST /api/charging-stations/:id/stop-session Закінчити зарядну сесію 
PUT /api/charging-stations/:id   Оновити дані станції 
Варіант 10: Диспетчерський центр управління 
Об’єкт: REST  API  для  центрів  управління  енергосистемами  з  моніторингом  балансу 
генерації та навантаження, частоти мережі та тривог. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Ідентифікатор диспетчерського центру 
name   string  Назва диспетчерського центру 
monitoredObjects number Кількість об'єктів під контролем 
totalGeneration number Загальна генерація в системі (МВт) 
totalLoad  number Загальне навантаження системи (МВт) 
frequency  number Частота в електромережі (Гц) 
systemBalance number Баланс генерації та споживання (МВт) 
alarmCount  number Кількість активних тривог 
operatorCount  number Кількість чергових операторів 
Endpoints API: 
GET /api/dispatch-center   Отримати дані центру 
GET /api/dispatch-center/objects  Список всіх підконтрольних об'єктів 
GET /api/dispatch-center/alarms  Отримати активні тривоги 
GET /api/dispatch-center/balance  Баланс системи 
POST /api/dispatch-center/commands Відправити команду управління 
PUT /api/dispatch-center   Оновити параметри центру 
Варіант 11: Високовольтний вимикач 
Об’єкт: REST  API  для  управління  комутаційним  обладнанням  високої  напруги  з 
контролем положення, кількості спрацювань та технічного стану. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор вимикача 
name   string  Позначення вимикача в схемі 
voltage   number Номінальна напруга (кВ) 
current   number Номінальний струм (А) 
position  string  Положення контактів: open/closed 
switchingCount number Загальна кількість комутацій 
lastSwitching  string  Час останньої комутації (ISO 8601) 
mechanism  string  Тип приводу: spring/hydraulic/motor 
operationTime  number Час спрацювання (мс) 
Endpoints API: 
GET  /api/circuit-breakers   Отримати всі вимикачі 
GET  /api/circuit-breakers/:id  Отримати конкретний вимикач 
POST  /api/circuit-breakers/:id/switch Виконати комутацію вимикача 

23 
 
GET  /api/circuit-breakers/:id/history Історія комутацій 
PUT  /api/circuit-breakers/:id  Оновити параметри вимикача 
DELETE /api/circuit-breakers/:id  Видалити вимикач із системи 
Варіант 12: SCADA система моніторингу 
Об’єкт: REST API для систем диспетчерського управління та збору даних з можливістю 
моніторингу підключених пристроїв, точок даних та тривог. 
Параметри об'єкта: 
Параметр   Тип  Опис 
id    number Ідентифікатор SCADA системи 
systemName   string  Назва SCADA системи 
connectedDevices  number Кількість підключених пристроїв 
dataPointsCount  number Загальна кількість точок даних 
samplingRate   number Частота опитування пристроїв (с) 
alarmLevel   string  Рівень тривог: normal/warning/critical 
communicationStatus  string  Статус зв'язку з пристроями 
lastUpdate   string  Час останнього оновлення даних 
storageUsed   number Використання сховища даних (%) 
Endpoints API: 
GET /api/scada  Отримати дані SCADA системи 
GET /api/scada/devices Список всіх пристроїв 
GET /api/scada/datapoints Список точок даних 
GET /api/scada/alarms Отримати активні тривоги 
POST /api/scada/configure Налаштувати систему 
PUT /api/scada  Оновити параметри SCADA 
Варіант 13: Конденсаторна установка компенсації 
Об’єкт: REST  API  для  управління  пристроями  компенсації  реактивної  потужності  з 
автоматичним або ручним перемиканням ступенів. 
Параметри об'єкта: 
Параметр Тип  Опис 
id  number Унікальний ідентифікатор установки 
name  string  Назва конденсаторної установки 
ratedPower number Номінальна потужність компенсації (кВАр) 
activePower number Поточна задіяна потужність (кВАр) 
stepsCount number Загальна кількість ступенів 
activeSteps number Кількість увімкнених ступенів 
voltage  number Робоча напруга (кВ) 
powerFactor number Коефіцієнт потужності після компенсації 
mode  string  Режим роботи: auto/manual 
Endpoints API: 
GET  /api/capacitor-banks    Отримати всі установки 
GET  /api/capacitor-banks/:id   Отримати конкретну установку 
POST  /api/capacitor-banks/:id/switch-step  Перемкнути ступінь компенсації 
GET  /api/capacitor-banks/:id/compensation Дані компенсації 
PUT  /api/capacitor-banks/:id/mode  Змінити режим роботи 

24 
 
DELETE /api/capacitor-banks/:id   Видалити установку 
Варіант 14: Релейний захист та автоматика (РЗА) 
Об’єкт: REST  API  для  систем  релейного  захисту  електрообладнання  з  моніторингом 
уставок, подій спрацювання та тестування пристроїв. 
Параметри об'єкта: 
Параметр Тип Опис 
id   number Унікальний ідентифікатор пристрою РЗА 
name   string  Назва або позначення пристрою 
protectionType string  Тип захисту: overcurrent/differential/distance 
settings  object  Об'єкт з уставками спрацювання 
status   string  Статус: armed/blocked/triggered 
lastOperation  string  Час останнього спрацювання 
faultType  string  Тип останнього пошкодження 
operationTime  number Час спрацювання захисту (мс) 
eventLog  array  Масив подій та спрацювань 
Endpoints API: 
GET  /api/protection-devices  Отримати всі пристрої РЗА 
GET  /api/protection-devices/:id  Отримати конкретний пристрій 
GET  /api/protection-devices/:id/events Журнал подій пристрою 
POST  /api/protection-devices/:id/test Виконати тестування РЗА 
PUT  /api/protection-devices/:id/settings Змінити уставки захисту 
DELETE /api/protection-devices/:id  Видалити пристрій РЗА 
Варіант 15: Розумна система вуличного освітлення 
Об’єкт: REST  API  для  інтелектуального  управління  вуличним  освітленням  з 
можливістю автоматичного та ручного керування яскравістю. 
Параметри об'єкта: 
Параметр Тип Опис 
id   number Унікальний ідентифікатор системи 
name   string  Назва системи або сегмента освітлення 
lampCount  number Загальна кількість світильників 
activeLamps  number Кількість увімкнених світильників 
totalPower  number Загальна споживана потужність (кВт) 
brightness  number Рівень яскравості світіння (%) 
mode   string  Режим роботи: auto/manual/schedule 
energyConsumed number Спожита енергія за період (кВт·год) 
lightLevel  number Виміряний рівень освітленості (люкс) 
Endpoints API: 
GET  /api/lighting-systems   Отримати всі системи освітлення 
GET  /api/lighting-systems/:id  Отримати конкретну систему 
POST  /api/lighting-systems/:id/control Керування світильниками 
GET  /api/lighting-systems/:id/schedule Розклад роботи системи 
PUT  /api/lighting-systems/:id/brightness Змінити яскравість 
DELETE /api/lighting-systems/:id  Видалити систему 

25 
 
Варіант 16: Система HVAC будівлі 
Об’єкт: REST  API  для  систем  опалення,  вентиляції  та  кондиціонування  з  контролем 
температури, вологості та енергоспоживання. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор системи 
name   string Назва HVAC системи або зони 
indoorTemperature number Температура всередині приміщення (°C) 
outdoorTemperature number Температура зовні будівлі (°C) 
targetTemperature number Задана цільова температура (°C) 
humidity  number Відносна вологість повітря (%) 
powerConsumption number Поточне споживання енергії (кВт) 
mode   string  Режим: heating/cooling/ventilation/off 
fanSpeed  number Швидкість вентилятора (%) 
Endpoints API: 
GET  /api/hvac-systems   Отримати всі HVAC системи 
GET  /api/hvac-systems/:id   Отримати конкретну систему 
POST  /api/hvac-systems/:id/setpoint Встановити цільову температуру 
GET  /api/hvac-systems/:id/efficiency Показники енергоефективності 
PUT  /api/hvac-systems/:id/mode  Змінити режим роботи 
DELETE /api/hvac-systems/:id   Видалити систему 
Варіант 17: Дизель-генераторна установка 
Об’єкт: REST API для резервних дизельних генераторів з моніторингом стану двигуна, 
рівня палива та параметрів генерованої електроенергії. 
Параметри об'єкта: 
Параметр Тип Опис 
Id  number Унікальний ідентифікатор ДГУ 
name  string  Назва дизель-генераторної установки 
ratedPower number Номінальна потужність генератора (кВт) 
currentPower number Поточна генерована потужність (кВт) 
voltage  number Напруга на виході генератора (В) 
frequency number Частота генерованої електроенергії (Гц) 
fuelLevel number Рівень палива в баці (%) 
engineSpeed number Обороти двигуна (об/хв) 
oilPressure number Тиск мастила в двигуні (бар) 
status  string  Статус: standby/running/fault 
Endpoints API: 
GET /api/generators  Отримати всі ДГУ 
GET /api/generators/:id  Отримати конкретну ДГУ 
POST /api/generators/:id/start Запустити генератор 
POST /api/generators/:id/stop Зупинити генератор 
GET /api/generators/:id/fuel Дані про паливо 
PUT /api/generators/:id  Оновити параметри ДГУ 

26 
 
Варіант 18: Аналізатор якості електроенергії 
Об’єкт: REST  API  для  приладів  контролю  якості  електроенергії  з  моніторингом 
відхилень напруги, гармонійних спотворень та подій у мережі. 
Параметри об'єкта: 
Параметр Тип Опис 
id   number Унікальний ідентифікатор аналізатора 
location  string  Місце встановлення приладу 
voltage   number Виміряна напруга в мережі (В) 
frequency  number Частота мережі (Гц) 
thd   number Коефіцієнт гармонічних спотворень THD (%) 
powerFactor  number Коефіцієнт потужності 
voltageDeviation number Відхилення напруги від номіналу (%) 
flickerPst  number Показник фліккера Pst 
unbalance  number Несиметрія напруг (%) 
events   array  Масив подій (провали, перенапруги) 
Endpoints API: 
GET /api/power-quality   Отримати всі аналізатори 
GET /api/power-quality/:id   Отримати конкретний прилад 
GET /api/power-quality/:id/harmonics Гармонічний склад напруги/струму 
GET /api/power-quality/:id/events  Події якості електроенергії 
POST /api/power-quality/:id/report  Згенерувати звіт про якість 
PUT /api/power-quality/:id   Оновити параметри аналізатора 
Варіант 19: Система Demand Response 
Об’єкт: REST API для програм  управління попитом на електроенергію з можливістю 
активації подій зменшення навантаження та контролю економії. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id    number Унікальний ідентифікатор програми 
name   string  Назва програми Demand Response 
participantCount number Кількість учасників програми 
availableCapacity number Доступна для регулювання потужність (МВт) 
activatedLoad  number Активоване навантаження (МВт) 
demandReduction number Фактичне зменшення попиту (%) 
tariffPeriod  string  Тарифний період: peak/off-peak/shoulder 
eventStatus  string  Статус події: active/inactive/scheduled 
savings  number Економія коштів (грн) 
Endpoints API: 
GET /api/demand-response Отримати всі DR програми 
GET /api/demand-response/:id Отримати конкретну програму 
POST /api/demand-response/:id/activate Активувати подію DR 
GET /api/demand-response/:id/participants Список учасників 
GET /api/demand-response/:id/savings Дані про економію 
PUT /api/demand-response/:id Оновити параметри програми 

27 
 
Варіант 20: Мікрогрід (Автономна мікромережа) 
Об’єкт: REST  API  для  управління  автономними  мікромережами  з  балансуванням 
генерації, навантаження та обміну з основною мережею. 
Параметри об'єкта: 
Параметр Тип Опис 
id   number Унікальний ідентифікатор мікромережі 
name  string  Назва мікрогріда 
mode  string  Режим роботи: grid-connected/islanded 
generation number Загальна генерація в мікромережі (кВт) 
load  number Навантаження споживачів (кВт) 
storage  number Стан накопичувачів енергії (кВт·год) 
gridImport number Імпорт з основної мережі (кВт) 
gridExport number Експорт в основну мережу (кВт) 
frequency number Частота в мікромережі (Гц) 
voltage  number Напруга в мікромережі (В) 
Endpoints API: 
GET /api/microgrids  Отримати всі мікромережі 
GET /api/microgrids/:id  Отримати конкретну мікромережу 
GET /api/microgrids/:id/balance Енергобаланс мікромережі 
POST /api/microgrids/:id/mode Змінити режим роботи 
GET /api/microgrids/:id/forecast Прогноз генерації та споживання 
PUT /api/microgrids/:id  Оновити параметри мікромережі 
Варіант 21: Система автоматизованого обліку АСКОЕ 
Об’єкт: REST API для систем комерційного обліку електроенергії з аналізом даних від 
великої кількості лічильників та формуванням розрахункових документів. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id    number Унікальний ідентифікатор системи 
systemName  string  Назва системи обліку 
meterCount  number Загальна кількість лічильників у системі 
dataCompleteness number Повнота отриманих даних (%) 
activeEnergy  number Облікована активна енергія (МВт·год) 
reactiveEnergy number Облікована реактивна енергія (МВАр·год) 
peakDemand  number Пікове навантаження за період (МВт) 
billingPeriod  string  Розрахунковий період (YYYY-MM) 
revenue  number Очікувана виручка за період (грн) 
Endpoints API: 
GET /api/metering-system   Отримати дані системи обліку 
GET /api/metering-system/meters  Список всіх лічильників 
GET /api/metering-system/consumption Агреговані дані споживання 
GET /api/metering-system/billing  Розрахункові дані та звіти 
POST /api/metering-system/readings Завантажити покази лічильників 
PUT /api/metering-system   Оновити параметри системи 

28 
 
Варіант 22: Інвертор для сонячних панелей 
Об’єкт: REST  API  для  мережевих  інверторів  фотоелектричних  систем  з  контролем 
перетворення постійного струму в змінний та показників ефективності. 
Параметри об'єкта: 
Параметр Тип Опис 
id   number Унікальний ідентифікатор інвертора 
serialNumber string  Серійний номер пристрою 
manufacturer string  Виробник інвертора 
ratedPower number Номінальна потужність інвертора (кВт) 
dcVoltage number Вхідна напруга постійного струму (В) 
dcCurrent number Вхідний струм постійний (А) 
acVoltage number Вихідна напруга змінного струму (В) 
acCurrent number Вихідний струм змінний (А) 
efficiency number Поточна ефективність перетворення (%) 
temperature number Температура інвертора (°C) 
status  string  Статус роботи: operating/standby/fault 
Endpoints API: 
GET  /api/inverters    Отримати всі інвертори 
GET  /api/inverters/:id   Отримати конкретний інвертор 
GET  /api/inverters/:id/performance Показники роботи та ефективності 
GET  /api/inverters/:id/faults  Історія помилок та несправностей 
PUT  /api/inverters/:id/settings  Налаштування параметрів інвертора 
DELETE /api/inverters/:id   Видалити інвертор із системи 
Варіант 23: Система моніторингу трансформаторів 
Об’єкт: REST  API  для  діагностики  силових  трансформаторів  з  контролем 
температурного режиму, якості масла та електричних параметрів. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор трансформатора 
name   string  Позначення трансформатора 
ratedPower  number Номінальна потужність трансформатора (МВА) 
oilTemperature number Температура трансформаторного масла (°C) 
windingTemperature number Температура обмотки трансформатора (°C) 
tapPosition  number Поточне положення РПН (регулятора напруги) 
oilLevel  number Рівень масла в розширювачі (%) 
moisture  number Вміст вологи в маслі (ppm) 
dissolvedGases object  Концентрація розчинених газів (ppm) 
partialDischarge number Рівень часткових розрядів (пКл) 
Endpoints API: 
GET /api/transformer-monitoring    Отримати всі трансформатори 
GET /api/transformer-monitoring/:id   Отримати конкретний 
трансформатор 
GET /api/transformer-monitoring/:id/diagnostics  Діагностичні дані та аналіз стану 
GET /api/transformer-monitoring/:id/oil-analysis  Результати аналізу масла 
POST /api/transformer-monitoring/:id/alarm  Зареєструвати тривожну подію 

29 
 
PUT /api/transformer-monitoring/:id   Оновити параметри моніторингу 
Варіант 24: Система прогнозування навантаження 
Об’єкт: REST API для короткострокового прогнозування електричного навантаження з 
урахуванням метеоданих, типу дня та історичних трендів. 
Параметри об'єкта: 
Параметр Тип Опис 
id   number Унікальний ідентифікатор системи прогнозування 
region   string  Регіон або зона прогнозування 
currentLoad  number Поточне фактичне навантаження (МВт) 
forecastHorizon number Горизонт прогнозування (години) 
predictedLoad  number Прогнозоване навантаження (МВт) 
temperature  number Температура повітря для прогнозу (°C) 
dayType  string  Тип дня: workday/weekend/holiday 
accuracy  number Історична точність прогнозів (%) 
lastUpdate  string  Час останнього оновлення прогнозу 
Endpoints API: 
GET  /api/load-forecast  Отримати всі прогнози навантаження 
GET  /api/load-forecast/:region  Отримати прогноз для регіону 
GET  /api/load-forecast/:region/hourly Погодинний детальний прогноз 
GET  /api/load-forecast/:region/accuracy Метрики точності прогнозування 
POST  /api/load-forecast/:region/update Оновити прогнозну модель 
DELETE /api/load-forecast/:region  Видалити прогноз для регіону 
Варіант 25: Система управління енергетичними активами EAM 
Об’єкт: REST  API  для  управління  життєвим  циклом  енергетичного  обладнання  з 
плануванням технічного обслуговування та контролем надійності. 
Параметри об'єкта: 
Параметр Тип Опис 
id    number Унікальний ідентифікатор активу 
assetType   string  Тип активу: transformer/breaker/line/generator 
name    string  Назва або позначення активу 
location   string  Місцезнаходження активу 
commissionDate  string  Дата введення в експлуатацію (ISO 8601) 
condition   string  Технічний стан: good/fair/poor/critical 
maintenanceSchedule  string  Графік обслуговування: monthly/quarterly/yearly 
lastMaintenance  string  Дата останнього ТО (ISO 8601) 
reliability   number Показник надійності активу (%) 
replacementCost  number Орієнтовна вартість заміни (грн) 
Endpoints API: 
GET  /api/asset-management   Отримати всі активи 
GET  /api/asset-management/:id   Отримати конкретний актив 
GET  /api/asset-management/:id/history  Історія експлуатації та ТО 
POST  /api/asset-management/:id/maintenance Запланувати обслуговування 
PUT  /api/asset-management/:id/condition  Оновити технічний стан 
DELETE /api/asset-management/:id   Видалити актив зі списку 

30 
 
Варіант 26: Система контролю втрат електроенергії 
Об’єкт: REST  API  для  аналізу  та  мінімізації  технологічних  і  комерційних  втрат 
електроенергії в розподільних мережах. 
Параметри об'єкта: 
Параметр Тип Опис 
id   number Унікальний ідентифікатор об'єкта контролю 
objectName  string  Назва об'єкта (підстанція, фідер, лінія) 
inputEnergy  number Вхідна електроенергія за період (кВт·год) 
outputEnergy  number Вихідна/відпущена електроенергія (кВт·год) 
technicalLosses number Розраховані технічні втрати (кВт·год) 
commercialLosses number Комерційні втрати (кВт·год) 
lossPercentage  number Загальний відсоток втрат (%) 
calculationMethod string  Метод розрахунку: measured/calculated/estimated 
period   string  Період аналізу: hour/day/month/year 
Endpoints API: 
GET /api/loss-control   Отримати всі об'єкти контролю втрат 
GET /api/loss-control/:id   Отримати конкретний об'єкт 
GET /api/loss-control/:id/analysis  Детальний аналіз структури втрат 
GET /api/loss-control/:id/trends  Динаміка втрат за періоди 
POST /api/loss-control/:id/calculate  Розрахувати втрати за період 
PUT /api/loss-control/:id   Оновити параметри контролю 
Варіант 27: Система моніторингу повітряних ліній 
Об’єкт: REST  API  для  онлайн-моніторингу  стану  повітряних  ліній  електропередачі  з 
контролем температури проводів, провисання та метеоумов. 
Параметри об'єкта: 
Параметр   Тип  Опис 
id    number Унікальний ідентифікатор лінії 
lineName   string  Назва або номер повітряної лінії 
voltage    number Клас напруги лінії (кВ) 
length    number Довжина лінії (км) 
conductorTemperature number Температура проводу (°C) 
sag    number Стріла провисання проводу (м) 
iceLoad   number Маса ожеледного навантаження (кг/м) 
windSpeed   number Швидкість вітру вздовж лінії (м/с) 
current    number Струм навантаження лінії (А) 
towerCondition  string  Стан опор: good/inspection_required/damaged 
Endpoints API: 
GET /api/transmission-lines   Отримати всі повітряні лінії 
GET /api/transmission-lines/:id   Отримати конкретну лінію 
GET /api/transmission-lines/:id/temperature Температурний моніторинг проводу 
GET /api/transmission-lines/:id/weather  Метеорологічні дані вздовж траси 
POST /api/transmission-lines/:id/inspection Записати результати огляду 
PUT /api/transmission-lines/:id   Оновити параметри лінії 

31 
 
Варіант 28: Біогазова когенераційна установка 
Об’єкт: REST  API  для  біогазових  електростанцій  з  контролем  процесу  ферментації, 
виробництва біогазу та комбінованої генерації електроенергії і тепла. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор БГУ 
name   string  Назва біогазової установки 
electricPower  number Електрична потужність когенератора (кВт) 
thermalPower  number Теплова потужність когенератора (кВт) 
biogasProduction number Вироблення біогазу (м³/год) 
methaneContent number Вміст метану в біогазі (%) 
substrateType  string  Тип органічної сировини 
feedRate  number Швидкість подачі субстрату (т/добу) 
digesterTemperature number Температура в реакторі (°C) 
efficiency  number Загальна ефективність установки (%) 
Endpoints API: 
GET /api/biogas-plants   Отримати всі біогазові установки 
GET /api/biogas-plants/:id   Отримати конкретну установку 
GET /api/biogas-plants/:id/production Дані виробництва біогазу та енергії 
GET /api/biogas-plants/:id/substrate Інформація про субстрат та подачу 
POST /api/biogas-plants/:id/readings Записати технологічні покази 
PUT /api/biogas-plants/:id   Оновити параметри установки 
Варіант 29: Система управління будівлею BMS 
Об’єкт: REST  API  для  комплексного  енергоменеджменту  будівель  з  контролем  всіх 
інженерних систем та оптимізацією енергоспоживання. 
Параметри об'єкта: 
Параметр   Тип  Опис 
Id    number Унікальний ідентифікатор будівлі 
buildingName   string  Назва або адреса будівлі 
totalArea   number Загальна площа будівлі (м²) 
electricityConsumption number Споживання електроенергії за період (кВт·год) 
gasConsumption  number Споживання природного газу (м³) 
waterConsumption  number Споживання води (м³) 
indoorTemperature  number Середня температура в будівлі (°C) 
occupancy   number Рівень заповненості будівлі (%) 
lightingLevel   number Рівень освітлення приміщень (%) 
energyEfficiency  string  Клас енергоефективності: A/B/C/D/E 
Endpoints API: 
GET /api/building-management  Отримати всі будівлі в системі 
GET /api/building-management/:id  Отримати конкретну будівлю 
GET /api/building-management/:id/consumption Детальні дані споживання ресурсів 
GET /api/building-management/:id/comfort Параметри комфорту мешканців 
POST /api/building-management/:id/optimize Запустити оптимізацію режимів 
PUT /api/building-management/:id  Оновити дані будівлі 

32 
 
Варіант 30: Віртуальна електростанція VPP 
Об’єкт: REST  API  для  агрегації  розподіленої  генерації  та  керованого  навантаження  з 
оптимізацією роботи портфелю ресурсів та участю на ринках електроенергії. 
Параметри об'єкта: 
Параметр  Тип  Опис 
id   number Унікальний ідентифікатор VPP 
name   string  Назва віртуальної електростанції 
aggregatedCapacity number Загальна агрегована потужність (МВт) 
activeResources number Кількість активних ресурсів у портфелі 
solarGeneration number Генерація від сонячних джерел (МВт) 
windGeneration number Генерація від вітрових джерел (МВт) 
storageCapacity number Доступна ємність накопичення (МВт·год) 
demandResponse number Потужність керованого навантаження (МВт) 
marketBids  number Кількість активних ринкових заявок 
revenue  number Виручка від діяльності VPP (грн) 
Endpoints API: 
GET /api/virtual-power-plants   Отримати всі VPP в системі 
GET /api/virtual-power-plants/:id   Отримати конкретну VPP 
GET /api/virtual-power-plants/:id/resources Список ресурсів у портфелі VPP 
GET /api/virtual-power-plants/:id/dispatch План диспетчеризації ресурсів 
POST /api/virtual-power-plants/:id/optimize Оптимізувати портфель VPP 
PUT /api/virtual-power-plants/:id   Оновити параметри VPP 
Додаток Б. Приклади команд curl 
bash: 
# GET запит 
curl http://localhost:3000/api/substations 
 
# POST з даними 
curl -X POST http://localhost:3000/api/substations \ 
  -H "Content-Type: application/json" \ 
  -d '{"name":"Test","voltage":110}' 
 
# PUT оновлення 
curl -X PUT http://localhost:3000/api/substations/1 \ 
  -H "Content-Type: application/json" \ 
  -d '{"name":"Updated","voltage":110}' 
 
# PATCH часткове оновлення 
curl -X PATCH http://localhost:3000/api/substations/1 \ 
  -H "Content-Type: application/json" \ 
  -d '{"temperature":75}' 
 
# DELETE 
curl -X DELETE http://localhost:3000/api/substations/1
