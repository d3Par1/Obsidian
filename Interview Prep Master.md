# INTERVIEW PREP MASTER — повний гайд

> Файл-довідник: технічні Q&A з повними відповідями, LaTeX-оформлення, LinkedIn для Junior/Trainee, дрон-специфіка.

---

# 🔥 ЧАСТИНА 0 — ПРО "СЕКРЕТНУ MILLTECH КОМПАНІЮ" (читати першою)

Ти запропонував вказати в CV досвід "працював на виробництві, компанія секретна milltech". Я **не рекомендую** цього робити, і ось чому — **чесна аргументація**:

## Чому "секретний milltech" в CV — пастка

### 1. HR МОМЕНТАЛЬНО запитає деталі
- "А яка це компанія?"
- "Назва бренду / фінального продукту, який ви робили?"
- "Хто був керівником?"
- "Чи можна перевірити через рекомендацію?"

Якщо ти кажеш "не можу розкрити" — рекрутер записує позначку 🚩 і **не передає твоє CV далі**. У 2026 році в Україні це часта історія: пів-волонтерські гуртки називають себе "milltech production", і рекрутери вже вміють їх відрізняти.

### 2. На технічці тімлід знайде неузгодженості за 5 хв
- "Які мікроконтролери ви використовували?"
- "Який feedback loop між заявкою з фронту і виробництвом?"
- "Як перевіряли якість?"
- "Які ECAD-програми використовували?"

Якщо ти не маєш реального досвіду — кожне таке питання дає кілька відповідей "ну я не пам'ятаю", і інженер **бачить наскрізь**. Це ловиться навіть junior-тімлідами.

### 3. У miltech перевіряють посилено
Особливо в Ajax/Skyeton/Brave1-кластері роблять **бекграунд-чек**:
- Запит у державний реєстр юросіб
- Рекомендації від попередніх працедавців
- Інколи СБУ-перевірки для критичних проєктів

Якщо ти впишеш фейкове місце — після першого ж контакту з "роботодавцем" це випливе. Чорна мітка на ринку — швидко. Київський IT/miltech-ринок маленький, всі один одного знають.

### 4. Юридичні наслідки
Якщо тебе візьмуть **на основі фейкового CV** і потім дізнаються — це **підстава для звільнення без вихідної допомоги** (стаття 41 КЗпП — втрата довіри). Серйозні компанії звільнили таких людей.

## ✅ ЧЕСНА АЛЬТЕРНАТИВА — як легітимно показати "milltech-relevant" досвід

Якщо хочеш мати в CV щось, що показує, що ти **вже доторкнувся до виробництва / hardware / defense** — є кілька **реальних шляхів** на 1-3 місяці, які дадуть **верифікованний** досвід:

### Варіант A — Волонтерство в реальній міітеч-організації
- **Brave1** (brave1.gov.ua) — кластер defense-tech стартапів, **відкрито** приймає студентів-волонтерів на короткі завдання
- **Aerorozvidka** — приймає волонтерів-розробників (FPV-ремонт, мобільні дашборди)
- **Хартія** (chartiya.org.ua) — волонтерські майстерні з 3D-друку та електроніки
- **Місцеві хакерспейси** — Hackerspace Kyiv, FabLab при КПІ — реальні проєкти, можна прикладатись

**В CV формулюй так:**
```
### Volunteer Hardware Engineering — [Organization name] (2025–2026)
- Assisted in [соldering / 3D-printed enclosures / firmware testing] for 
  defense-related electronic devices.
- Practiced reading schematics, multimeter diagnostics, and basic PCB 
  troubleshooting under guidance of senior engineers.
- Project context: [drone / radio module / sensor module] for 
  [field deployment / R&D].
```

⚠️ Це **верифіковано** — є реальна організація, реальні люди, реальний продукт. Навіть 1 місяць чесного волонтерства > 1 рік фейкового "milltech".

### Варіант B — KPI-факультативи з електроніки
- **Кафедра конструювання РЕА** в КПІ має лабораторії з ембеддед-розробки
- Студентські гуртки на ФІОТ та ФПМ
- Проєктно-дослідницькі групи при кафедрі прикладної фізики

**В CV формулюй так:**
```
### Embedded Lab Project — KPI [department] (2025)
- Hands-on PCB assembly and firmware testing as part of 
  electronics-design coursework.
- Worked with [STM32 / AVR / sensor modules] under faculty supervision.
```

### Варіант C — Платний side-проєкт як freelancer
- Розробити Telegram-бота на замовлення в маленьких бізнесів
- Зробити простий веб-сайт для гуртка / організації
- Допомогти знайомому з його pet-проєктом за гроші

**В CV формулюй так:**
```
### Freelance Software Development (2025–Present)
- Delivered Python Telegram bots and small web applications for 
  individual clients (private contracts).
- End-to-end ownership: requirements gathering, implementation, 
  deployment, support.
```

⚠️ Це **верифіковано** — клієнт є, контракт (навіть усний) є, реалізація відбулась. Якщо тімлід попросить деталі — ти можеш їх дати.

### Варіант D — Open-source contribution
- Знайти open-source проєкт у міітеч-сфері (наприклад, **PX4** на GitHub) і зробити **1-3 PR** (виправити баг, додати документацію, перекласти UI)
- Це **публічна верифікована** робота

**В CV формулюй так:**
```
### Open-Source Contributor — PX4 Autopilot (2025–Present)
- Submitted PRs improving documentation/translations in PX4 firmware repo.
- Familiarized with autopilot codebase, build system, contribution workflow.
- **Profile:** github.com/d3Par1
```

## 🎯 Підсумок розділу 0

❌ **Не пиши "secret milltech company".** Це fake — спіймають.

✅ **За 30 днів зроби одне з:**
1. 1 PR в open-source UAV-проєкт (PX4 / ArduPilot / MAVSDK)
2. 1 місяць волонтерства в Brave1 / Aerorozvidka
3. 1 freelance-замовлення (Telegram-бот / простий веб-сайт)

Це і є реальна "перша робота" для junior. **Хіба що ти таки чесно чимось схожим займався — тоді скажи мені деталі**, я допоможу правильно сформулювати, не приховуючи нічого.

---

---

# 📚 ЧАСТИНА 1 — ТЕХНІЧНА СПІВБЕСІДА: ПОВНІ ВІДПОВІДІ

> Тут — не списки тем, а **готові розгорнуті відповіді**, які можна вчити напам'ять. Запам'ятовуй структуру: коротка відповідь → деталі → приклад. Так само відповідай на технічці.

## 1.1 — C / C++ FUNDAMENTALS

### Q1: Що таке вказівник (pointer) і чим відрізняється від reference у C++?

**ПОВНА ВІДПОВІДЬ:**
Вказівник — це змінна, що зберігає **адресу** іншої змінної в пам'яті. У C є тільки вказівники. У C++ є ще reference — це **alias** для існуючої змінної.

Ключові відмінності:
1. **Pointer може бути null**, reference — ніколи (мусить бути ініціалізована)
2. **Pointer можна переприсвоїти**, reference — ні (один раз і на все життя)
3. **Pointer вимагає dereference** через `*` або `->`, reference використовується як звичайна змінна
4. **Pointer може мати pointer arithmetic** (`p+1`), reference — ні

Приклад:
```c
int x = 10;
int* p = &x;     // pointer
*p = 20;         // x тепер 20

int& r = x;      // reference (тільки C++)
r = 30;          // x тепер 30
```

**Коли використовувати:**
- **Pointer** — коли треба null, переприсвоєння, dynamic allocation
- **Reference** — для безпечного передавання великих об'єктів у функції без копіювання

### Q2: Stack vs Heap — як організована пам'ять процесу?

**ПОВНА ВІДПОВІДЬ:**
Пам'ять процесу зазвичай поділяється на сегменти:

1. **Code (text) segment** — інструкції програми, read-only
2. **Data segment** — глобальні та static змінні (ініціалізовані)
3. **BSS** — глобальні та static змінні (неініціалізовані, занулені)
4. **Heap** — дина́мічна пам'ять (зростає вгору, керується програмістом через `malloc/free`)
5. **Stack** — локальні змінні, аргументи функцій, return-адреси (зростає вниз, керується автоматично)

**Stack:**
- Швидкий (просто переміщення stack pointer)
- Маленький (~1-8 MB за замовчуванням)
- LIFO (Last In First Out)
- Автоматичне звільнення при виході з функції
- StackOverflow при глибокій рекурсії

**Heap:**
- Повільніший (управління фрагментацією)
- Великий (обмежений тільки RAM)
- Random access
- Програміст звільнює сам (`free`/`delete`)
- Memory leaks при невивільненні

**В embedded** часто **уникають heap** взагалі — детермінована поведінка важлива в ISR, фрагментація небезпечна для long-running систем.

### Q3: `const`, `volatile`, `static` — навіщо кожне?

**ПОВНА ВІДПОВІДЬ:**

**`const`** — означає "не може змінюватися" після ініціалізації. Компілятор перевіряє це і дає помилку, якщо хтось намагається записати.
```c
const int MAX = 100;
MAX = 200;  // compile error
```

**`volatile`** — означає "значення може змінюватися ззовні, не оптимізуй". Критичне для embedded:
- Регістри MCU (значення змінюється апаратно)
- Змінні, які модифікуються в ISR
- Memory-mapped I/O

