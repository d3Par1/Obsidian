# Rider — Підсвічування SOLID / GoF / GRASP у коді

> Як налаштувати JetBrains Rider, щоб клас, метод чи рядок коду візуально позначався який принцип/патерн він демонструє. Робоча демонстрація — у файлі `SingletonPattern.cs` ([LR2](../../../University-Repository/Year-2/Semester-2/OOA/LR/LR2/CreationalPatterns/Patterns/SingletonPattern.cs)).

## Підсумок: 4 техніки, що працюють разом

| # | Техніка | Що дає | Складність |
|---|---|---|---|
| 1 | **TODO-pattern з кольором** | Кольоровий маркер у TODO-вікні, підсвічування коментарів | ⭐ Найшвидше |
| 2 | **#region directives** | Складуваний блок із заголовком "SOLID + GoF analysis" | ⭐ |
| 3 | **XML doc comments** | При hover над класом — повний tooltip з усіма принципами | ⭐⭐ |
| 4 | **`[Applies]` attribute** | Запит "де ми використовуємо SOLID:SRP" через Find Usages | ⭐⭐⭐ Найімпресивніше |

Усі чотири — НЕ взаємовиключні. Реальна демо у `SingletonPattern.cs` поєднує всі 4.

---

## Техніка 1. TODO-pattern з кольоровою категорією

### Що пишеш у коді

```csharp
// SOLID:SRP — клас має одну відповідальність — логування
// SOLID:DIP — ПОРУШЕНО: клієнти залежать від конкретного класу
// TODO[GoF:Singleton]: перевірити double-check locking
// TODO[Concurrency]: розглянути Lazy<T> як ідіоматичну альтернативу
```

### Як налаштувати Rider один раз

1. `File → Settings` (або `Ctrl+Alt+S`)
2. `Editor → TODO`
3. Натисни `+` (Add Pattern):

**Pattern А — SOLID-маркери:**
- **Pattern**: `\bSOLID:\w+\b.*`
- **Case sensitive**: ☑
- **Use color scheme `TODO`**: змінити на власний → `Foreground = #4FC3F7` (блакитний)

**Pattern Б — GoF-патерни:**
- **Pattern**: `\bGoF:\w+\b.*`
- **Foreground = #81C784** (зелений)

**Pattern В — GRASP:**
- **Pattern**: `\bGRASP:\w+\b.*`
- **Foreground = #FFB74D** (оранжевий)

**Pattern Г — Категоризований TODO:**
- **Pattern**: `\bTODO\[[A-Z][\w:]+\]:.*`
- **Foreground = #BA68C8** (фіолетовий)

4. Apply → OK.

### Результат

- У редакторі коментарі `// SOLID:SRP — ...` підсвічуються блакитним.
- `Tools → View → TODO` (Alt+6) показує усі ці коментарі згруповано.
- Можна фільтрувати: бачити лише SOLID-маркери, лише GoF, лише TODO.

### Плюс

Прямо на захисті можна сказати: "Дивіться, я можу відкрити TODO-панель і побачити ВСІ застосування SOLID у проєкті за 1 клік" — і відкриваєш список.

---

## Техніка 2. #region directives

### Що пишеш

```csharp
#region GoF:Singleton + SOLID-аналіз

public sealed class LogService
{
    // ...
}

#endregion
```

### Що дає

- У редакторі Rider біля номера рядка з'являється `[+]` — клас можна **згорнути** одним кліком.
- При згорнутому стані видно тільки заголовок region — це фактично "тема" блоку.
- Rider Structure View (Alt+7) показує regions окремою категорією — навігація стає швидшою.

### Best practice

Заголовок region — це не просто назва патерну, а **категорія аналізу**:
- `#region GoF:Decorator — клієнт-сторона`
- `#region SOLID:OCP — точки розширення`
- `#region GRASP:LowCoupling — інтерфейсна границя`

---

## Техніка 3. XML doc comments

### Що пишеш

```csharp
/// <summary>
/// <para><b>GoF:Singleton</b> — гарантує одиничність екземпляра.</para>
/// <para><b>SOLID:SRP — ПОРУШЕНО</b>: клас і керує життєвим циклом, і логує.</para>
/// <para><b>SOLID:DIP — ПОРУШЕНО</b>: клієнти залежать від конкретного класу.</para>
/// <para><b>GRASP:PureFabrication</b> — не існує у предметній області.</para>
/// </summary>
public sealed class LogService { ... }
```

### Що дає

