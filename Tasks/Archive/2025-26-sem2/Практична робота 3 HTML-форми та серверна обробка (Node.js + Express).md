---
course: "Веб-програмування: Практичні"
type: практика
due: 2026-04-05
status: done
year: 2
semester: 2
period: 2025-26
---
# Практична робота 3 HTML-форми та серверна обробка (Node.js + Express)

**Курс:** Основи Веб-програмування ТВ-43: 2-й Семестр 2025/26 навчального року
**Дедлайн:** 5 квіт.

## Вкладення

- 📎 _ОВП Практична робота 3 v_2025_11_24.pdf

## Google Classroom

[Відкрити завдання](https://classroom.google.com/u/0/c/ODE4NTM3MzA5OTg0/a/ODMyMzY0MjQxODQx/details)

---

## 📄 _ОВП Практична робота 3 v_2025_11_24.pdf

1 
 
МІНІСТЕРСТВО ОСВІТИ І НАУКИ УКРАЇНИ 
НАЦІОНАЛЬНИЙ ТЕХНІЧНИЙ УНІВЕРСИТЕТ УКРАЇНИ 
«КИЇВСЬКИЙ ПОЛІТЕХНІЧНИЙ ІНСТИТУТ ІМЕНІ ІГОРЯ СІКОРСЬКОГО» 
 
 
 
 
 
 
 
 
 
 
ОСНОВИ ВЕБ-ПРОГРАМУВАННЯ 
 
 
Практична робота No3 
(практичні заняття 7 - 9) 
 
 
 
 
 
 
 
 
 
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
 
ПРАКТИЧНА РОБОТА No3 (практичні заняття 7 - 9). HTML-
форми та серверна обробка (Node.js + Express). 
 
ЗМІСТ 
ПРАКТИЧНА РОБОТА No3 (практичні заняття 7 - 9). HTML-форми та серверна обробка 
(Node.js + Express). ................................................................................................................................. 2 
План практичної роботи No3: HTML-форми та серверна обробка (Node.js + Express). .............. 3 
Практичне заняття No7: проєктування HTML-форми та серверної обробки (Node.js + 
Express) ............................................................................................................................................. 3 
Практичне заняття No8: реалізація HTML-форми та серверної обробки (Node.js + Express) . 3 
Практичне заняття No9: тестування HTML-форми та серверної обробки (Node.js + Express) 3 
Загальна інформація ........................................................................................................................... 3 
3.1. Теоретичний матеріал ................................................................................................................. 3 
3.1.1. HTML-форми ......................................................................................................................... 3 
3.1.2. Node.js та Express .................................................................................................................. 3 
3.1.3. Обробка даних форм ............................................................................................................. 3 
3.1.4. Збереження даних ................................................................................................................. 4 
3.2. Приклад повної реалізації ........................................................................................................... 4 
3.2.1. Завдання ................................................................................................................................. 4 
2.2.2. Виконання .............................................................................................................................. 4 
3.3. Структура звіту до практичної роботи .................................................................................... 18 
3.3.1. Титульна сторінка ............................................................................................................... 18 
3.3.2. Мета роботи ......................................................................................................................... 18 
3.3.3. Теоретична частина ............................................................................................................ 18 
3.3.4. Опис реалізації .................................................................................................................... 19 
3.3.5. Тестування ........................................................................................................................... 19 
3.3.6. Висновки .............................................................................................................................. 19 
3.3.7. Список використаних джерел ............................................................................................ 19 
3.3.8. Додатки ................................................................................................................................ 19 
3.4. Критерії оцінювання ................................................................................................................. 19 
3.4.1. Реалізація мінімального функціоналу (60 балів) ............................................................. 19 
3.4.2. Реалізація основного функціоналу (20 балів) .................................................................. 19 
3.4.3. Реалізація додаткового функціоналу (20 балів) ............................................................... 19 
3.5. Контрольні питання ................................................................................................................... 20 
Список рекомендованої літератури ................................................................................................ 20 
Перелік посилань .............................................................................................................................. 20 
Додатки .............................................................................................................................................. 21 
Додаток А. Варіанти індивідуальних завдань ............................................................................ 21 
Додаток Б. Додаткові завдання .................................................................................................... 28 
 
 
 
 
 
 

3 
 
План практичної роботи No3: HTML-форми та серверна обробка 
(Node.js + Express). 
Практичне заняття No7: проєктування HTML-форми та серверної обробки (Node.js 
+ Express) 
Проєктування форми збору даних та організація її обробки на сервері (напр., створення 
сайту для реєстрації споживачів енергії або обліку генерації, з формою, що містить: ім’я; тип 
об’єкта; адреса; параметри підключення; запис даних у JSON або БД). 
Практичне заняття No8: реалізація HTML-форми та серверної обробки (Node.js + 
Express) 
Реалізація форми  збору  даних  та  організація  її  обробки  на сервері  (напр.,  створення 
сайту для реєстрації споживачів енергії або обліку генерації, з формою, що містить: ім’я; тип 
об’єкта; адреса; параметри підключення; запис даних у JSON або БД). 
Практичне заняття No9: тестування HTML-форми та серверної обробки (Node.js + 
Express) 
Тестування та оформлення звіту з реалізації форми збору даних та організація її обробки 
на сервері  (напр., створення  сайту  для  реєстрації  споживачів  енергії  або  обліку генерації,  з 
формою, що містить: ім’я; тип об’єкта; адреса; параметри підключення; запис даних у JSON 
або БД). 
Загальна інформація 
Мета: Навчитися створювати HTML-форми  для  збору даних енергетичних об'єктів та 
організовувати їх обробку на сервері за допомогою Node.js та Express. 
Завдання: 
1.  Спроєктувати  структуру форми  збору  даних  та  організація  її  обробки  на  сервері  у 
відповідності з індивідуальним варіантом завдання. 
2. Реалізувати форми збору даних та організація її обробки на сервері у відповідності з 
індивідуальним варіантом завдання 
3.  Протестувати  роботу форми  збору  даних  та  організація  її  обробки  на  сервері  у 
відповідності з індивідуальним варіантом завдання 
Тривалість: 6 годин (3 заняття по 2 години) 
3.1. Теоретичний матеріал 
3.1.1. HTML-форми 
HTML-форми є основним способом збору даних від користувачів. Основні елементи: 
&lt;form> - контейнер форми 
&lt;input> - поля введення (text, number, date тощо) 
&lt;select> - випадаючі списки 
&lt;textarea> - багаторядкові текстові поля 
&lt;button> - кнопки для відправки/очищення 
3.1.2. Node.js та Express 
Node.js - середовище виконання JavaScript на сервері. 
Express - мінімалістичний веб-фреймворк для Node.js. 
3.1.3. Обробка даних форм 
Для обробки даних форм використовують middleware: 

4 
 
- express.urlencoded() - парсинг даних форм 
- express.json() - парсинг JSON даних 
- express.static() - обслуговування статичних файлів 
3.1.4. Збереження даних 
Варіанти збереження на сервері: 
- JSON файли - просто, без БД 
- PostgreSQL - реляційна БД 
- MongoDB - документо-орієнтована БД 
3.2. Приклад повної реалізації 
3.2.1. Завдання 
Назва об'єкта: Сайт для реєстрації споживачів енергії 
Основні вимоги: 
Розробити  форму  збору  даних  та  організувати  її  обробку  на  сервері  для  сайту для 
реєстрації споживачів енергії з формою, що містить: 
- ім’я; 
- тип об’єкта; 
- адреса; 
- параметри підключення; 
- запис даних у JSON або БД. 
2.2.2. Виконання 
2.2.2.1. Структура проєкту 
project/ 
│ 
├── server.js          # Серверний код 
├── public/           # Статичні файли 
│   ├── index.html   # HTML-форма 
│   ├── style.css    # Стилі 
│   └── script.js    # Клієнтський JS 
├── data/ 
│   └── consumers.json # Файл для збереження даних 
└── package.json      # Залежності проєкту 
2.2.2.1.1. Ініціалізація проєкту (package.json) 
json: 
{ 
  "name": "energy-consumers-registry", 
  "version": "1.0.0", 
  "description": "Реєстрація споживачів енергії", 
  "main": "server.js", 
  "scripts": { 
    "start": "node server.js", 
    "dev": "nodemon server.js" 
  }, 

5 
 
  "dependencies": { 
    "express": "^4.18.2" 
  }, 
  "devDependencies": { 
    "nodemon": "^3.0.1" 
  } 
} 
 
2.2.2.1.2. Встановлення залежностей: 
bash: 
npm install 
 
2.2.2.1.3. Серверний код (server.js) 
javascript: 
const express = require('express'); 
const fs = require('fs'); 
const path = require('path'); 
 
const app = express(); 
const PORT = 3000; 
 
// Middleware 
app.use(express.json()); 
app.use(express.urlencoded({ extended: true })); 
app.use(express.static('public')); 
 
// Шлях до файлу даних 
const DATA_FILE = path.join(__dirname, 'data', 'consumers.json'); 
 
// Допоміжна функція для читання даних 
function readData() { 
  try { 
    if (!fs.existsSync(DATA_FILE)) { 
      return []; 
    } 
    const data = fs.readFileSync(DATA_FILE, 'utf8'); 
    return JSON.parse(data); 
  } catch (error) { 
    console.error('Помилка читання даних:', error); 
    return []; 
  } 
} 
 

6 
 
// Допоміжна функція для запису даних 
function writeData(data) { 
  try { 
    const dir = path.dirname(DATA_FILE); 
    if (!fs.existsSync(dir)) { 
      fs.mkdirSync(dir, { recursive: true }); 
    } 
    fs.writeFileSync(DATA_FILE, JSON.stringify(data, null, 2)); 
    return true; 
  } catch (error) { 
    console.error('Помилка запису даних:', error); 
    return false; 
  } 
} 
 
// Маршрут для отримання всіх споживачів 
app.get('/api/consumers', (req, res) => { 
  const consumers = readData(); 
  res.json(consumers); 
}); 
 
// Маршрут для додавання нового споживача 
app.post('/api/consumers', (req, res) => { 
  try { 
    const newConsumer = { 
      id: Date.now().toString(), 
      name: req.body.name, 
      objectType: req.body.objectType, 
      address: req.body.address, 
      connectionPower: req.body.connectionPower, 
      voltage: req.body.voltage, 
      phase: req.body.phase, 
      registrationDate: new Date().toISOString() 
    }; 
 
    const consumers = readData(); 
    consumers.push(newConsumer); 
     
    if (writeData(consumers)) { 
      res.status(201).json({ 
        success: true, 
        message: 'Споживача успішно зареєстровано', 
        data: newConsumer 
      }); 
    } else { 

7 
 
      throw new Error('Помилка запису даних'); 
    } 
  } catch (error) { 
    res.status(500).json({ 
      success: false, 
      message: 'Помилка реєстрації споживача', 
      error: error.message 
    }); 
  } 
}); 
 
// Маршрут для видалення споживача 
app.delete('/api/consumers/:id', (req, res) => { 
  try { 
    const consumers = readData(); 
    const filteredConsumers = consumers.filter(c => c.id !== req.params.id); 
     
    if (writeData(filteredConsumers)) { 
      res.json({ 
        success: true, 
        message: 'Споживача видалено' 
      }); 
    } else { 
      throw new Error('Помилка запису даних'); 
    } 
  } catch (error) { 
    res.status(500).json({ 
      success: false, 
      message: 'Помилка видалення споживача' 
    }); 
  } 
}); 
 
// Запуск сервера 
app.listen(PORT, () => { 
  console.log(`Сервер запущено на http://localhost:${PORT}`); 
}); 
 
2.2.2.1.4. HTML-форма (public/index.html) 
html: 
&lt;!DOCTYPE html> 
&lt;html lang="uk"> 
&lt;head> 
    &lt;meta charset="UTF-8"> 

8 
 
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    &lt;title>Реєстрація споживачів енергії&lt;/title> 
    &lt;link rel="stylesheet" href="style.css"> 
&lt;/head> 
&lt;body> 
    &lt;div class="container"> 
        &lt;header> 
            &lt;h1>⚡ Реєстр споживачів електроенергії&lt;/h1> 
        &lt;/header> 
 
        &lt;main> 
            &lt;section class="form-section"> 
                &lt;h2>Реєстрація нового споживача&lt;/h2> 
                &lt;form id="consumerForm"> 
                    &lt;div class="form-group"> 
                        &lt;label for="name">Повне найменування об'єкта *&lt;/label> 
                        &lt;input type="text" id="name" name="name" required  
                               placeholder="Наприклад: ТОВ 'Енергопром'"> 
                    &lt;/div> 
 
                    &lt;div class="form-group"> 
                        &lt;label for="objectType">Тип об'єкта *&lt;/label> 
                        &lt;select id="objectType" name="objectType" required> 
                            &lt;option value="">Оберіть тип&lt;/option> 
                            &lt;option value="industrial">Промисловий об'єкт&lt;/option> 
                            &lt;option value="residential">Житловий будинок&lt;/option> 
                            &lt;option value="commercial">Комерційний об'єкт&lt;/option> 
                            &lt;option value="public">Об'єкт соціальної сфери&lt;/option> 
                            &lt;option value="agricultural">Сільськогосподарський об'єкт&lt;/option> 
                        &lt;/select> 
                    &lt;/div> 
 
                    &lt;div class="form-group"> 
                        &lt;label for="address">Адреса підключення *&lt;/label> 
                        &lt;textarea id="address" name="address" required  
                                  placeholder="Повна адреса з індексом">&lt;/textarea> 
                    &lt;/div> 
 
                    &lt;div class="form-row"> 
                        &lt;div class="form-group"> 
                            &lt;label for="connectionPower">Потужність підключення (кВт) *&lt;/label> 
                            &lt;input type="number" id="connectionPower" name="connectionPower"  
                                   required min="0" step="0.1" placeholder="100"> 
                        &lt;/div> 
 

9 
 
                        &lt;div class="form-group"> 
                            &lt;label for="voltage">Напруга живлення (кВ) *&lt;/label> 
                            &lt;select id="voltage" name="voltage" required> 
                                &lt;option value="">Оберіть напругу&lt;/option> 
                                &lt;option value="0.4">0,4 кВ (низька)&lt;/option> 
                                &lt;option value="6">6 кВ (середня)&lt;/option> 
                                &lt;option value="10">10 кВ (середня)&lt;/option> 
                                &lt;option value="35">35 кВ (висока)&lt;/option> 
                                &lt;option value="110">110 кВ (висока)&lt;/option> 
                            &lt;/select> 
                        &lt;/div> 
                    &lt;/div> 
 
                    &lt;div class="form-group"> 
                        &lt;label for="phase">Кількість фаз *&lt;/label> 
                        &lt;div class="radio-group"> 
                            &lt;label> 
                                &lt;input type="radio" name="phase" value="1" required> Однофазне 
                            &lt;/label> 
                            &lt;label> 
                                &lt;input type="radio" name="phase" value="3" required> Трифазне 
                            &lt;/label> 
                        &lt;/div> 
                    &lt;/div> 
 
                    &lt;div class="form-actions"> 
                        &lt;button type="submit" class="btn btn-primary">Зареєструвати&lt;/button> 
                        &lt;button type="reset" class="btn btn-secondary">Очистити&lt;/button> 
                    &lt;/div> 
                &lt;/form> 
 
                &lt;div id="message" class="message">&lt;/div> 
            &lt;/section> 
 
            &lt;section class="data-section"> 
                &lt;h2>Зареєстровані споживачі&lt;/h2> 
                &lt;div id="consumersList" class="consumers-list">&lt;/div> 
            &lt;/section> 
        &lt;/main> 
    &lt;/div> 
 
    &lt;script src="script.js">&lt;/script> 
&lt;/body> 
&lt;/html> 

10 
 
2.2.2.1.5. Стилі (public/style.css) 
css: 
* { 
    margin: 0; 
    padding: 0; 
    box-sizing: border-box; 
} 
 
body { 
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
    min-height: 100vh; 
    padding: 20px; 
} 
 
.container { 
    max-width: 1200px; 
    margin: 0 auto; 
} 
 
header { 
    background: white; 
    padding: 20px; 
    border-radius: 10px; 
    margin-bottom: 20px; 
    box-shadow: 0 4px 6px rgba(0,0,0,0.1); 
} 
 
header h1 { 
    color: #667eea; 
    text-align: center; 
} 
 
main { 
    display: grid; 
    grid-template-columns: 1fr 1fr; 
    gap: 20px; 
} 
 
section { 
    background: white; 
    padding: 30px; 
    border-radius: 10px; 
    box-shadow: 0 4px 6px rgba(0,0,0,0.1); 
} 

11 
 
 
h2 { 
    color: #333; 
    margin-bottom: 20px; 
    padding-bottom: 10px; 
    border-bottom: 2px solid #667eea; 
} 
 
.form-group { 
    margin-bottom: 20px; 
} 
 
label { 
    display: block; 
    margin-bottom: 8px; 
    color: #555; 
    font-weight: 500; 
} 
 
input[type="text"], 
input[type="number"], 
select, 
textarea { 
    width: 100%; 
    padding: 12px; 
    border: 2px solid #e0e0e0; 
    border-radius: 6px; 
    font-size: 14px; 
    transition: border-color 0.3s; 
} 
 
input:focus, 
select:focus, 
textarea:focus { 
    outline: none; 
    border-color: #667eea; 
} 
 
textarea { 
    resize: vertical; 
    min-height: 80px; 
} 
 
.form-row { 
    display: grid; 

12 
 
    grid-template-columns: 1fr 1fr; 
    gap: 15px; 
} 
 
.radio-group { 
    display: flex; 
    gap: 20px; 
} 
 
.radio-group label { 
    display: flex; 
    align-items: center; 
    gap: 8px; 
    font-weight: normal; 
} 
 
.form-actions { 
    display: flex; 
    gap: 10px; 
    margin-top: 25px; 
} 
 
.btn { 
    padding: 12px 30px; 
    border: none; 
    border-radius: 6px; 
    font-size: 16px; 
    cursor: pointer; 
    transition: all 0.3s; 
} 
 
.btn-primary { 
    background: #667eea; 
    color: white; 
} 
 
.btn-primary:hover { 
    background: #5568d3; 
    transform: translateY(-2px); 
    box-shadow: 0 4px 8px rgba(102, 126, 234, 0.4); 
} 
 
.btn-secondary { 
    background: #f0f0f0; 
    color: #333; 

13 
 
} 
 
.btn-secondary:hover { 
    background: #e0e0e0; 
} 
 
.btn-delete { 
    padding: 6px 12px; 
    background: #ff4444; 
    color: white; 
    font-size: 14px; 
} 
 
.btn-delete:hover { 
    background: #cc0000; 
} 
 
.message { 
    margin-top: 20px; 
    padding: 15px; 
    border-radius: 6px; 
    display: none; 
} 
 
.message.success { 
    background: #d4edda; 
    color: #155724; 
    border: 1px solid #c3e6cb; 
    display: block; 
} 
 
.message.error { 
    background: #f8d7da; 
    color: #721c24; 
    border: 1px solid #f5c6cb; 
    display: block; 
} 
 
.consumers-list { 
    display: flex; 
    flex-direction: column; 
    gap: 15px; 
} 
 
.consumer-card { 

14 
 
    border: 2px solid #e0e0e0; 
    border-radius: 8px; 
    padding: 15px; 
    transition: all 0.3s; 
} 
 
.consumer-card:hover { 
    border-color: #667eea; 
    box-shadow: 0 2px 8px rgba(102, 126, 234, 0.2); 
} 
 
.consumer-card h3 { 
    color: #667eea; 
    margin-bottom: 10px; 
} 
 
.consumer-card p { 
    margin: 5px 0; 
    color: #666; 
} 
 
.consumer-card .label { 
    font-weight: 600; 
    color: #333; 
} 
 
@media (max-width: 968px) { 
    main { 
        grid-template-columns: 1fr; 
    } 
     
    .form-row { 
        grid-template-columns: 1fr; 
    } 
} 
2.2.2.1.6. Клієнтський JavaScript (public/script.js) 
javascript: 
// Отримання елементів 
const form = document.getElementById('consumerForm'); 
const messageDiv = document.getElementById('message'); 
const consumersList = document.getElementById('consumersList'); 
 
// Завантаження списку споживачів при завантаженні сторінки 
document.addEventListener('DOMContentLoaded', loadConsumers); 

15 
 
 
// Обробка відправки форми 
form.addEventListener('submit', async (e) => { 
    e.preventDefault(); 
     
    const formData = new FormData(form); 
    const data = Object.fromEntries(formData); 
     
    try { 
        const response = await fetch('/api/consumers', { 
            method: 'POST', 
            headers: { 
                'Content-Type': 'application/json' 
            }, 
            body: JSON.stringify(data) 
        }); 
         
        const result = await response.json(); 
         
        if (result.success) { 
            showMessage('success', result.message); 
            form.reset(); 
            loadConsumers(); 
        } else { 
            showMessage('error', result.message); 
        } 
    } catch (error) { 
        showMessage('error', 'Помилка з\'єднання з сервером'); 
        console.error('Error:', error); 
    } 
}); 
 
// Завантаження списку споживачів 
async function loadConsumers() { 
    try { 
        const response = await fetch('/api/consumers'); 
        const consumers = await response.json(); 
         
        displayConsumers(consumers); 
    } catch (error) { 
        console.error('Error loading consumers:', error); 
    } 
} 
 
// Відображення споживачів 

16 
 
function displayConsumers(consumers) { 
    if (consumers.length === 0) { 
        consumersList.innerHTML   =   '&lt;p   style="color:   #999;">Немає   зареєстрованих 
споживачів&lt;/p>'; 
        return; 
    } 
     
    consumersList.innerHTML = consumers.map(consumer => ` 
        &lt;div class="consumer-card"> 
            &lt;h3>${consumer.name}&lt;/h3> 
            &lt;p>&lt;span class="label">Тип:&lt;/span> 
${getObjectTypeName(consumer.objectType)}&lt;/p> 
            &lt;p>&lt;span class="label">Адреса:&lt;/span> ${consumer.address}&lt;/p> 
            &lt;p>&lt;span class="label">Потужність:&lt;/span> ${consumer.connectionPower} кВт&lt;/p> 
            &lt;p>&lt;span class="label">Напруга:&lt;/span> ${consumer.voltage} кВ&lt;/p> 
            &lt;p>&lt;span  class="label">Фази:&lt;/span>  ${consumer.phase  ===  '1'  ?  'Однофазне'  : 
'Трифазне'}&lt;/p> 
            &lt;p>&lt;span class="label">Дата реєстрації:&lt;/span> ${new 
Date(consumer.registrationDate).toLocaleDateString('uk-UA')}&lt;/p> 
            &lt;button class="btn btn-delete" 
onclick="deleteConsumer('${consumer.id}')">Видалити&lt;/button> 
        &lt;/div> 
    `).join(''); 
} 
 
// Видалення споживача 
async function deleteConsumer(id) { 
    if (!confirm('Ви впевнені, що хочете видалити цього споживача?')) { 
        return; 
    } 
     
    try { 
        const response = await fetch(`/api/consumers/${id}`, { 
            method: 'DELETE' 
        }); 
         
        const result = await response.json(); 
         
        if (result.success) { 
            showMessage('success', result.message); 
            loadConsumers(); 
        } else { 
            showMessage('error', 'Помилка видалення'); 
        } 
    } catch (error) { 

17 
 
        showMessage('error', 'Помилка з\'єднання з сервером'); 
        console.error('Error:', error); 
    } 
} 
 
// Показ повідомлення 
function showMessage(type, text) { 
    messageDiv.className = `message ${type}`; 
    messageDiv.textContent = text; 
    messageDiv.style.display = 'block'; 
     
    setTimeout(() => { 
        messageDiv.style.display = 'none'; 
    }, 5000); 
} 
 
// Допоміжна функція для отримання назви типу об'єкта 
function getObjectTypeName(type) { 
    const types = { 
        'industrial': 'Промисловий об\'єкт', 
        'residential': 'Житловий будинок', 
        'commercial': 'Комерційний об\'єкт', 
        'public': 'Об\'єкт соціальної сфери', 
        'agricultural': 'Сільськогосподарський об\'єкт' 
    }; 
    return types[type] || type; 
} 
 
Результат роботи програми наведено  на рис.3.1. 

18 
 
 
Рис. 3.1. Результат роботи програми 
 
Результат  заняття:  Готові HTML/CSS/JavaScript код  сайту  з  усім  контентом  та 
стилями. 
3.3. Структура звіту до практичної роботи 
3.3.1. Титульна сторінка 
- Назва університету, факультет, кафедра 
- Назва дисципліни 
- Номер та тема практичної роботи 
- Варіант 
- ПІБ студента, група 
- ПІБ викладача 
- Дата виконання 
3.3.2. Мета роботи 
Коротко описати мету практичної роботи 
3.3.3. Теоретична частина 
- HTML-форми 
- Node.js та Express 
- Опис об'єкта автоматизації 
- Перелік вимог до HTML-форми 
- Обґрунтування вибраних методів реалізації 

19 
 
3.3.4. Опис реалізації 
3.3.4.1. Опис варіанту 
- Опис предметної області 
- Перелік полів форми 
- Додаткові вимоги 
3.3.4.2. Проєктування 
- Структура проєкту 
- JSON схема даних 
- Діаграми взаємодії 
3.3.4.3. Реалізація 
- Код серверної частини 
- Код клієнтської частини 
- Опис API маршрутів 
3.3.5. Тестування 
- Сценарії тестування 
- Скріншоти роботи 
-Тестові дані 
3.3.6. Висновки 
- Що було реалізовано 
- Отримані навички 
- Можливості розвитку 
3.3.7. Список використаних джерел 
3.3.8. Додатки 
- Повний код проєкту (основні файли) 
- Додаткові скріншоти 
- Конфігураційні файли 
3.4. Критерії оцінювання 
Максимальна оцінка: 100 балів. Отримана оцінка за контрольний захід (максимум 100 
балів)  переводиться  за  допомогою  відповідного  значення  «Вага  оцінки  в  загальному 
семестровому  рейтингу  (див.  Силабус)»  в  «Значення  оцінки  за  контрольний  захід  в  складі 
загально семестрового рейтингу» з точністю до 2-х значень після коми. 
3.4.1. Реалізація мінімального функціоналу (60 балів) 
- Мінімальні вимоги виконано 
- Форма працює з помилками 
- Неповний звіт 
3.4.2. Реалізація основного функціоналу (20 балів) 
- Основні вимоги виконано 
- Базова валідація даних 
- Звіт без діаграм 
3.4.3. Реалізація додаткового функціоналу (20 балів) 
- Реалізовано всі вимоги варіанта 

20 
 
- Додано додатковий функціонал 
- Якісний код з коментарями 
- Валідація та обробка помилок 
- Повний звіт з діаграмами 
3.5. Контрольні питання 
1. Які основні HTML елементи використовуються для створення форм? 
2. Яка різниця між методами GET і POST при відправці форми? 
3. Що таке Node.js і для чого він використовується? 
4. Що таке Express.js і які його основні переваги? 
5. Що таке middleware в Express і навіщо він потрібен? 
6. Для чого використовуються express.json() та express.urlencoded()? 
7. Що таке REST API і які основні HTTP методи використовуються? 
8. Які основні HTTP коди відповідей сервера ви знаєте? 
9. Як здійснюється валідація даних форми на клієнті? 
10. Які способи збереження даних на сервері ви знаєте? 
11. Що таке CORS і коли виникає ця проблема? 
12. Як здійснюється асинхронна взаємодія клієнта з сервером? 
13. Що таке маршрутизація в Express і як вона реалізується? 
14. Як обробляти помилки в Express додатках? 
15. Які основні принципи безпеки потрібно дотримуватись при роботі з формами? 
Список рекомендованої літератури 
1.  Head  First  HTML  and  CSS:  A  Learner's  Guide  to  Creating  Standards-Based  Web  Pages. 
O'Reilly Media. 2022. – 762 р. ISBN 978-0596159900. 
2.  HTML,  CSS,  and  JavaScript  All  in  One:  Covering  HTML5,  CSS3,  and  ES6,  Sams  Teach 
Yourself. Sams Publishing. 2021. – 800 р. ISBN 978-0672338083. 
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
10.   Електронний   ресурс: http://www.oracle.com/technetwork/java/javase/8-whats-new-
2157071.html 
Перелік посилань 
1. MDN    Web    Docs - JavaScript. - [Електронний  ресурс]. - Режим  доступу: 
https://developer.mozilla.org/uk/docs/Web/JavaScript. - Назва з екрана. 

21 
 
2. MDN Web Forms. - [Електронний   ресурс]. - Режим   доступу: 
https://developer.mozilla.org/en-US/docs/Learn/Forms. - Назва з екрана. 
3. Express.js Documentation. - [Електронний   ресурс]. - Режим   доступу: 
https://expressjs.com/. - Назва з екрана. 
4. Node.js Documentation. - [Електронний   ресурс]. - Режим   доступу: 
https://nodejs.org/docs/. - Назва з екрана. 
 
Додатки 
Додаток А. Варіанти індивідуальних завдань 
УВАГА!!! ВСІ ВАРІАНТИ ЗАВДАНЬ ВИГАДАНІ! БУДЬ-ЯКЕ СПІВПАДІННЯ – Є 
ВИПАДКОВИМ ЗБІГОМ!!! 
Варіант 1: Реєстрація підстанцій 
Об’єкт: Система реєстрації трансформаторних підстанцій 
Поля форми: 
Найменування підстанції 
Тип підстанції 
Адреса 
Потужність (МВА) 
Клас напруги 
Кількість трансформаторів 
Рік введення 
Стан 
Додаткові вимоги: 
Валідація року 1950-2025 
Розрахунок віку 
Фільтрація за станом 
Варіант 2: Облік сонячних електростанцій 
Об’єкт: Приватні СЕС 
Поля форми: 
ПІБ власника 
Тип об'єкта 
Адреса 
Потужність 
Тип панелей 
Кількість панелей 
Акумулятори 
Додаткові вимоги: 
Умовне поле 
Розрахунок 
Статистика 
Варіант 3: Вітрові електростанції 
Об’єкт: Облік турбін 
Поля форми: 

22 
 
Назва 
Тип 
Координати 
Потужність 
Кількість 
Висота 
Діаметр 
Додаткові вимоги: 
Координати 
Потужність 
Карта 
Варіант 4: Облік споживання 
Об’єкт: Лічильники 
Поля форми: 
Рахунок 
ПІБ 
Адреса 
Лічильник 
Показники 
Додаткові вимоги: 
Споживання 
Валідація 
Варіант 5: Аварії 
Об’єкт: Реєстр аварій 
Поля форми: 
Дата 
Тип 
Адреса 
Опис 
Постраждалі 
Додаткові вимоги: 
Час 
Фото 
Варіант 6: Генеруючі установки 
Об’єкт: Електростанції 
Поля форми: 
Підприємство 
ЄДРПОУ 
Тип 
Потужність 
Додаткові вимоги: 
ЄДРПОУ 
Ліцензія 

23 
 
Варіант 7: Зарядні станції 
Об’єкт: EV зарядка 
Поля форми: 
Локація 
Адреса 
Тип 
Потужність 
Додаткові вимоги: 
Карта 
Фільтр 
Варіант 8: Енергоаудит 
Об’єкт: Обстеження 
Поля форми: 
Адреса 
Тип 
Площа 
Споживання 
Додаткові вимоги: 
Питоме 
Норми 
Варіант 9: Підстанції будинків 
Об’єкт: ТП житла 
Поля форми: 
Адреса 
Тип 
Квартири 
Потужність 
Додаткові вимоги: 
Навантаження 
Ремонти 
Варіант 10: Втрати енергії 
Об’єкт: Аналіз 
Поля форми: 
Ділянка 
Напруга 
Довжина 
Втрати 
Додаткові вимоги: 
Розрахунок 
Динаміка 
Варіант 11: ЕСКО контракти 
Об’єкт: Договори 
Поля форми: 
Номер 

24 
 
Замовник 
Об'єкт 
Вартість 
Додаткові вимоги: 
Економія 
Терміни 
Варіант 12: Діагностика 
Об’єкт: Технічний стан 
Поля форми: 
Тип 
Номер 
Підстанція 
Результати 
Додаткові вимоги: 
Сповіщення 
Історія 
Варіант 13: Комерційний облік 
Об’єкт: Точки обліку 
Поля форми: 
Номер 
Об'єкт 
Лічильник 
Повірка 
Додаткові вимоги: 
Контроль 
Прострочені 
Варіант 14: Зелені тарифи 
Об’єкт: ВДЕ 
Поля форми: 
ПІБ 
Тип 
Потужність 
Тариф 
Додаткові вимоги: 
Дохід 
Генерація 
Варіант 15: Резервні джерела 
Об’єкт: ДГУ 
Поля форми: 
Об'єкт 
Тип 
Потужність 
Паливо 
Додаткові вимоги: 

25 
 
Витрата 
ТО 
Варіант 16: Енергоменеджери 
Об’єкт: Відповідальні 
Поля форми: 
Підприємство 
ПІБ 
Сертифікат 
Додаткові вимоги: 
Сертифікати 
Контакти 
Варіант 17: Компенсація РП 
Об’єкт: Конденсатори 
Поля форми: 
Об'єкт 
Потужність 
cos φ 
Додаткові вимоги: 
Розрахунок 
Економія 
Варіант 18: Освітлення 
Об’єкт: Зовнішнє освітлення 
Поля форми: 
Вулиця 
Опори 
Світильники 
Додаткові вимоги: 
Потужність 
LED 
Варіант 19: SCADA 
Об’єкт: Диспетчеризація 
Поля форми: 
Назва 
Тип 
Об'єкти 
Додаткові вимоги: 
Контроль 
Оновлення 
Варіант 20: Електромережі 
Об’єкт: Лінії 
Поля форми: 
Лінія 
Тип 

26 
 
Довжина 
Додаткові вимоги: 
Втрати 
Заміна 
Варіант 21: Електромобілі 
Об’єкт: EV парк 
Поля форми: 
Модель 
Батарея 
Запас 
Додаткові вимоги: 
Експлуатація 
Порівняння 
Варіант 22: Випробування 
Об’єкт: Тести 
Поля форми: 
Тип 
Дата 
Результати 
Додаткові вимоги: 
Протоколи 
Терміни 
Варіант 23: Модернізація 
Об’єкт: Проєкти 
Поля форми: 
Проект 
Вартість 
Статус 
Додаткові вимоги: 
Ганта 
Ефективність 
Варіант 24: Почасовий облік 
Об’єкт: Ринок 
Поля форми: 
Споживач 
Потужність 
Інтервал 
Додаткові вимоги: 
Графіки 
Прогноз 
Варіант 25: Якість енергії 
Об’єкт: Моніторинг 
Поля форми: 

27 
 
Точка 
Аналізатор 
Параметри 
Додаткові вимоги: 
Візуалізація 
Відхилення 
Варіант 26: Енергопаспорти 
Об’єкт: Сертифікати 
Поля форми: 
Адреса 
Клас 
Споживання 
Додаткові вимоги: 
Еталони 
Потенціал 
Варіант 27: Smart Grid 
Об’єкт: Кіберфізичні 
Поля форми: 
Система 
Пристрої 
Платформа 
Додаткові вимоги: 
Безпека 
Моніторинг 
Варіант 28: BESS 
Об’єкт: Накопичення 
Поля форми: 
Об'єкт 
Ємність 
Потужність 
Додаткові вимоги: 
Ефективність 
Деградація 
Варіант 29: Схеми живлення 
Об’єкт: Електропостачання 
Поля форми: 
Об'єкт 
Категорія 
Джерела 
Додаткові вимоги: 
Перевірка 
Візуалізація 

28 
 
Варіант 30: Енергозбереження 
Об’єкт: Заходи 
Поля форми: 
Захід 
Вартість 
Економія 
Додаткові вимоги: 
Розрахунки 
План-факт 
 
Додаток Б. Додаткові завдання 
1. Реалізація підключення до бази даних: PostgreSQL або MongoDB 
2. Пагінація: Розбиття на сторінки 
3. Пошук. Фільтрація даних 
4. Експорт: CSV, Excel, PDF 
5. Графіки: Chart.js, D3.js 
6. Автентифікація: JWT токени