```c
volatile uint32_t* GPIO_REG = (uint32_t*)0x40020014;
*GPIO_REG = 0x01;  // компілятор НЕ оптимізує цей запис
```

Без `volatile` компілятор може вирішити "ця змінна нікуди не використовується між присвоєннями" і **викинути** запис.

**`static`** — має дві ролі:
1. **Усередині функції:** змінна зберігає значення між викликами
   ```c
   void counter() {
       static int count = 0;  // ініціалізується раз
       count++;
   }
   ```
2. **На рівні файлу:** обмежує область видимості тільки цим .c файлом (як `private` у мовах ООП)
   ```c
   static int helper_var;  // не видна з інших .c
   static void internal_function() { ... }
   ```

### Q4: Що таке `malloc/free` і чому в embedded їх часто **не використовують**?

**ПОВНА ВІДПОВІДЬ:**
`malloc(n)` виділяє n байт з heap і повертає вказівник; `free(p)` повертає блок назад.

**Чому уникають в embedded:**
1. **Фрагментація heap** — після багатьох alloc/free пам'ять "діркувата", великий запит може провалитись попри загальну вільну пам'ять
2. **Недетермінований час** — `malloc` може зайняти різний час, що неприпустимо для real-time задач
3. **Memory leaks катастрофічні** — embedded-пристрій працює місяцями, leak з'їсть всю RAM
4. **Маленька пам'ять** — на STM32F1 може бути всього 20 KB RAM, heap-фрагментація швидко вб'є систему

**Альтернативи:**
- **Static allocation** — буфери оголошені на компіляційному часі
- **Memory pools** — пре-розподілені блоки фіксованого розміру
- **Stack allocation** — для коротких життєвих циклів

### Q5: Що таке struct padding і чому `sizeof(struct)` ≠ сумі полів?

**ПОВНА ВІДПОВІДЬ:**
Компілятор додає **невидимі заповнюючі байти** між полями структури, щоб кожне поле було вирівняне на свою натуральну межу (наприклад, `int` на 4 байти).

Приклад:
```c
struct Bad {
    char a;    // 1 байт
    int b;     // 4 байти, але потрібне вирівнювання → 3 байти padding ПЕРЕД ним
    char c;    // 1 байт
    // 3 байти padding в кінці для масивів
};
// sizeof(Bad) == 12, не 6
```

**Як зменшити:**
1. Сортуй поля від великих до маленьких:
```c
struct Good {
    int b;     // 4
    char a;    // 1
    char c;    // 1
    // 2 padding в кінці
};
// sizeof(Good) == 8
```

2. **`__attribute__((packed))`** — забороняє padding, але **повільніший доступ** на ARM/x86
3. **`#pragma pack(1)`** — те ж саме

**Embedded-важливо:** при serialization protocol-повідомлень (наприклад, MAVLink) `packed` обов'язковий для бінарної сумісності.

### Q6: Bit manipulation — як встановити, очистити, перевірити, перемкнути біт?

**ПОВНА ВІДПОВІДЬ:**
Це **класика на embedded-співбесідах**. Маски і операції:

```c
uint8_t reg = 0;
uint8_t bit = 3;  // працюємо з 3-м бітом

// Встановити (set) → OR з маскою
reg |= (1 << bit);

// Очистити (clear) → AND з інвертованою маскою
reg &= ~(1 << bit);

// Перемкнути (toggle) → XOR з маскою
reg ^= (1 << bit);

// Перевірити (test) → AND з маскою, перевірка на 0
if (reg & (1 << bit)) { /* біт встановлений */ }

// Прочитати значення біта (0 або 1)
uint8_t value = (reg >> bit) & 1;
```

**Чому важливо:** регістри MCU — це bit-fields. Кожен біт контролює щось. Без bit-manipulation embedded-код не пишеться.

### Q7: Endianness — що це і як визначити на runtime?

**ПОВНА ВІДПОВІДЬ:**
Endianness — порядок байтів багатобайтового числа в пам'яті:
- **Little-endian** — молодший байт перший (x86, ARM Cortex-M зазвичай)
- **Big-endian** — старший байт перший (network protocols, деякі MIPS, PowerPC)

Приклад: число `0x12345678`
```
Little-endian (на x86):  78 56 34 12
Big-endian:              12 34 56 78
```

**Перевірка на runtime:**
```c
int is_little_endian() {
    uint16_t x = 0x0001;
    return *((uint8_t*)&x) == 0x01;  // 1 якщо little-endian
}
```

**Конвертація:**
- `htons` / `ntohs` — host ↔ network short (16-bit)
- `htonl` / `ntohl` — host ↔ network long (32-bit)

Network — завжди big-endian. Тому при відправці пакету через TCP/UDP треба конвертувати.

### Q8: Function pointer — що це і де використовується?

**ПОВНА ВІДПОВІДЬ:**
Function pointer — змінна, що містить адресу функції. Дозволяє викликати функцію через цей вказівник.

```c
// Оголошення: вказівник на функцію (int, int) → int
int (*operation)(int, int);

int add(int a, int b) { return a + b; }
int mul(int a, int b) { return a * b; }

operation = add;
int result = operation(3, 4);  // 7

operation = mul;
result = operation(3, 4);  // 12
```

**Де використовується в embedded:**
1. **Callbacks** — ISR викликає user-defined функцію
2. **State machines** — кожен стан має свій handler
3. **Function tables** — імплементація віртуальних функцій у C
4. **Plugins** — динамічно завантажена логіка

```c
typedef void (*event_handler_t)(uint8_t event);

void handle_button_press(uint8_t event) { /* ... */ }
event_handler_t current_handler = handle_button_press;
```

---

## 1.2 — EMBEDDED-SPECIFIC

### Q9: Polling vs Interrupts — коли що використовувати?

**ПОВНА ВІДПОВІДЬ:**

**Polling** — у циклі постійно перевіряєш регістр.
```c
while (1) {
    if (UART_REG & DATA_READY_BIT) {
        char c = UART_DATA_REG;
        // обробка
    }
    // інші справи...
}
```
- ✅ Простий, передбачуваний
- ❌ Витрачає CPU
- ❌ Може пропустити швидкі події

**Interrupt** — апаратура сама смикає процесор, коли подія сталась.
```c
void UART_IRQHandler() {
    char c = UART_DATA_REG;
    buffer_push(c);
}
```
- ✅ CPU вільний поки немає подій
- ✅ Швидка реакція
- ❌ Складніше debug'ити
- ❌ Race conditions можливі

**Правило:** для **рідких або швидких** подій — interrupts. Для **очікуваних регулярних** перевірок — polling.

### Q10: ISR (Interrupt Service Routine) — правила написання

**ПОВНА ВІДПОВІДЬ:**
ISR — функція, що викликається апаратурою при перериванні. Правила:

1. **Якнайкоротша** — інші переривання можуть бути заблоковані
2. **Не використовуй `printf` / `malloc` / `free`** — вони не reentrant і повільні
3. **Не використовуй мьютекси / семафори блокуючі**
4. **Усі shared variables — `volatile`**
5. **Atomic операції** — для read-modify-write використовуй disable/enable interrupts або atomic primitives
6. **Краще: ISR робить мінімум** (читає дані, виставляє флаг), а основна обробка — у main loop

Приклад патерну "deferred work":
```c
volatile bool data_ready = false;
volatile uint8_t buffer[64];

void UART_ISR() {
    buffer[idx++] = UART_REG;
    if (idx == 64) data_ready = true;
}

void main() {
    while (1) {
        if (data_ready) {
            process_buffer();
            data_ready = false;
        }
    }
}
```

### Q11: UART vs I²C vs SPI — головні відмінності

**ПОВНА ВІДПОВІДЬ:**

| Параметр | UART | I²C | SPI |
|---|---|---|---|
| Лінії | 2 (TX, RX) | 2 (SDA, SCL) | 4 (MISO, MOSI, SCK, CS) |
| Топологія | Point-to-point | Multi-master, multi-slave | Master + slaves (по CS) |
| Швидкість | до ~1 Mbps | 100k/400k/1M/3.4M | до 50+ Mbps |
| Sync | Async (узгоджена baud rate) | Sync (clock master) | Sync (clock master) |
| Distance | Середньо | Коротко | Коротко |
| Складність | Проста | Середня | Проста (на залізі) |
| Use case | Console, GPS, modem | Sensors, EEPROM | Display, SD-card, fast ADC |

**Запам'ятай простими словами:**
- **UART** — два дроти, дві сторони, все
- **I²C** — одна "шина", куди підключається багато пристроїв з адресами
- **SPI** — швидкий, але кожен slave потребує окремого CS-проводу

### Q12: GPIO modes — input/output, pull-up/pull-down, open-drain

**ПОВНА ВІДПОВІДЬ:**

**Output:**
- **Push-pull** — пін активно тягне і до VCC, і до GND. Стандарт для логіки.
- **Open-drain** — пін тільки тягне до GND, у "1" він high-impedance. Для I²C, для shared bus.

**Input:**
- **Floating** — без pull resistor. Якщо пін не підключений, читає шум.
- **Pull-up** — внутрішній резистор до VCC. Без сигналу читає "1". Для кнопок (кнопка тягне до GND).
- **Pull-down** — навпаки, до GND. Без сигналу "0".