- При наведенні курсором (`Ctrl + Q` або hover) на `LogService` будь-де у коді — спливає tooltip з повним аналізом принципів.
- При використанні `LogService.Instance` у інших класах — той самий tooltip.
- Bonus: на захисті можна показати "ось я hoverю — і викладач бачить, що клас одночасно демонструє Singleton, SRP (порушено), DIP (порушено) та PureFabrication".

### Синтаксис XML

- `<para>` — параграф (нова стрічка).
- `<b>...</b>` — жирний шрифт у tooltip.
- `<see cref="..."/>` — клікабельне посилання на інший клас/метод.
- `<list type="bullet">` + `<item>` — буллет-лист.

---

## Техніка 4. Custom `[Applies]` attribute

### Файл `Annotations.cs` у проєкті

Створено: [Annotations.cs](../../../University-Repository/Year-2/Semester-2/OOA/LR/LR2/CreationalPatterns/Annotations.cs)

```csharp
namespace CreationalPatterns;

[AttributeUsage(
    AttributeTargets.Class | AttributeTargets.Interface |
    AttributeTargets.Method | AttributeTargets.Struct | AttributeTargets.Property,
    AllowMultiple = true)]
public sealed class AppliesAttribute : Attribute
{
    public string Principle { get; }
    public string Note      { get; }

    public AppliesAttribute(string principle, string note = "")
    {
        Principle = principle;
        Note      = note;
    }
}
```

### Як використовувати

```csharp
[Applies("GoF:Singleton",         note: "Приватний конструктор + double-check lock")]
[Applies("SOLID:SRP",             note: "ПОРУШЕНО — керує і життєвим циклом, і логуванням")]
[Applies("SOLID:DIP",             note: "ПОРУШЕНО — клієнти залежать від конкретного класу")]
[Applies("GRASP:PureFabrication", note: "Сервіс не існує у предметній області")]
public sealed class LogService { ... }
```

### Що дає (це найкрутіше)

1. **Hover** — Rider показує усі `[Applies]` у tooltip разом з XML doc.
2. **Find Usages (Alt+F7) на `AppliesAttribute`** — Rider покаже **список ВСІХ класів у проєкті, що його використовують**. Прокрутка цього списку = огляд усіх застосованих принципів.
3. **Текстовий пошук** (`Ctrl+Shift+F`) — `Applies("SOLID:SRP"` знайде всі демонстрації SRP. `Applies("GoF:Decorator"` — всі Decorator-и.
4. **Programmatic introspection** — теоретично можна написати тест, який запускає reflection і друкує таблицю "клас → принципи". На захисті: "Я можу одним викликом отримати каталог застосувань".

### Чому це не зламає билд

`[Applies]` — звичайний `Attribute` без runtime-логіки. Анотації компілюються в метадані збірки, але не впливають на виконання. Збірка LR2 з анотаціями: 0 warnings, 0 errors.

### Розширення

Можна додати enum-варіанти замість рядків, для type-safety:

```csharp
public enum Solid { SRP, OCP, LSP, ISP, DIP }
public enum Grasp { Creator, InformationExpert, LowCoupling, HighCohesion, Controller, PureFabrication, Indirection, Polymorphism, ProtectedVariations }
public enum GofCat { Creational, Structural, Behavioral }

[AppliesSolid(Solid.SRP, note: "...")]
[AppliesGoF("Singleton", category: GofCat.Creational)]
public sealed class LogService { ... }
```

Це більш type-safe, але вимагає 3 різні атрибути. Для лабораторних — overkill, рядкова версія простіша.

---

## Усе разом — реальний приклад у моєму коді

Файл: [SingletonPattern.cs](../../../University-Repository/Year-2/Semester-2/OOA/LR/LR2/CreationalPatterns/Patterns/SingletonPattern.cs)

Що там зараз:
- `#region GoF:Singleton + SOLID-аналіз` — групує клас + аналіз.
- `/// <summary>` з `<para>` для кожного принципу — hover tooltip.
- `[Applies(...)]` × 4 — каталог-маркери для Find Usages.
- `// TODO[SOLID:DIP]:` — категоризований TODO.

Запусти Rider, відкрий цей файл, наведи курсор на `LogService` — побачиш ВСЕ це у tooltip одночасно. Спробуй `Alt+F7` на атрибуті `Applies` — побачиш список усіх класів з анотаціями (поки що один, далі додамо).

---

## Як перенести на ЛР3 та ЛР4

1. Скопіювати `Annotations.cs` із LR2 у LR3/`StructuralPatterns/` та LR4/`BehavioralPatterns/` (змінити namespace на `StructuralPatterns` чи `BehavioralPatterns` відповідно).
2. Поступово додати `[Applies]` + XML doc до основних класів кожного патерну.
3. Якщо хочеш узагальнити — винеси `Annotations.cs` у спільну `Common/` бібліотеку і референси з усіх проєктів.

