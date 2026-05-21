# ООА та конструювання програмних систем — Конспект

Курс: Об'єктно-орієнтований аналіз та конструювання програмних систем
Семестр 2, 2025/26
Студент: Степаненко Назар (ТВ-43)
Код лабораторних: [University-Repository/Year-2/Semester-2/OOA/LR](../../../University-Repository/Year-2/Semester-2/OOA/LR)

## Структура курсу

| Лабораторна | Тема | Файл | Статус |
|---|---|---|---|
| ЛР №1 | Принципи SOLID | [[SOLID Принципи]] | ✅ Готово |
| ЛР №2 | Породжувальні патерни | [[Породжувальні патерни]] | ✅ Готово (5 патернів) |
| ЛР №3 | Структурні патерни | [[Структурні патерни]] | ✅ Готово (7 патернів) |
| ЛР №4 | Поведінкові патерни | [[Поведінкові патерни]] | ✅ Готово (10 патернів) |
| 📚 **Теорія** | Лекції — застосування / переваги / недоліки кожного патерна | [[Теорія з лекцій]] | Лекції 1–8 |
| 🎓 **Захист** | Шпаргалка + теорія + наслідування C++/C# | [[Захист Лабораторних]] | Готово до захисту |
| ⚙️ **Rider Setup** | Підсвічування SOLID/GoF у коді — 4 техніки + ресурси для OOP | [[Rider Highlight Setup]] | Demo: SingletonPattern.cs |
| 🎨 **Rider читабельність** | Color scheme, Code Vision, Gutter Icons, плагіни (Rainbow Brackets, CodeGlance) | [[Rider Налаштування Читабельності]] | 12 секцій налаштувань |

## 📊 Звіти лабораторних — для показу в Obsidian

Красиво оформлені звіти з callouts, mermaid-діаграмами, ==highlight==, before/after таблицями:

- [[Звіти/ЛР1 — Принципи SOLID]] 🧩 — 5 порушень SOLID з виправленнями (SRP, DIP, OCP, ISP, LSP)
- [[Звіти/ЛР2 — Породжувальні патерни]] 🏗 — 5 патернів (Builder, AbstractFactory, Singleton, Prototype, FactoryMethod)
- [[Звіти/ЛР3 — Структурні патерни]] 🏛 — 7 патернів (Adapter, Facade, Proxy, Composite, Decorator, Bridge, Flyweight)
- [[Звіти/ЛР4 — Поведінкові патерни]] 🎭 — 10 патернів (Observer, Strategy, State, Memento, CoR, TemplateMethod, Command, Iterator, Mediator, Visitor)

## Зв'язок між темами

```
SOLID ──── фундамент
  │
  ├── SRP    ─→ мотивує Strategy, State, Visitor, Command
  ├── OCP    ─→ мотивує практично всі патерни GoF
  ├── LSP    ─→ обмежує дизайн ієрархій (Observer, Decorator)
  ├── ISP    ─→ мотивує Adapter, мінімальні інтерфейси
  └── DIP    ─→ фундамент Bridge, Strategy, Factory Method

GoF патерни ── 3 категорії
  ├── Породжувальні  (як створювати об'єкти)
  ├── Структурні     (як з'єднувати об'єкти)
  └── Поведінкові    (як об'єкти взаємодіють)
```

## Робочий процес лабораторної

1. Прочитати завдання у `KPI Завдання.md` (kanban).
2. Створити проєкт у `University-Repository/Year-2/Semester-2/OOA/LR/LR<N>/`.
3. Кожен патерн — окремий файл у `Patterns/`.
4. Запустити: `dotnet run` у папці проєкту.
5. Написати звіт `LR<N>.md` поряд із проєктом.

## Конвенції коду

- `.NET 9`, `<TargetFramework>net9.0</TargetFramework>`
- File-scoped namespaces, `<Nullable>enable</Nullable>`
- Кожен патерн → файл `<Pattern>Pattern.cs` із класом `<Pattern>Demo.Run()`
- Спільний `.editorconfig` (4 пробіли, CRLF, `_camelCase` для private полів)
- `global.json` пінить SDK `9.0.311` із `rollForward: latestMinor`

## Корисні матеріали

- Книга: GoF "Design Patterns: Elements of Reusable Object-Oriented Software"
- Книга: Robert C. Martin "Clean Code", "Agile Software Development: Principles, Patterns, Practices"
- Сайт: [refactoring.guru](https://refactoring.guru/uk/design-patterns) — українською!
- Сайт: [sourcemaking.com/design_patterns](https://sourcemaking.com/design_patterns)