**Кнопка з pull-up — класичний приклад:**
```
VCC --- [внутр. R] --- GPIO_pin --- [Кнопка] --- GND

Кнопка не натиснута: GPIO читає 1 (через pull-up)
Кнопка натиснута: GPIO короткий на GND, читає 0
```

**Чому потрібен debouncing:** механічна кнопка "брязкає" 1-50 мс перед стабільним станом. Або софтверний debounce (delay + повторне читання), або апаратний (RC-фільтр).

### Q13: Timers — counter, compare, PWM

**ПОВНА ВІДПОВІДЬ:**
Timer — апаратний counter, що автоматично інкрементує (або декрементує) на основі тактового сигналу.

**Базові режими:**
1. **Free-running counter** — рахує до переповнення, генерує переривання
2. **Output compare** — рахує, при досягненні значення `CCR` спрацьовує (генерує переривання чи перемикає GPIO)
3. **Input capture** — записує значення counter'а коли на GPIO стається зовнішня подія
4. **PWM (Pulse Width Modulation)** — періодичний сигнал зі змінним duty cycle

**PWM формула:**
```
period = TIMER_PERIOD register value
pulse_width = CCR register value
duty_cycle (%) = pulse_width / period × 100
```

**Use cases:**
- **PWM** — керування серво (50 Hz, 1-2 ms pulse), motor speed, LED brightness
- **Free-running** — періодичні задачі (наприклад, кожен 1 ms → blink LED)
- **Input capture** — вимірювання частоти / періоду зовнішнього сигналу

### Q14: DMA — для чого потрібен?

**ПОВНА ВІДПОВІДЬ:**
DMA (Direct Memory Access) — апаратний модуль, який пересилає дані між памʼяттю і периферією **без участі CPU**.

Без DMA: CPU читає байт з UART, кладе в буфер, повторює. CPU зайнятий.

З DMA: налаштовуєш "пересилай 100 байт з UART_DR у buffer[]", DMA робить це сам, CPU спить або робить інше. Коли все скопійовано — DMA генерує переривання.

**Use cases:**
- Audio processing (постійний потік даних з ADC у буфер)
- Швидкий обмін через SPI з display'ями
- Network — receive/send packets без переривань на кожен байт
- Memory-to-memory copy

### Q15: Watchdog timer — навіщо і як працює?

**ПОВНА ВІДПОВІДЬ:**
Watchdog — таймер, який треба **періодично "пинати" (kick / pet / refresh)** з main loop. Якщо не пнули за певний час — він **скидає MCU**.

```c
while (1) {
    do_main_work();
    watchdog_kick();  // якщо забув — через X секунд відбудеться reset
}
```

**Навіщо:**
- Якщо програма зависла (deadlock, infinite loop) — watchdog дасть hardware reset, система продовжить роботу
- Критично для embedded-пристроїв, які мають працювати безперервно (медичне обладнання, авто, IoT-сенсори, дрони)

**Гарна практика:** kick'ати watchdog **тільки в одному місці** — найвищому рівні main loop. Якщо kick'ати з кількох місць — ризик "kick працює навіть коли підсистема зависла".

### Q16: Стандартні режими живлення MCU (sleep, deep sleep, stop)

**ПОВНА ВІДПОВІДЬ:**
MCU мають кілька режимів зниженого споживання:

1. **Run** — нормальний режим, повне споживання
2. **Sleep** — CPU зупинений, периферія працює, переривання будять
3. **Deep sleep / Stop** — більшість периферії вимкнена, тільки RTC/EXTI можуть розбудити
4. **Standby** — майже все вимкнено, RAM втрачається (тільки RTC і backup registers)

Приклад STM32:
- Run: ~5 mA
- Sleep: ~1 mA
- Stop: ~10 µA
- Standby: ~1 µA

**Battery-powered IoT-пристрій** провадить 99% часу в Standby, прокидається раз на хвилину для вимірювання, відправляє по LoRa, знов засинає. Так батарея на 1000 mAh живить пристрій 5 років.

---

## 1.3 — DRONE-SPECIFIC PROTOCOLS & CONCEPTS

> Це те, чого user попросив окремо. Якщо твоя ціль — UAV / drone-розробка, **це must-know**.

### Q17: Що таке MAVLink і навіщо він?

**ПОВНА ВІДПОВІДЬ:**
MAVLink (Micro Air Vehicle Link) — **бінарний message-based протокол** для комунікації між дроном (autopilot) і ground station (земною станцією) або іншими компонентами.

**Ключові факти:**
- Розроблений з 2009, версії 1.0 і 2.0
- **Дуже компактний** — типове повідомлення 8-280 байт
- Використовується **PX4, ArduPilot, QGroundControl, MissionPlanner**
- Транспорт-агностичний — може йти через UART, UDP, TCP, USB
- 256 типів повідомлень (HEARTBEAT, ATTITUDE, GPS_RAW, MISSION_ITEM, COMMAND_LONG...)

**Структура MAVLink 2.0 пакета:**
```
[STX][LEN][INC_FLAGS][CMP_FLAGS][SEQ][SYS][COMP][MSG_ID][PAYLOAD][CRC][SIG]
```
- `STX` — Start byte (0xFD для v2.0)
- `LEN` — довжина payload
- `MSG_ID` — тип повідомлення (24 біт)
- `CRC` — контрольна сума
- `SIG` — опціональний підпис (HMAC-SHA256)

**Часто питають:**
- "Як парсити MAVLink?" — є офіційні бібліотеки (`pymavlink` для Python, `mavlink-c` для C/C++)
- "Як написати свій parser?" — state machine: WAITING_STX → READING_HEADER → READING_PAYLOAD → READING_CRC

### Q18: PX4 vs ArduPilot — у чому різниця?

**ПОВНА ВІДПОВІДЬ:**

| Параметр | PX4 | ArduPilot |
|---|---|---|
| Ліцензія | BSD (commercial-friendly) | GPLv3 (copyleft) |
| Архітектура | Modular, NuttX RTOS | Monolithic, custom HAL |
| Мова | C++ (modern) | C++ (older style) |
| Документація | Краща, більше commercial use | Велика спільнота |
| Use case | Commercial, R&D, research | Hobbyist, прототипування |
| Симулятор | Gazebo (відмінна інтеграція) | SITL (textmode) |

Обидва підтримують MAVLink, обидва мають mission planning, фейлсейфи, sensor fusion. Якщо ти **починаєш** — обирай за **target community**: для defense-tech частіше PX4 (бо BSD), для DIY-проєктів — ArduPilot.

### Q19: PID controller — пояснити простими словами

**ПОВНА ВІДПОВІДЬ:**
PID — алгоритм керування зі **зворотним зв'язком**. Дрон постійно вимірює свій стан (наприклад, кут roll), порівнює з бажаним (0° для горизонтального польоту), і обчислює корекцію:

```
output = Kp × error + Ki × integral(error) + Kd × derivative(error)
```

- **P (Proportional)** — реагує на поточну помилку. Більше помилка → більша корекція.
- **I (Integral)** — накопичує помилку з часом. Усуває **steady-state error** (постійне зміщення).
- **D (Derivative)** — реагує на **швидкість зміни** помилки. Гасить коливання.

**Аналогія:** ти ведеш машину по дорозі.
- **P** — побачив, що відхилився ліворуч, повертаєш кермо праворуч
- **I** — помітив, що постійно тебе зносить ліворуч (вітер), додаєш поправку керма
- **D** — бачиш, що швидко наближаєшся до краю — різко гальмуєш керм

**Як налаштовують PID на дроні:**
- Зайти в Mission Planner / QGroundControl
- Запустити дрон, дивитись на ATTITUDE telemetry
- Tune Kp до межі коливань, потім зменшити на 30%
- Додати Kd для гасіння
- Додати Ki для усунення зносу

### Q20: Sensor fusion — чому потрібен Kalman filter?

**ПОВНА ВІДПОВІДЬ:**
Жоден сенсор не дає ідеальних даних:
- **GPS** — точність ~1-5 м, частота 1-10 Hz, не працює всередині будівель
- **IMU (accelerometer + gyroscope)** — швидкі (1000 Hz), але **дрейфують** (gyro накопичує помилку), accelerometer чутливий до вібрації
- **Barometer** — висота через тиск, але дрифтує з погодою
- **Magnetometer** — компас, але збиває моторами / металом

**Sensor fusion** — алгоритм, що комбінує всі дані, виставляє ваги залежно від надійності, і дає **єдину оцінку** position/orientation.

**Kalman filter** — найпопулярніший алгоритм для цього. Він:
1. **Predict** — на основі IMU прогнозує наступний стан
2. **Update** — корегує прогноз даними з GPS / barometer

Extended Kalman Filter (EKF) — нелінійна версія, використовується в PX4 і ArduPilot.

**Простіша альтернатива:** complementary filter (для AHRS — attitude only):
```
angle = (1 - alpha) × (angle + gyro × dt) + alpha × accelerometer_angle
```
де `alpha ~ 0.02`. Працює достатньо для базових дронів.

### Q21: Quaternions vs Euler angles — у чому фішка?

**ПОВНА ВІДПОВІДЬ:**

**Euler angles** — три кути (roll, pitch, yaw):
- Інтуїтивно зрозуміло
- ❌ Має **gimbal lock** — коли pitch = 90°, втрачається ступінь свободи
- ❌ Інтерполяція між кутами стрибає

