# SOLID — Принципи об'єктно-орієнтованого проєктування

> Лабораторна №1. Курс ООА.
> Код звіту: [University-Repository/.../OOA/LR/LR1.md](../../../University-Repository/Year-2/Semester-2/OOA/LR/LR1.md)
> Дедлайн: 24.02.2026 ✅

SOLID — це акронім п'яти принципів, які сформулював Robert C. Martin. Вони визначають, що означає "хороший дизайн" в ООП. Дотримання SOLID робить код модульним, розширюваним, і простим у тестуванні.

## Загальна таблиця

| Літера | Принцип | Що означає | Симптом порушення |
|---|---|---|---|
| **S** | Single Responsibility | Один клас — одна причина для зміни | Бог-клас, який робить усе |
| **O** | Open/Closed | Відкритий для розширення, закритий для модифікації | Безліч `if`/`switch` за типом |
| **L** | Liskov Substitution | Підкласи замінювані на батьків | Підклас "ламає" контракт батька |
| **I** | Interface Segregation | Малі спеціалізовані інтерфейси | `NotImplementedException` у реалізації |
| **D** | Dependency Inversion | Залежність від абстракцій, а не конкретних класів | Прямі `new` у конструкторі високого рівня |

## S — Single Responsibility Principle

> "Клас повинен мати лише одну причину для зміни."

### Завдання 1 з ЛР1

`Client.Add()` робив 4 речі: валідація, збереження в БД, надсилання email, контроль помилок. Зміна формату email = зміна `Client` = зміна моделі даних. Це конфлікт відповідальностей.

### Виправлення

```csharp
Client            // тільки дані
ClientValidator   // тільки валідація
ClientRepository  // тільки БД
EmailService      // тільки пошта
ClientService     // оркестрація — це теж єдина відповідальність
```

### Чому SRP важливий

- **Тестування**: можна тестувати валідацію без БД і пошти.
- **Зміни**: правка SMTP-настройок не торкається моделі.
- **Розуміння**: ім'я класу пояснює, що він робить.

### Як виявити порушення

Якщо у назві класу є "And" (`ClientAndEmailService`) або у методах різні рівні абстракції (`SaveToDb()` + `SendEmail()`) — це червоний прапор.

## O — Open/Closed Principle

> "Програмні сутності повинні бути відкритими для розширення, але закритими для модифікації."

### Завдання 3 з ЛР1

`CarRental.Rent()` мав `if (rentType == Daily) ... if (rentType == Weekly) ...`. Кожен новий тип оренди — модифікація працюючого методу.

### Виправлення (Strategy pattern)

```csharp
abstract class RentalStrategy { abstract Calculate(...); }
class DailyRental : RentalStrategy { ... }
class WeeklyRental : RentalStrategy { ... }
class HourlyRental : RentalStrategy { ... }  // ← новий — БЕЗ зміни CarRental
```

### Зв'язок з патернами

OCP — це ідеологічний фундамент майже всіх GoF-патернів:
- Strategy, State, Command — розширення через додавання класів
- Decorator — розширення через композицію
- Visitor — розширення новими операціями
- Template Method — розширення через override

## L — Liskov Substitution Principle

> "Об'єкти підкласу повинні бути замінні на об'єкти базового класу без порушення коректності."

### Завдання 5 з ЛР1

`Square : Rectangle`. Здавалося б, квадрат — це прямокутник. Але `Square.Width = 5` змінює і `Height`. Метод, що працює з `Rectangle`, не очікує такої поведінки → площа стає неправильною.

### Виправлення

Не успадковувати `Square` від `Rectangle`. Натомість — спільний інтерфейс `IShape`:

```csharp
interface IShape { double Area { get; } }
class Rectangle : IShape { double Height; double Width; ... }
class Square    : IShape { double Side; ... }
```

### Контракт — це не лише сигнатура

LSP стосується **семантики**, не лише типів. Підклас не може:
- Викидати винятків, які не очікує батько.
- Посилювати передумови (вимагати більшого від клієнта).
- Послаблювати постумови (повертати менше, ніж обіцяв батько).

### Приклад порушення

`File.Read()` повертає рядок, `BinaryFile.Read()` повертає масив байтів через override → клієнт `File`-абстракції падає при роботі з BinaryFile.

## I — Interface Segregation Principle

> "Клієнти не повинні залежати від інтерфейсів, які вони не використовують."

### Завдання 4 з ЛР1

`IEnroll { Validate(); Persist(); SendEmail(); SendSMS(); }`. Продукти не мають email — змушені кидати `NotImplementedException`.

### Виправлення

```csharp
interface IValidatable     { void Validate(); }
interface IPersistable     { void Persist(); }
interface IEmailNotifiable { void SendEmail(); }
interface ISmsNotifiable   { void SendSMS(); }

class ProductEnroll : IValidatable, IPersistable           // лише потрібне
class ContactEnroll : IValidatable, IPersistable, IEmailNotifiable, ISmsNotifiable
```

### Як виявити

- `throw new NotImplementedException()` у реалізації → ISP порушено.
- `if (something)` де метод вирішує "робити чи ні" → ISP порушено.
- Великі інтерфейси з 10+ методами → майже завжди ISP порушено.

## D — Dependency Inversion Principle

> "Залежати потрібно від абстракцій, а не від конкретних класів. Високорівневі модулі не повинні залежати від низькорівневих."

### Не з ЛР1, але приклад

```csharp
// Погано: ClientService жорстко прив'язаний до SQL-репозиторію
class ClientService {
    private readonly SqlClientRepository _repo = new();  // ← конкретний клас
}

// Добре: залежимо від абстракції
class ClientService {
    private readonly IClientRepository _repo;
    public ClientService(IClientRepository repo) => _repo = repo;
}
```

### DI / IoC контейнери

DIP — це теоретична основа всіх DI-фреймворків (`Microsoft.Extensions.DependencyInjection`, Autofac, Ninject). Вони підставляють залежності зовні через конструктор.

### DIP ≠ DI

- **DI (Dependency Injection)** — техніка передачі залежностей через конструктор/сетер.
- **DIP (Dependency Inversion Principle)** — принцип, який каже залежати від абстракцій. DI — один зі способів його дотриматись.

## SOLID у моїй курсовій (finance-app)

Хоча `finance-app` — це Node.js (без класів-фабрик), принципи застосовуються:

- **SRP**: окремі модулі для auth, accounts, dashboard, charts, API.
- **OCP**: різні стратегії експорту (CSV/PDF/JSON) додаються без зміни ядра.
- **ISP**: окремі router-and і middleware замість мегаконтролера.
- **DIP**: `db.js` повертає інтерфейс, а не SQLite напряму — теоретично можна замінити на PostgreSQL.

## Підсумок

| Принцип | Питання, яке варто ставити коду |
|---|---|
| SRP | "Скільки причин для зміни має цей клас?" |
| OCP | "Чи доведеться мені правити цей файл, коли додам новий тип Y?" |
| LSP | "Чи зможу я підставити підклас замість батька і нічого не зламається?" |
| ISP | "Чи реалізують класи всі методи інтерфейсу, чи частина — заглушки?" |
| DIP | "Від чого залежить мій клас — від конкретного класу чи від інтерфейсу?" |

[[README|← Назад до конспекту ООА]]