Для захисту досить продемонструвати **на одному файлі** (Singleton) і сказати: "за тим самим принципом анотовано всі інші патерни".

---

## Команда для switchу між regions у Rider

| Команда | Hotkey |
|---|---|
| Згорнути всі regions | `Ctrl + Shift + Numpad -` |
| Розгорнути всі regions | `Ctrl + Shift + Numpad +` |
| Згорнути / розгорнути поточний | `Ctrl + Numpad -` / `+` |
| Перейти до наступної помилки/попередження | `F2` |
| Show TODO panel | `Alt + 6` |
| Structure view | `Alt + 7` |
| Find Usages | `Alt + F7` |
| Quick Documentation (hover) | `Ctrl + Q` |

---

## OOP-принципи: каталог-замінник для refactoring.guru

❗ На refactoring.guru **немає окремої сторінки** `/uk/oop-principles/catalog` — я перевірив. SOLID/GRASP/Закон Деметри там висвітлюються лише фрагментарно у вступних розділах.

Найближче за духом — це **каталог "запахів коду"** (`code smells`), бо кожен запах = порушення певного OOP-принципу.

### Рекомендований мікс ресурсів

| Ресурс | URL | Що дає |
|---|---|---|
| **Refactoring.guru — Каталог запахів коду** (uk) | https://refactoring.guru/uk/refactoring/smells | 22 запахи у 5 категоріях. **Категорія "Порушники ОО-дизайну"** прямо мапить порушення на запахи. Це найближче до "каталогу принципів" з ілюстраціями. |
| **Refactoring.guru — Каталог рефакторингу** (uk) | https://refactoring.guru/uk/refactoring/catalog | 60+ технік. Кожна техніка = спосіб дотриматися принципу. |
| **Refactoring.guru — Каталог патернів** (uk) | https://refactoring.guru/uk/design-patterns/catalog | 23 патерни GoF — те, що ти вже знаєш. |
| **Refactoring.guru — Вступ до патернів** (uk) | https://refactoring.guru/uk/design-patterns/what-is-pattern | Вступ Алекса Швеца. Тут є побіжно про OOP-принципи. |
| **Wikipedia UA — SOLID** | https://uk.wikipedia.org/wiki/SOLID | Чесні визначення, нормальна укр. термінологія. |
| **Wikipedia UA — GRASP** | https://uk.wikipedia.org/wiki/GRASP | 9 шаблонів Лармана. |
| **Wikipedia UA — Закон Деметри** | https://uk.wikipedia.org/wiki/Закон_Деметри | Коротко і по суті. |
| **Wikipedia EN — Object-oriented design** | https://en.wikipedia.org/wiki/Object-oriented_design | Найдетальніший огляд, з посиланнями на всі принципи. |
| **Wikipedia EN — SOLID** | https://en.wikipedia.org/wiki/SOLID | Розгорнутіший за UA-версію. |

### Книги (якщо хочеш глибше)

| Книга | Що дає |
|---|---|
| Robert C. Martin — **"Чиста архітектура"** (Clean Architecture) | SOLID, компонентні принципи, межі архітектури. Базова класика. |
| Robert C. Martin — **"Чистий код"** (Clean Code) | OOP-принципи через призму "як писати читабельний код". |
| Craig Larman — **"Applying UML and Patterns"** | Першоджерело GRASP. |
| GoF — **"Design Patterns: Elements of Reusable Object-Oriented Software"** | 23 патерни, оригінал. |
| Joshua Bloch — **"Effective Java"** | Java-specific, але принципи універсальні. |

### Інтерактивні ресурси

- **principlesofoop.com / oodesign.com** — англомовні каталоги принципів.
- **Stack Overflow тег `solid-principles`** — реальні кейси.

---

## Підсумок: моя рекомендація

1. **Скопіюй `Annotations.cs` у LR3 та LR4** і додай `[Applies]` до 1-2 ключових класів кожного патерну (це 30 хв роботи на всі лаби).
2. **Налаштуй TODO-patterns у Rider** один раз — і вся група анотацій у проєктах буде підсвічуватись.
3. **На захисті** — відкрий `SingletonPattern.cs`, наведи hover, покажи tooltip; натисни `Alt+F7` на `Applies` — покажи список усіх застосувань.
4. **Для теоретичних питань про OOP-принципи** — використовуй мій файл [[Теорія з лекцій]] (там 100% структуровано) + Wikipedia UA для основних термінів.

[[README|← Назад]] · [[Теорія з лекцій|Теорія →]] · [[Захист Лабораторних|Захист →]]