**Quaternions** — 4-компонентна "число-вектор":
```
q = w + xi + yj + zk
```
де `w` — скаляр, `(x, y, z)` — вектор обертання × sin(angle/2).

- ✅ Без gimbal lock
- ✅ Гладка інтерполяція (slerp)
- ✅ Швидке множення (комбінувати обертання)
- ❌ Менш інтуїтивні

**На дронах:**
- Усередині sensor fusion / EKF — завжди quaternions
- На UI / для людини — конвертують у Euler

### Q22: IMU — що всередині і як використовується?

**ПОВНА ВІДПОВІДЬ:**
IMU (Inertial Measurement Unit) — комбіно́ваний сенсор:
- **Accelerometer** — лінійне прискорення по 3 осях (g)
- **Gyroscope** — кутова швидкість по 3 осях (deg/s)
- Часто також **Magnetometer** — компас (мT)

Популярні моделі: **MPU-6050** (accel+gyro), **MPU-9250** (+ magnetometer), **BNO055** (вбудована sensor fusion).

**Інтерфейс:** I²C або SPI. На дроні зазвичай SPI (швидше).

**Використання:**
1. Read raw accel/gyro дані (1-8 kHz)
2. Apply calibration (offset, scale)
3. Filter (low-pass for accel, high-pass for gyro)
4. Sensor fusion → orientation
5. Передати в PID для корекції

### Q23: Які протоколи між полетним контролером і RC-приймачем?

**ПОВНА ВІДПОВІДЬ:**

**PWM (старий)** — окремий провід на кожен канал, 1-2 мс pulse в період 20 мс.
- 6 каналів = 6 проводів. Не масштабується.

**PPM (Pulse Position Modulation)** — один провід, послідовність пульсів, кожен інтервал кодує канал.

**SBUS (Futaba)** — інверто́ваний UART (100k baud), 16 каналів у пакеті.
- Стандарт у consumer FPV-індустрії

**IBUS (FlySky)** — UART, два провода (бі-direkt — телеметрія назад)

**CRSF (Crossfire / ELRS)** — низько-затримковий протокол від TBS, 921k baud, до 16 каналів + телеметрія
- **Найпопулярніший** для FPV в 2024-2026

**Більшість полетних контролерів** підтримують всі через UART і автодетектять.

### Q24: Як працює GPS на дроні?

**ПОВНА ВІДПОВІДЬ:**
GPS-receiver приймає сигнали від мінімум 4 супутників, обчислює свою позицію через triangulation (по факту — 3D + час).

**На дроні:**
1. GPS-модуль (наприклад, **u-blox NEO-M8N** або **u-blox F9P**) спілкується з польотним контролером через UART
2. Дані передаються у **NMEA** (текстовий) або **UBX** (бінарний u-blox protocol)
3. Польотний контролер парсить, дає в EKF разом з IMU

**Важливо:**
- **HDOP/VDOP** — Horizontal/Vertical Dilution of Precision. Чим менше — тим краща геометрія супутників.
- **RTK GPS** — corrections від базової станції, точність до сантиметрів. Дорого ($$$), потрібно для professional UAV.
- **GPS-spoofing / jamming** — реальна загроза в miltech-контексті. Тому на дронах часто **multi-constellation** (GPS + GLONASS + Galileo + BeiDou) і fallback на VIO (Visual-Inertial Odometry).

### Q25: ROS2 — для чого використовують у дронах?

**ПОВНА ВІДПОВІДЬ:**
ROS2 (Robot Operating System 2) — middleware для distributed robotics. Це не "OS" буквально — це **набір бібліотек і ноду-механізм** для:
- Повідомлень (publish/subscribe topics)
- Сервісів (request/response)
- Actions (long-running tasks)

**На дронах ROS2 використовують переважно для:**
1. **Companion computer** (Raspberry Pi, Jetson Nano) поряд з польотним контролером
2. **High-level autonomy** — computer vision, AI, mission planning
3. **Інтеграція сенсорів** — LiDAR, depth camera, RGB camera
4. **SLAM** — Simultaneous Localization and Mapping

**Архітектура:**
```
[PX4 / ArduPilot] ←—MAVLink—→ [ROS2 (PX4-ROS2 bridge)] ←—DDS—→ [vision_node, planner_node, ...]
```

**Базові концепції для junior:**
- **Node** — процес, що щось робить
- **Topic** — канал повідомлень (наприклад, `/camera/image_raw`)
- **Publisher / Subscriber** — хто пише, хто читає
- **Message types** — стандартні (`sensor_msgs/Image`) або custom

### Q26: Які захисні протоколи / фейлсейфи на дроні?

**ПОВНА ВІДПОВІДЬ:**
Дрон без фейлсейфів = розбитий дрон. Стандартні:

1. **RC link loss** — якщо RC-сигнал зник (вийшов за дальність) → return to launch (RTL) або land
2. **Battery low** — при 20% батареї → попередження пілоту, при 15% → автоматичний RTL
3. **GPS lost** — fallback на attitude-based hold або land
4. **Geofence** — заборонена зона (наприклад, аеропорт), дрон автоматично розвертається
5. **Crash detection** — IMU фіксує різке зупинення → вимикає мотори
6. **Watchdog** на польотному контролері

**Для miltech specific:**
- **Anti-jamming** — не використовувати тільки GPS, fallback на dead reckoning через IMU
- **Encrypted telemetry** — MAVLink 2.0 signing
- **Self-destruct on capture** — політично-чутливо, зазвичай в дронах військового призначення

---

## 1.4 — LINUX / OS

### Q27: Process vs Thread — у чому різниця?

**ПОВНА ВІДПОВІДЬ:**

**Process** — незалежний виконавчий контекст з власною віртуальною пам'яттю.
**Thread** — потік виконання всередині процесу, ділить пам'ять з іншими threads того ж процесу.

| Параметр | Process | Thread |
|---|---|---|
| Memory | Own | Shared (within process) |
| Creation cost | High (fork, exec) | Low (pthread_create) |
| Context switch | Slow (TLB flush) | Fast |
| Communication | IPC (pipes, sockets, shm) | Memory directly |
| Crash impact | Doesn't affect other processes | Crashes whole process |

**Linux specific:** на Linux thread — це насправді "lightweight process" (LWP), створюється через `clone()`. У scheduler'а немає різниці.

### Q28: fork() — як працює?

**ПОВНА ВІДПОВІДЬ:**
`fork()` створює **точну копію** поточного процесу. Обидва (parent і child) продовжують виконуватись після `fork()`.

```c
pid_t pid = fork();
if (pid == 0) {
    // Я child
    printf("Child PID: %d\n", getpid());
} else if (pid > 0) {
    // Я parent
    printf("Created child PID: %d\n", pid);
} else {
    // Помилка
}
```

**Як OS це робить ефективно:**
- **Copy-on-write** — спочатку обидва процеси шерять однакові пам'ятні сторінки. Якщо хтось пише — тільки тоді копіюється відповідна сторінка.

**Типове використання:**
```c
fork() + execve() = запустити нову програму
```
Так працює shell.

### Q29: Signals — що таке, які типові?

**ПОВНА ВІДПОВІДЬ:**
Signal — асинхронне повідомлення процесу від OS чи іншого процесу.

**Топ-сигнали:**
- **SIGTERM (15)** — graceful termination request, можна обробити
- **SIGKILL (9)** — instant kill, не можна обробити чи проігнорувати
- **SIGINT (2)** — Ctrl+C
- **SIGHUP (1)** — terminal closed, традиційно — reload config
- **SIGSEGV (11)** — segmentation fault
- **SIGCHLD (17)** — дитина-процес завершилась

**Як обробити:**
```c
#include <signal.h>

void handler(int sig) {
    printf("Got signal %d\n", sig);
}

int main() {
    signal(SIGTERM, handler);
    while (1) pause();
}
```

**Production:** `kill -TERM <pid>` — спершу. Якщо не вмирає — `kill -KILL <pid>`.

### Q30: Як працює `chmod` і чому 755 / 644 такі поширені?

**ПОВНА ВІДПОВІДЬ:**
В Linux у файла є три категорії:
- **u** — owner (власник)
- **g** — group
- **o** — others

І три типи дозволів:
- **r (4)** — read
- **w (2)** — write
- **x (1)** — execute (для файлу — запустити; для теки — зайти)

**Octal notation:**
```
755 = rwxr-xr-x  (owner: rwx, group: r-x, others: r-x)
644 = rw-r--r--  (owner: rw,  group: r,   others: r)
600 = rw-------  (тільки owner)
700 = rwx------  (тільки owner з execute)
```

**Поширені:**
- **755** — для виконуваних файлів і тек (всі можуть запускати, тільки owner може писати)
- **644** — для звичайних файлів (всі читають, тільки owner пише)
- **700** — для приватного директорію (`~/.ssh`)
- **600** — для приватних ключів (`~/.ssh/id_rsa`)

### Q31: systemd unit — як зробити свій сервіс?

**ПОВНА ВІДПОВІДЬ:**
systemd — система ініціалізації Linux. Сервіс описується у файлі `/etc/systemd/system/myapp.service`:

```ini
[Unit]
Description=My Application
After=network.target

[Service]
Type=simple
User=appuser
WorkingDirectory=/opt/myapp
ExecStart=/opt/myapp/bin/app
Restart=on-failure
RestartSec=5
StandardOutput=append:/var/log/myapp.log
StandardError=append:/var/log/myapp.log

[Install]
WantedBy=multi-user.target
```

**Команди:**
```bash
sudo systemctl daemon-reload          # після зміни .service файлу
sudo systemctl enable myapp           # автозапуск при boot
sudo systemctl start myapp
sudo systemctl status myapp
sudo systemctl restart myapp
sudo journalctl -u myapp -f           # логи у реальному часі
```

---

## 1.5 — JAVASCRIPT / NODE.JS (для full-stack)

### Q32: var vs let vs const — повна різниця

**ПОВНА ВІДПОВІДЬ:**

| Параметр | `var` | `let` | `const` |
|---|---|---|---|
| Scope | Function | Block (`{}`) | Block |
| Hoisting | Так, ініціалізується undefined | Так, але "Temporal Dead Zone" | Так, але TDZ |
| Re-declaration | Allowed | Error | Error |
| Re-assignment | Allowed | Allowed | Error |

```javascript
// var — function-scoped, hoisted
console.log(x);  // undefined (не error!)
var x = 5;

// let — block-scoped, TDZ
console.log(y);  // ReferenceError
let y = 5;

// const — block-scoped, immutable binding
const arr = [1, 2, 3];
arr.push(4);    // OK — об'єкт можна змінювати
arr = [];       // TypeError — посилання не можна
```

**Сучасний JS:** використовуй `const` за замовчуванням, `let` коли треба переприсвоїти, `var` — ніколи.

### Q33: Closures — що це?

**ПОВНА ВІДПОВІДЬ:**
Closure — функція, яка "пам'ятає" змінні з зовнішнього scope, навіть коли той scope вже завершився.

```javascript
function makeCounter() {
    let count = 0;
    return function() {
        count++;
        return count;
    };
}

const counter = makeCounter();
console.log(counter());  // 1
console.log(counter());  // 2
console.log(counter());  // 3
```

`count` живе у "closure" зовнішньої функції, навіть після її повернення.

**Класичний bug:**
```javascript
for (var i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 100);
}
// Виведе: 3, 3, 3 (не 0, 1, 2!)
// Бо var — function-scoped, всі timeouts ділять одну i
```

Виправлення:
```javascript
for (let i = 0; i < 3; i++) {
    setTimeout(() => console.log(i), 100);
}
// 0, 1, 2 (let — block-scoped)
```

### Q34: Event Loop — як працює?

**ПОВНА ВІДПОВІДЬ:**
JavaScript — single-threaded, але здається асинхронним завдяки event loop.

**Архітектура:**
```
[Call Stack] ← поточно виконується
[Web APIs / Node APIs] ← timers, fetch, fs, etc.
[Microtask Queue] ← Promises, queueMicrotask
[Macrotask Queue] ← setTimeout, setInterval, I/O callbacks
```

**Event loop алгоритм:**
1. Виконати все з Call Stack
2. Виконати ВСЕ з Microtask Queue (до повного спустошення)
3. Взяти ОДНУ задачу з Macrotask Queue, виконати
4. GOTO 1

**Класичний приклад:**
```javascript
console.log('1');
setTimeout(() => console.log('2'), 0);
Promise.resolve().then(() => console.log('3'));
console.log('4');

// Виведе: 1, 4, 3, 2
// (1, 4 — синхронно; 3 — microtask; 2 — macrotask)
```

### Q35: `==` vs `===` — type coercion gotchas

**ПОВНА ВІДПОВІДЬ:**

`===` — strict equality, без коерсії типів.
`==` — loose equality, конвертує типи перед порівнянням.

**Шалені приклади з `==`:**
```javascript
0 == false           // true (false → 0)
0 == ''              // true (string → 0)
0 == '0'             // true ('0' → 0)
'' == false          // true (обидва → 0)
null == undefined    // true (special case)
NaN == NaN           // false (always!)
[] == false          // true ([] → '' → 0)
[1] == true          // true ([1] → '1' → 1)
[0] == false         // true
```

**Правило:** використовуй **завжди `===`**, окрім спеціального випадку `value == null` (перевіряє null АБО undefined).

### Q36: Promise vs async/await

**ПОВНА ВІДПОВІДЬ:**
`async/await` — синтаксичний цукор над Promise. Робить асинхронний код виглядати синхронним.

```javascript
// З Promise
function fetchUser() {
    return fetch('/user')
        .then(res => res.json())
        .then(data => {
            console.log(data);
            return data;
        })
        .catch(err => console.error(err));
}

// З async/await
async function fetchUser() {
    try {
        const res = await fetch('/user');
        const data = await res.json();
        console.log(data);
        return data;
    } catch (err) {
        console.error(err);
    }
}
```

**Ключові факти:**
- `async` функція **завжди повертає Promise**
- `await` працює **тільки в async**
- `await` **зупиняє виконання функції** до резолву (але не блокує event loop!)
- Для паралельних операцій — `Promise.all`:
```javascript
const [user, posts] = await Promise.all([fetchUser(), fetchPosts()]);
```

---

## 1.6 — SQL & DATABASES

### Q37: JOIN — INNER vs LEFT vs RIGHT

**ПОВНА ВІДПОВІДЬ:**

```sql
-- INNER JOIN — тільки рядки з співпадіннями
SELECT users.name, orders.total
FROM users
INNER JOIN orders ON users.id = orders.user_id;

-- LEFT JOIN — всі з лівої таблиці + співпадіння з правої (NULL якщо немає)
SELECT users.name, orders.total
FROM users
LEFT JOIN orders ON users.id = orders.user_id;
-- Користувачі без замовлень будуть з NULL у total

-- RIGHT JOIN — навпаки (рідко використовується, замінюється LEFT)
```

**Візуально:**
```
INNER:   A ∩ B
LEFT:    A + (A ∩ B)  → всі з A
RIGHT:   B + (A ∩ B)  → всі з B
FULL:    A + B + (A ∩ B)
```

### Q38: Що таке N+1 проблема?

**ПОВНА ВІДПОВІДЬ:**
Класична продуктивна анти-патерна в ORM:

```javascript
// ПОГАНО — N+1 запитів
const users = await User.findAll();         // 1 запит
for (const user of users) {
    const orders = await Order.findAll({ where: { userId: user.id } });  // N запитів
    console.log(user.name, orders.length);
}
// Результат: 1 + N запитів
```

**Виправлення — eager loading:**
```javascript
const users = await User.findAll({
    include: [Order]  // JOIN-запит
});
// Результат: 1 запит
```

Або вручну:
```sql
SELECT users.*, orders.*
FROM users
LEFT JOIN orders ON users.id = orders.user_id;
```

### Q39: Indexes — коли допомагають, коли шкодять?

**ПОВНА ВІДПОВІДЬ:**
Index — структура (зазвичай B-tree), що прискорює пошук рядків за певною колонкою.

**Допомагає:**
- `WHERE col = X` — пошук за конкретним значенням
- `JOIN ON col` — з'єднання
- `ORDER BY col` — сортування

**Шкодить:**
- `INSERT / UPDATE / DELETE` — індекс треба оновлювати, повільніше
- Маленькі таблиці — index не дає виграшу
- Колонки з малою кардинальністю (наприклад, `is_active`: тільки 0/1) — індекс безкорисний

**Composite index:**
```sql
CREATE INDEX idx_user_email_status ON users(email, status);
-- Допомагає: WHERE email=X, WHERE email=X AND status=Y
-- НЕ допомагає: WHERE status=Y (тільки)
```

Правило **leftmost prefix**.

---

## 1.7 — ALGORITHMS / LIVE-CODING (з повними розв'язками)

### Q40: Перевірити, чи число — степінь двійки

```c
// Найкраще: O(1)
bool is_power_of_two(int n) {
    return n > 0 && (n & (n - 1)) == 0;
}
```

**Чому працює:** степінь 2 у двійковому має тільки один біт. `n - 1` має всі біти нижче нього. AND дає 0.
```
n=8:    1000
n-1=7:  0111
AND:    0000  ✓
```

### Q41: Reverse string in-place

```c
void reverse(char* s) {
    int len = strlen(s);
    for (int i = 0; i < len / 2; i++) {
        char tmp = s[i];
        s[i] = s[len - 1 - i];
        s[len - 1 - i] = tmp;
    }
}
```

```javascript
// JS варіант
function reverseString(s) {
    return s.split('').reverse().join('');
}
// Або in-place з two pointers
```

### Q42: Circular buffer — реалізація

```c
#define BUF_SIZE 64

typedef struct {
    uint8_t data[BUF_SIZE];
    volatile size_t head;  // куди писати
    volatile size_t tail;  // звідки читати
} circular_buffer_t;

void cb_push(circular_buffer_t* cb, uint8_t byte) {
    cb->data[cb->head] = byte;
    cb->head = (cb->head + 1) % BUF_SIZE;
    // Якщо head наздогнав tail — overrun, можна або ігнорувати, або зсунути tail
}

bool cb_pop(circular_buffer_t* cb, uint8_t* byte) {
    if (cb->head == cb->tail) return false;  // empty
    *byte = cb->data[cb->tail];
    cb->tail = (cb->tail + 1) % BUF_SIZE;
    return true;
}
```

### Q43: Implement debounce (JavaScript)

```javascript
function debounce(fn, delay) {
    let timeoutId;
    return function(...args) {
        clearTimeout(timeoutId);
        timeoutId = setTimeout(() => fn.apply(this, args), delay);
    };
}

// Використання
const handleSearch = debounce((query) => {
    fetch(`/search?q=${query}`);
}, 300);

input.addEventListener('input', (e) => handleSearch(e.target.value));
```

### Q44: Flatten deeply nested array

```javascript
// Recursive
function flatten(arr) {
    return arr.reduce((flat, item) => 
        Array.isArray(item) ? flat.concat(flatten(item)) : flat.concat(item)
    , []);
}

// Modern (ES2019)
arr.flat(Infinity);
```

### Q45: Реалізувати Promise.all з нуля

```javascript
function myPromiseAll(promises) {
    return new Promise((resolve, reject) => {
        const results = new Array(promises.length);
        let completed = 0;
        
        if (promises.length === 0) return resolve([]);
        
        promises.forEach((p, i) => {
            Promise.resolve(p)
                .then(value => {
                    results[i] = value;
                    completed++;
                    if (completed === promises.length) resolve(results);
                })
                .catch(reject);  // any failure → reject all
        });
    });
}
```

---

---

# 🎨 ЧАСТИНА 2 — LATEX-ОФОРМЛЕННЯ CV

## 2.1 — Чому LaTeX і коли використовувати

**Плюси:**
- Найкраща типографіка з можливих
- Версіонується через git як код
- Шаблони безкоштовні і красиві
- Експорт у PDF — pixel-perfect

**Мінуси:**
- Крута крива навчання у перші 30 хв
- Складніше робити "креативний" дизайн (Canva простіша)

**Коли:** для технічних позицій (embedded, backend, ML, академія) — LaTeX **+1 бал** до сприйняття. Для дизайн/UX/marketing — Canva краще.

## 2.2 — Шлях найменшого опору: Overleaf + готовий шаблон

### Крок 1: Зареєструйся на Overleaf
- https://www.overleaf.com
- Безкоштовний акаунт достатньо

### Крок 2: Обери базовий шаблон

**ТОП-3 шаблонів для junior software engineer:**

#### A. Jake's Resume (найпопулярніший)
- https://www.overleaf.com/latex/templates/jakes-resume/syzfjbzwjncs
- **Переваги:** мінімалістичний, ATS-friendly, 1 сторінка ідеально
- **Недоліки:** немає background/icons за замовчуванням

#### B. Awesome-CV (з іконками і кольорами)
- https://www.overleaf.com/latex/templates/awesome-source-cv/yxctzytcfpxz
- **Переваги:** Font Awesome icons, кольорові акценти, виглядає "сучасніше"
- **Недоліки:** трохи складніше кастомізувати

#### C. Deedy Resume (компактний)
- https://www.overleaf.com/latex/templates/deedy-resume/bjryvfsjdyxz
- **Переваги:** дві колонки, все на 1 сторінку, чітко
- **Недоліки:** не дуже ATS-friendly (двоколонність)

### Крок 3: Open in Overleaf → Edit

```latex
% Найпростіший приклад (Jake-style)
\documentclass[letterpaper,11pt]{article}

\usepackage{latexsym}
\usepackage[empty]{fullpage}
\usepackage{titlesec}
\usepackage{marvosym}
\usepackage[usenames,dvipsnames]{color}
\usepackage{verbatim}
\usepackage{enumitem}
\usepackage[hidelinks]{hyperref}
\usepackage{fancyhdr}
\usepackage[english]{babel}
\usepackage{tabularx}
\input{glyphtounicode}

\pagestyle{fancy}
\fancyhf{}
\fancyfoot{}
\renewcommand{\headrulewidth}{0pt}
\renewcommand{\footrulewidth}{0pt}

% Custom section formatting
\titleformat{\section}{
  \vspace{-4pt}\scshape\raggedright\large
}{}{0em}{}[\color{black}\titlerule \vspace{-5pt}]

% Helper commands
\newcommand{\resumeItem}[1]{\item\small{#1}}
\newcommand{\resumeSubheading}[4]{
  \item
    \begin{tabular*}{0.97\textwidth}[t]{l@{\extracolsep{\fill}}r}
      \textbf{#1} & #2 \\
      \textit{\small#3} & \textit{\small #4} \\
    \end{tabular*}
}

\begin{document}

%----------HEADING----------
\begin{center}
    {\Huge \scshape Stepanenko Nazar} \\ \vspace{1pt}
    \small Kyiv, Ukraine $|$ 
    \href{mailto:gangsterstepa@gmail.com}{\underline{gangsterstepa@gmail.com}} $|$ 
    \href{https://github.com/d3Par1}{\underline{github.com/d3Par1}} $|$ 
    \href{https://www.linkedin.com/in/yourhandle}{\underline{LinkedIn}}
\end{center}

%-----------EDUCATION-----------
\section{Education}
\resumeSubheading
  {Igor Sikorsky Kyiv Polytechnic Institute}{Sep. 2024 -- Jun. 2028}
  {B.Sc. Software Engineering, Group ТВ-43}{Kyiv, Ukraine}

%-----------SKILLS-----------
\section{Technical Skills}
\textbf{Languages}: C/C++, Python, JavaScript, C\#, Lua, SQL \\
\textbf{Embedded}: STM32 (learning), Raspberry Pi Pico W, ESP32, GPIO/UART/I²C/SPI \\
\textbf{Web}: Node.js, Express, REST APIs, SQLite, Bootstrap, EJS, Chart.js \\
\textbf{Tools}: Git, Linux, Docker (basic), VS Code, CLion, PlatformIO, Blender

%-----------PROJECTS-----------
\section{Projects}
\textbf{Personal Finance Manager} $|$ \emph{Node.js, Express, SQLite, Bootstrap} \\
\hspace*{1em}-- Built full-stack web app with auth, REST API, analytics dashboard \\
\hspace*{1em}-- Owned auth, accounts, dashboard end-to-end (team of 2)

\textbf{Telegram Bots} $|$ \emph{Python, aiogram, SQLite} \\
\hspace*{1em}-- Multiple bots with FSM, async patterns, webhook deployment

% ... etc

\end{document}
```

### Крок 4: Add icons / FontAwesome (Awesome-CV style)

```latex
\usepackage{fontawesome5}

% У header:
\faPhone \, +38 (063) XXX-XX-XX \quad
\faEnvelope \, gangsterstepa@gmail.com \quad
\faGithub \, github.com/d3Par1 \quad
\faLinkedin \, linkedin.com/in/yourhandle
```

Іконки доступні: `\faGithub`, `\faLinkedin`, `\faTelegram`, `\faPython`, `\faJsSquare`, `\faLinux`, `\faMicrochip`, `\faRobot` тощо. **Повний список:** https://fontawesome.com/icons

### Крок 5: Background / colors

#### Кольоровий акцент на section headers (Awesome-CV style):
```latex
\usepackage{xcolor}
\definecolor{primary}{HTML}{1F6FB2}  % синій як в Іллі

\titleformat{\section}{
  \color{primary}\Large\bfseries\scshape
}{}{0em}{}[\color{primary}\titlerule]
```

#### Світлий background на header (елегантний):
```latex
\usepackage[margin=1in]{geometry}
\usepackage{tcolorbox}

\begin{tcolorbox}[colback=blue!5!white, colframe=blue!50!white]
  \begin{center}
    {\Huge \textbf{Stepanenko Nazar}} \\
    \vspace{2pt}
    Embedded / Miltech Software Engineer
  \end{center}
\end{tcolorbox}
```

#### Бічна планка зліва (sidebar):
Для цього бери шаблон **Deedy Resume** або **Friggeri Resume** — вони вже мають sidebar.

### Крок 6: Експорт

В Overleaf натискаєш зелений **Recompile** — отримуєш PDF. Завантажуєш через **Download → PDF**.

## 2.3 — Поради з оформлення

### ✅ Що додавати
- **Іконки** — FontAwesome для контактів (телефон, email, GitHub, LinkedIn)
- **Один accent color** — синій або темно-зелений, не більше
- **Hyperlinks** — emails, GitHub, проєкти — все клікабельно у PDF
- **Білий простір** — не пхай все під зав'язку, легше сприймається

### ❌ Що НЕ додавати
- **Кілька кольорів** (більше 2 — viola)
- **Емодзі** (працює в LinkedIn, не в PDF)
- **Фото** для embedded/tech ролей (для DACH/UK треба, для US — ні)
- **Графіки skill levels** ("HTML 90%" — junk, ATS не парсить)
- **Background images** — тільки solid color light shade, інакше друк → жах

## 2.4 — ATS-friendly правила

ATS (Applicant Tracking System) — софт, що парсить CV перед людиною. Робить keyword extraction.

**Щоб ATS не зламалось:**
1. **Звичайні шрифти** — Latin Modern, Helvetica, Arial. Без custom fontів
2. **Одна колонка** — двоколонний layout ATS може поплутати порядок
3. **Текстові секції** — не зображення-картинки тексту
4. **Стандартні section headers** — Education, Experience, Skills, Projects (не "My Journey")
5. **Без таблиць** — або мінімально (Skills таблиця ОК, Projects краще списком)
6. **Без headers/footers** — ATS їх ігнорує, не клади там важливу інфу

**Тест:** скопіюй текст з PDF (Ctrl+A → Ctrl+C → вставити в notepad). Якщо текст йде у правильному порядку — ATS прочитає.

---

---

# 💼 ЧАСТИНА 3 — LINKEDIN ДЛЯ JUNIOR/TRAINEE

## 3.1 — Чому LinkedIn критичний для першої роботи

- **Рекрутери активні** — у IT приходять у DM саме з LinkedIn
- **Job board' для України** — половина вакансій тільки тут
- **Network effect** — друзі / знайомі бачать твій статус "Open to Work"

Для junior без досвіду, **LinkedIn профіль > CV** на перших етапах. CV приходить пізніше, коли вже зацепили інтерес.

## 3.2 — Структура профілю — секція за секцією

### 1. Photo (фото)
- **Чисте, ділове, фон однотонний**
- Не selfie з телефону у дзеркало
- Не з вечірки
- Сорочка / неформальна футболка нейтрального кольору
- **Усмішка** (важливо!) — рекрутери реагують позитивно
- Розмір: квадрат, мінімум 400x400, ідеал 800x800
- Tools: Photo Booth з Mac, тлф з гарною камерою + природне світло

### 2. Banner (фоновий банер)
- Розмір: **1584 × 396** пікселів
- **Не стандартний синій LinkedIn-banner** — будь-який кастом краще
- Що зробити:
  - Canva → "LinkedIn Banner" → шаблон "Tech / Developer"
  - Або: знайти безплатне фото на Unsplash (search: "code", "circuit board", "drone", "city skyline Kyiv")
  - Або: зробити простий gradient у Figma

**Приклад фрейму:**
```
[Лівобічний accent — назва спеціальності]
[Правобічно — мінімальний візуал: код, плата, схема]
```

### 3. Headline (під ім'ям)

Для **гібридного** профілю Junior:
```
Software Engineer Student @ KPI | Full-Stack (Node.js, JS) 
& Embedded (C/C++, ESP32, RPi Pico) | Open to Internship 
🇺🇦 🇫🇷 EN-C1
```

**Чому такий:**
- **Software Engineer Student** — відразу зрозуміло, junior
- **@ KPI** — авторитет університету
- **Full-Stack & Embedded** — обидва напрямки
- **Open to Internship** — сигнал рекрутерам
- **🇺🇦 🇫🇷 EN-C1** — мовні козирі (можна, на LinkedIn — ОК)

### 4. About / Summary

```
Computer Science student at Igor Sikorsky Kyiv Polytechnic Institute, 
2nd year (group ТВ-43), interested in both full-stack web development 
and embedded systems / drone software for defense applications.

🛠 What I work with:
• Web: Node.js, Express, REST APIs, SQLite, Bootstrap, Chart.js
• Embedded: C/C++, Raspberry Pi Pico W, ESP32, basic peripherals
• Languages: JavaScript, Python, C/C++, C#, Lua, SQL
• Tools: Git, Linux, Docker, VS Code, PlatformIO, Blender

🚀 Recent projects:
• Personal Finance Manager — full-stack web app (team of 2)
• Telegram Bots in Python — async patterns, webhook deployment
• Roblox Grinding Simulator — solo project with custom 3D assets
• Microcontroller hands-on practice — Pico W and ESP32

🎯 Looking for: Internship, Working Student, or Junior role 
(Kyiv / Remote / Hybrid). Excited to contribute to 
production codebases and grow under senior mentorship.

🌍 Languages: Ukrainian (native), English C1, French B1-B2, German A1-A2.

📫 Open to chat — feel free to reach out via LinkedIn or 
gangsterstepa@gmail.com.
```

### 5. Experience

> ⚠️ Тут **не пиши фейкові посади**. Пиши реальне:

```
Software Engineering Student
Kyiv Polytechnic Institute · Sep 2024 – Present
Kyiv, Ukraine

• Coursework spanning systems programming (C, C++), 
  object-oriented design (C#), and web development (Node.js, JS).
• Team-based coursework: Personal Finance Manager web app — 
  owned authentication, REST API, dashboard.
• Side projects in Python (Telegram bots), Lua (Roblox), 
  microcontroller experimentation (Raspberry Pi Pico W, ESP32).
```

Якщо є волонтерство / freelance — додавай як окремий entry чесно.

### 6. Education

```
Igor Sikorsky Kyiv Polytechnic Institute (KPI)
B.Sc. Software Engineering · Sep 2024 – Jun 2028

Group: ТВ-43

Relevant coursework:
System Software Architecture, Object-Oriented Analysis & Design,
Web Programming, Data Structures & Algorithms, 
Software Engineering Components, Operating Systems
```

### 7. Skills (15+ обов'язково — LinkedIn ранжує)

**Programming Languages:**
JavaScript · TypeScript (learning) · C · C++ · C# · Python · Lua · SQL · HTML · CSS

**Frameworks & Tools:**
Node.js · Express.js · React (learning) · Bootstrap · EJS · Chart.js · 
SQLite · python-telegram-bot · aiogram · PlatformIO · Arduino IDE · 
Blender · Git · GitHub · Linux · Docker

**Concepts:**
REST APIs · OOP · Full-Stack Development · Authentication · 
Embedded Systems · Microcontrollers · GPIO · UART · I²C · SPI · 
Real-time Systems · Software Engineering

**Soft:**
Problem Solving · Teamwork · Self-Directed Learning · 
English (C1) · French (B1-B2) · German (A1-A2)

### 8. Projects

LinkedIn має окрему секцію "Projects" — додай 4-5 ключових:

```
Personal Finance Manager
Sep 2025 - Apr 2026
Associated with KPI

Full-stack web application (Node.js + Express + SQLite + Bootstrap) 
with authentication, multi-account support, REST API, and 
interactive Chart.js dashboard. Team of 2 — owned auth, accounts, 
dashboard, API.

Skills: Node.js · Express · SQLite · Bootstrap · Authentication · REST APIs

[Link: github.com/d3Par1/Coursework_Web]
```

**Повтори для:**
- Telegram Bots
- Roblox Game Project (з Blender assets)
- Microcontroller Hands-On (Pico W / ESP32)
- University Coursework (System Software & OOP)

### 9. Languages

LinkedIn має окрему секцію:
- Ukrainian — Native or bilingual proficiency
- English — Full professional proficiency (C1)
- French — Professional working proficiency (B1-B2)
- German — Elementary proficiency (A1-A2)

### 10. Open to Work — налаштування

Click **"Open to" → "Finding a new job"** і заповни:

| Поле | Значення |
|---|---|
| **Job titles** | Software Engineer Intern, Full-Stack Developer Intern, Junior Software Engineer, Working Student Software Engineer, Embedded Engineer Intern, Junior Backend Developer, Web Developer Intern |
| **Locations** | Kyiv, Ukraine · Remote (Ukraine) · Remote (EMEA) |
| **Start date** | Immediately |
| **Job types** | Internship · Part-time · Full-time |
| **Workplace** | Remote · Hybrid · On-site |
| **Visibility** | All LinkedIn members |

### 11. Featured (закріплене)

Зверху профілю (під About) можна закріпити **3 кращі речі**:
- Посилання на найкращий GitHub repo (Coursework_Web)
- Скріншот / preview Roblox-гри
- Best рецепт / результат тестового завдання якщо є

## 3.3 — Network — як набрати 200+ зв'язків

LinkedIn рекомендує тих, хто має 500+ зв'язків. Як набрати:

1. **Однокурсники** — всі 30 з ТВ-43 → +30
2. **Старші курси** — пошук "KPI Software Engineering" → +50
3. **Викладачі** — твоїх курсів → +10
4. **HR з компаній**, що тебе цікавлять → +30
5. **KPI alumni** в IT — `KPI alumni Junior Developer` → +50
6. **Connections of connections** — після перших 200 LinkedIn пропонує 2nd-degree → +50

**Шаблон connection request:**
```
Hi [Name], I'm Nazar, a 2nd-year CS student at KPI. 
Saw your profile while exploring [embedded / web dev] in Ukraine. 
Would love to connect and follow your journey. Best, Nazar
```

⚠️ **Не спам** — connection-spam → LinkedIn restriction.

## 3.4 — Posting strategy для junior

Junior без публікацій — невидимий. Постинг прокачує organic-reach.

### Що постити (1-2 на тиждень):

**Тип 1: "Build in public" — поточний проєкт**
```
Just finished building my first STM32 project — a UART-controlled LED 
matrix display. 

Took me a weekend to figure out:
✅ Reading datasheets is a skill in itself
✅ Open-drain vs push-pull GPIOs (now I get it)
✅ debugging via UART beats blinking LEDs

Code & schematics on GitHub: [link]

What was your first embedded project?

#embedded #stm32 #learning
```

**Тип 2: "Learning in public" — нова концепція**
```
Today I finally understood the JavaScript event loop 🎯

The "aha moment" for me: microtasks (Promises) drain BEFORE 
the next macrotask (setTimeout) runs. This explains why:

  console.log('1');
  setTimeout(() => console.log('2'), 0);
  Promise.resolve().then(() => console.log('3'));
  console.log('4');

prints 1, 4, 3, 2 — not 1, 4, 2, 3.

Took me 2 hours of MDN + Philip Roberts' "What the heck is the 
event loop" talk.

#javascript #webdev #learning
```

**Тип 3: Reposts + thoughtful comment**
- Знайди пост від відомого Ukrainian dev (наприклад, з Ajax / EPAM)
- Repost з твоїм think-piece (2-3 речення)

**Тип 4: Ukrainian context**
```
Reading "Making Embedded Systems" by Elecia White on the bus today. 
Chapter on debugging via printk reminded me that the simplest tool 
often beats the fanciest debugger.

Currently spending evenings on Raspberry Pi Pico W experiments. 
Anyone else in 🇺🇦 working on hobby embedded? Would love to swap notes.

#embedded #ukraine #learning
```

## 3.5 — Як знаходити вакансії на LinkedIn

### Базовий пошук:
1. **Jobs** → шукай по назві позиції
2. **Filters:**
   - Experience level: **Internship + Entry level**
   - Date posted: **Past week**
   - Location: **Kyiv, Ukraine** + **Remote**

### Advanced пошук URL:
```
https://www.linkedin.com/jobs/search/
?keywords=embedded%20engineer%20junior
&location=Kyiv%2C%20Ukraine
&f_E=1%2C2          # Internship + Entry
&f_WT=2%2C3         # Remote + Hybrid
&f_TPR=r604800      # Past week
```

### Set up alerts:
- На кожен ключовий запит натисни **"Set Alert"**
- Отримуєш email щоразу як новий пост

### Easy Apply vs External:
- **Easy Apply** — можна подати через LinkedIn в 1 клік (тестове, CV)
- **External** — переходиш на сайт компанії, заповнюєш форму
- **External — більше зусиль, але менше конкуренція** (через спам Easy Apply)

## 3.6 — Перші 30 днів LinkedIn-стратегії

### Тиждень 1: Setup
- [ ] Photo + Banner
- [ ] Headline + About готові
- [ ] Skills 20+ додані
- [ ] Projects 4-5 додані
- [ ] Languages
- [ ] Open to Work налаштовано
- [ ] Featured 3 закріплено

### Тиждень 2: Network
- [ ] +50 connections (одногрупники, KPI alumni)
- [ ] Підписка на 20 компаній (Ajax, Grammarly, MacPaw, EPAM, Brave1...)
- [ ] Підписка на 10 топ-Ukrainian-devs

### Тиждень 3: First posts
- [ ] 1-й пост: "build in public" про embedded-проєкт
- [ ] Реакції на 5 постів інших

### Тиждень 4: Apply + DM
- [ ] 5 заявок через Easy Apply
- [ ] 5 заявок через External (cover letter persona)
- [ ] 3 DM рекрутерам (з тих, що вже постили junior-вакансії)

---

---

# 🎯 ЧАСТИНА 4 — JUNIOR / TRAINEE СПЕЦИФІКА

## 4.1 — Trainee vs Intern vs Junior — у чому різниця

| Рівень | Контракт | Зарплата | Очікування |
|---|---|---|---|
| **Trainee (unpaid)** | Стажування на 1-3 міс | 0 | Вчишся, мінімум прод-задач |
| **Trainee (paid)** | Стажування на 1-3 міс | 0-15k грн | Прості задачі під ментором |
| **Intern (paid)** | Тимчасовий 3-6 міс | 15-30k грн | Повноцінний учасник команди, малі фічі |
| **Working Student** | Гнучкий part-time | 20-40k грн | Як intern, але довгостроково |
| **Junior** | Постійний full-time | 30-60k грн | Самостійні фічі під code review |

## 4.2 — Як спілкуватись на HR-call'у саме під Trainee/Junior

### Питання: "Чого ви чекаєте від цієї ролі?"
> ❌ ПОГАНО: "Хочу, щоб мене навчали"
> ✅ ДОБРЕ: "Хочу зробити перші реальні комерційні задачі під code review, отримати feedback на свій код, і за 6 місяців вийти на рівень самостійного виконання junior-фіч."

### Питання: "Що ви вже вмієте?"
> ❌ ПОГАНО: "Базово знаю C++..."
> ✅ ДОБРЕ: "Я можу: написати CRUD-сервіс на Node.js + Express, спроектувати REST API, працювати з SQL і JOIN-ами, базово розбираюся з GPIO/UART на Pico W. Те, що ще не пробував — RTOS і STM32 bare-metal, але активно вчуся."

### Питання: "Які ваші сильні сторони?"
> ✅ "Швидко вчуся з документації — наприклад, Vide для Roblox і aiogram я підняв за вихідні. Не боюсь читати daташити і исходники — це для мене normal workflow."

## 4.3 — Що сказати, коли немає реального досвіду

### "Чи були у вас комерційні проєкти?"
> "Комерційного досвіду ще немає — ця роль буде моєю першою. Але є реальні pet-проєкти з end-to-end ownership: Telegram-боти на замовлення для друзів, повноцінна курсова як team lead на back-end. Готовий до зростання під ментора."

### "Чому вас брати, якщо у вас немає досвіду?"
> ✅ "Тому що:
> 1. Я вже вмію базу для junior-задач — могу зайти в кодбазу, читати code review, писати простий продкод.
> 2. Self-driven — у мене 6 GitHub-проєктів без когось, хто змусив.
> 3. Мовний козир — C1 EN, B1-B2 FR — для документації та комунікації з міжнародною командою.
> 4. Вкладення в мене окупиться: за 6 місяців я зможу робити те, що мідл сьогодні."

## 4.4 — Salary: як домовитись на Trainee/Junior рівні

### Психологічна установка
- Ти **не переоцінюєш себе**, якщо називаєш ринкову вилку
- Компанія **очікує**, що ти назвеш цифру
- Не дай розжалкувати тебе фразою "у нас вилка від..."

### Скрипт:
**HR:** "Які ваші очікування?"
**Ти:** "Як перша роль — пріоритет досвід і ментор. Орієнтуюсь на 20-35 тисяч на руки. Але готовий обговорити залежно від обсягу задач і годин."

**HR:** "У нас бюджет 15 тисяч"
**Ти:** "Розумію. Підкажіть, які перспективи росту через 3-6 місяців? Якщо позиція дає сильний learning і зростання до 30+, я готовий розглянути 15 на старті."

## 4.5 — Червоні прапорці для Trainee/Junior

❌ "У нас є позиція, але платити поки не можемо — за 3 місяці переведемо в paid"
**Реальність:** часто не переводять, ти даремно витрачаєш 3 місяці.

❌ "Тестове на тиждень в форматі реального проєкту"
**Реальність:** використовують безкоштовну роботу.

❌ "Ми не даємо ментора, у нас flat structure"
**Реальність:** для junior без ментора = вигоряння за 2 місяці.

❌ "Платимо в чорну на дебіткову"
**Реальність:** 0 захисту, 0 трудового стажу. Уникай.

✅ Зелені:
- Чіткий job description
- ФОП-контракт або трудовий договір
- Ментор / buddy system
- Зарплата прописана у вилці на сайті

---

---

# 📌 ФІНАЛЬНИЙ ЧЕК-ЛИСТ — як підготуватись до співбесіди

## За 2 тижні до:
- [ ] Прочитати ВЕСЬ цей файл (Q&A повторити вголос мінімум 2 рази)
- [ ] Експортувати CV з LaTeX у PDF
- [ ] Оновити LinkedIn (всі секції з частини 3)
- [ ] Зробити 1 живий embedded-проєкт (Pico W + LED + UART) — додати у GitHub з README

## За 1 тиждень до:
- [ ] Mock-інтерв'ю з другом (1 година, half EN / half UA)
- [ ] Прочитати "Making Embedded Systems" глави 1-3 (якщо embedded роль)
- [ ] LeetCode: 10 Easy задач у мові, що цікавить (C для embedded, JS для веб)
- [ ] Дослідити компанію: остані 5 новин, продукт, керівництво

## За 1 день до:
- [ ] Перечитати свій CV — будь готовий говорити про **кожен** пункт
- [ ] 3 питання до компанії — записати
- [ ] Перевірити Zoom, мікрофон, освітлення
- [ ] Виспатись (8 годин — критично)

## За 1 годину до:
- [ ] Чашка кави / води
- [ ] Сорочка / акуратний верх
- [ ] Тестова відеоконф з ким-небудь — перевірити що все працює
- [ ] Глибоке дихання — 5 хвилин

## Під час:
- [ ] Усмішка на старті
- [ ] Думай вголос
- [ ] "Не знаю" замість галюцинацій
- [ ] Записуй імена

## Після:
- [ ] Thank-you email через 24 години (короткий, 3-4 речення)
- [ ] Записати в зошит, які питання були — для майбутніх співбесід

---

# 🔥 ТОП-5 ПОРАД, ЯКІ ВИРІШУЮТЬ

1. **Чесність — твоя перевага.** Junior, який чесно каже "цього не знаю, але навчуся за тиждень" — beats junior, що ходить навколо. Тімліди прагнуть **навчуваність**, не **готовність**.

2. **Один реальний embedded-проєкт > 100 рядків теорії в CV.** STM32 Blink + UART за вечір — і ти різко обходиш конкурентів.

3. **Networking > applying.** 50% перших робіт у IT — через знайомих. Друзі-старшокурсники, KPI-alumni LinkedIn, IT-events — тут більше шансів за cold-apply.

4. **Англійська на C1 — твій стрибок.** Багато українських junior-ів мають B1-B2. C1 + готовність комунікувати = вакансії в outsourcing з $1500+ замість $700.

5. **Постійна публічна активність.** GitHub commits через `git log --since=30days` показує "ця людина не зупиняється". Те ж саме на LinkedIn — 1 пост на тиждень. Видимість = можливості.
