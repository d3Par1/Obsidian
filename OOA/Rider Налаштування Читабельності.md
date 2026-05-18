# Rider — Налаштування читабельності коду

> Як налаштувати Rider, щоб **візуально розрізняти** функції, успадковані члени, override-методи, інтерфейси, статичні класи; бачити **ієрархію** успадкування одним кліком; **підсвічувати** дужки, відступи, поточний символ. Усі рекомендації — для версії **Rider 2024.1+**.

## Зміст
1. [[#1. Швидкий старт — 10 must-have налаштувань]]
2. [[#2. Кольорове підсвічування ідентифікаторів]]
3. [[#3. Gutter icons (іконки на полях)]]
4. [[#4. Code Vision (показ usages / inheritors над декларацією)]]
5. [[#5. Inlay Hints (підказки в коді)]]
6. [[#6. Sticky Lines (прикріплений заголовок)]]
7. [[#7. Highlight Usages (підсвічування поточного символу)]]
8. [[#8. Method Separators (роздільники між методами)]]
9. [[#9. Плагіни — топ-7 для читабельності]]
10. [[#10. Хоткеї для навігації по OOP-структурам]]
11. [[#11. Color scheme — рекомендації]]
12. [[#12. Як перевірити, що все працює]]

---

## 1. Швидкий старт — 10 must-have налаштувань

Ці налаштування ввімкнути за **5 хвилин** — і код вже стане набагато читабельніший:

| # | Settings path | Що дає |
|---|---|---|
| 1 | `Editor → Color Scheme → C# → Identifiers` → enable various italic/bold | Розрізнення static / inherited / override |
| 2 | `Editor → General → Code Vision` → enable all | "5 usages", "2 inheritors" над методами |
| 3 | `Editor → General → Gutter Icons` → check all | Стрілки ↑↓ для override/inheritance |
| 4 | `Editor → General → Sticky Lines` → enable | Заголовок класу залишається зверху |
| 5 | `Editor → General → Highlight current line` → ☑ | Виділення поточного рядка |
| 6 | `Editor → General → Appearance` → ☑ Show method separators | Лінія між методами |
| 7 | `Editor → Inlay Hints → C#` → enable parameter names + type hints | Підказки прямо у коді |
| 8 | `Editor → Color Scheme → C# → Brace matcher` → bold + color | Підсвічування пари дужок |
| 9 | `Editor → General → Editor Tabs` → Show tabs in multiple rows | Зручніше з багатьма файлами |
| 10 | `Editor → Font` → use Cascadia Code or JetBrains Mono | Лігатури `=>`, `!=`, `>=` як один символ |

---

## 2. Кольорове підсвічування ідентифікаторів

**Файл**: `File → Settings → Editor → Color Scheme → C# → Identifiers`

Тут можна **окремо** налаштувати кожен тип ідентифікатора. Рекомендована конфігурація для дослідження OOP-коду:

### Класи та інтерфейси

| Ідентифікатор | Налаштування | Чому |
|---|---|---|
| `Class` | звичайний (defaults) | Базовий випадок |
| `Interface` | `Foreground = #B5CEA8` (м'який зелений) + italic | Інтерфейси одразу видно як абстракції |
| `Abstract class` | italic | Підкреслює, що клас не можна інстанціювати |
| `Static class` | underline | Виділяє утилітарні класи |
| `Sealed class` | звичайний | Не виділяти — це норма |

### Методи

| Ідентифікатор | Налаштування | Чому |
|---|---|---|
| `Method` | звичайний | Базовий |
| `Static method` | italic | Розрізняє Singleton.Instance vs instance.Method() |
| `Extension method` | italic + другий колір | Видно, що це extension, не "родний" метод |
| `Virtual method` | bold | Видно, що метод можна override |
| `Override method` | bold + інший колір | Видно, що це переозначення |

### Поля та властивості

| Ідентифікатор | Налаштування | Чому |
|---|---|---|
| `Field` | звичайний | Стандарт |
| `Constant` | `Foreground = #4FC1FF` (синій) + bold | Виділяє `const` |
| `Static field` | italic | Розрізняє з instance field |
| `Mutable local variable` | underline | Видно, що змінна змінюється — важливо для immutability |
| `Inherited member` | italic + темно-сірий | Видно, що метод/поле успадковане |
| `Property` | звичайний | Базовий |
| `Auto property` | звичайний | Базовий |

### Як саме клікати

1. `File → Settings` (Ctrl+Alt+S)
2. В лівому пошуку набери: `C# Identifiers`
3. Розгорни `Identifiers`
4. Виділи `Static method` → справа змінити `Font style: Italic`
5. Повтори для кожного типу зі списку вище
6. Apply

### Готовий пресет (export/import)

Якщо лінь налаштовувати вручну — створи новий Color Scheme:
1. `File → Manage IDE Settings → Export Settings` (експортує твою поточну схему).
2. Шукай готові схеми на JetBrains Marketplace: `One Dark`, `Material Theme`, `Dracula`, `Nord` — більшість мають оптимальні defaults.

---

## 3. Gutter Icons (іконки на полях)

**Файл**: `File → Settings → Editor → General → Gutter Icons`

Ці іконки з'являються в **лівій смузі** коду (між номером рядка і самим кодом). Найкорисніші:

| Іконка | Що означає | Дія по кліку |
|---|---|---|
| ↑ (стрілка вгору) | Цей метод **override** від базового | Перехід до базового методу |
| ↓ (стрілка вниз) | Цей метод **overridden** у нащадках | Список нащадків |
| ⓘ (інтерфейс) | Метод **реалізує інтерфейс** | Перехід до інтерфейсу |
| 🔄 (рекурсія) | Метод викликає сам себе | Список рекурсивних викликів |
| 🐛 (breakpoint) | Точка зупину | Toggle breakpoint |
| ☑ | Тест проходить | Перезапустити тест |

### Налаштування

Усі іконки **ввімкнути**:
- ☑ Implements
- ☑ Implemented
- ☑ Inherits
- ☑ Inherited
- ☑ Recursive call
- ☑ Hot reload

### Як перевірити на твоєму коді

Відкрий `StatePattern.cs` ([LR4](../../../University-Repository/Year-2/Semester-2/OOA/LR/LR4/BehavioralPatterns/Patterns/StatePattern.cs)). Біля кожного `Tick()` методу у `CleaningState`, `SeekingBaseState`, `StuckState` буде стрілка ↑ — клік → перехід до базового `IVacuumState.Tick()`. Біля інтерфейсного методу `IVacuumState.Tick()` — стрілка ↓ → список 3 реалізацій.

---

## 4. Code Vision (показ usages / inheritors над декларацією)

**Файл**: `File → Settings → Editor → General → Code Vision`

Це найпотужніша feature Rider для розуміння OOP. Вона додає **над** кожною декларацією класу/методу маленький текст:

```
4 usages • 2 inheritors                    ← це Code Vision
public abstract class CrmModule
{
    3 usages                               ← усі references на цей метод
    public abstract decimal GetTotalPrice();
}
```

### Які лінзи ввімкнути

| Code Vision | Що показує |
|---|---|
| ☑ **Usages** | Скільки разів клас/метод використовується (клік → список) |
| ☑ **Inheritors** | Скільки класів його успадковують |
| ☑ **Author** | Хто останній модифікував (з git blame) |
| ☑ **Code quality** | Скільки коментарів / warnings у методі |
| ☐ **Time author** | Час останньої зміни (надлишково) |

### Position

`Editor → Inlay Hints → Code Vision → Position` → `Top` (над декларацією) — найкраще для читабельності.

---

## 5. Inlay Hints (підказки прямо в коді)

**Файл**: `File → Settings → Editor → Inlay Hints → C#`

Inlay hints — це **сірі підказки прямо в коді**, які не є реальним кодом. Виглядає так:

```csharp
// Без hints
new Character(name: ...);   // ← треба пам'ятати назви параметрів

// З hints
new Character(name: "Назар", class: Warrior, hp: 100);
//             ↑         ↑              ↑
//             hint     hint           hint
```

### Топ inlay hints для C#

| Hint | Що показує | Корисність |
|---|---|---|
| **Parameter name hints** | Назви параметрів у викликах | 🔥 Must-have для патернів |
| **Type hints for var** | `var x` → `var x: int` | 🔥 Зрозуміти що повертає Factory |
| **Type hints for lambdas** | `(x) => ...` → `(x: int) => ...` | Зрозуміти LINQ |
| **Return type hints** | Видно return type у multiline expression | Корисно |
| **Range indexer hints** | `arr[0..5]` → `arr[0..5: 5 items]` | Менш критично |

### Налаштування

1. `Settings → Editor → Inlay Hints → C# → Implicit`
2. Усе ввімкнути.
3. Натиснути Apply і поглянути на свій код у `BuilderPattern.cs`:
   ```csharp
   .SetStats(str: 20, intel: 8, agi: 14)
   //         ↑       ↑          ↑
   //       hints (Rider додає, бо параметри названі — у тебе вже добре!)
   ```

Якщо подразнюють — натисни `Alt+H` → toggle. Hotkey для on/off.

---

## 6. Sticky Lines (прикріплений заголовок)

**Файл**: `File → Settings → Editor → General → Sticky Lines`

Коли ти скролиш всередині великого класу, **заголовок класу** і поточний метод **прикріпляються до верху редактора**. Так ти завжди знаєш, у якому контексті знаходишся.

### Налаштування

- ☑ Enable sticky lines
- Max lines: `4` (показує до 4 рівнів: namespace → class → method → if-блок)
- Color: трохи світліший за фон редактора

### Як виглядає

```
─────── Sticky area ───────
namespace BehavioralPatterns.Patterns;
public sealed class VacuumRobot
public void Tick()
    if (Battery < 20)
────────────────────────────
                              ← курсор тут, але контекст видно
   Console.WriteLine(...);
```

Особливо корисно у твоїх 200+-рядкових файлах (наприклад, `CommandPattern.cs`).

---

## 7. Highlight Usages (підсвічування поточного символу)

**Файл**: `File → Settings → Editor → General → Highlight Usages`

Коли курсор на змінній / методі / класі — **усі вживання цього символу у файлі підсвічуються**. Зручно зрозуміти, де ще використовується змінна.

### Налаштування

- ☑ Highlight usages on caret
- ☑ Highlight write-usages distinctly (write — інший колір ніж read)
- Color: `Background = #2D4F1E` (приглушений зелений) для read, `#5C2C1E` для write.

### Як використовувати

Постав курсор на `_state` у `VacuumRobot.cs` → усі місця, де `_state` читається або пишеться, підсвітяться. Видно, що поле використовується у:
- Конструкторі (write)
- `SetState()` (write)
- `Tick()` (read)

Це дає швидке розуміння **lifecycle** змінної.

---

## 8. Method Separators (роздільники між методами)

**Файл**: `File → Settings → Editor → General → Appearance` → ☑ Show method separators

Додає тонку горизонтальну лінію між методами:

```csharp
public class Foo
{
    public void Method1() { ... }
─────────────────────────────────────
    public void Method2() { ... }
─────────────────────────────────────
    public void Method3() { ... }
}
```

Маленька деталь, але дуже допомагає швидко "відстрибувати" поглядом між методами.

---

## 9. Плагіни — топ-7 для читабельності

`File → Settings → Plugins → Marketplace` → пошук.

### 9.1 Rainbow Brackets (JetBrains official)

**Що**: кожна пара дужок `()`, `[]`, `{}` — свого кольору. Видно, де закривається кожна.

**Особливо корисно у твоєму коді** — patterns мають вкладені `new XxxDecorator(new YyyDecorator(...))`, де порахувати дужки складно.

**Marketplace**: пошук "Rainbow Brackets" → JetBrains s.r.o.

### 9.2 Indent Rainbow

**Що**: кожен рівень відступу — свого кольору фону.

**Корисно**: у твоїх `Composite` (CRM-модулі) є вкладені блоки `.Add(new CompositeModule(...).Add(...))` — Indent Rainbow одразу показує рівні.

### 9.3 CodeGlance Pro

**Що**: мінімапа праворуч (як у Sublime / VS Code). Видно структуру файлу одразу.

**Корисно**: для файлів типу `CommandPattern.cs` (200+ рядків) — швидка навігація.

### 9.4 Key Promoter X

**Що**: коли ти робиш дію мишкою — показує спливаюче "цю дію можна було зробити хоткеєм Alt+F7". Через тиждень знатимеш усі хоткеї.

**Корисно**: для захисту — швидка робота з кодом справляє враження.

### 9.5 Material Theme UI

**Що**: набір тем (Darker, Palenight, Oceanic, Lighter). Виглядає просто, читабельно.

**Альтернативи**: One Dark Pro, Dracula Theme, Nord. Усі добрі — обирай за смаком.

### 9.6 Atom Material Icons

**Що**: різні іконки для типів файлів (`.cs`, `.csproj`, `.md`, `.json`). У дереві проєкту видно, що є що.

### 9.7 Roslynator

**Що**: 500+ додаткових code inspections та refactorings. Підкаже, де можна спростити код (`if-else` → expression-bodied, `string.Format` → interpolation).

**Корисно**: на захисті можна сказати: "Roslynator не знайшов проблем у моєму коді" — це доказ якості.

### Установка всіх 7 одразу

```
Settings → Plugins → Marketplace
Шукати → Install:
  - Rainbow Brackets
  - Indent Rainbow
  - CodeGlance Pro
  - Key Promoter X
  - Material Theme UI
  - Atom Material Icons
  - Roslynator
Restart Rider
```

Усі — безкоштовні.

---

## 10. Хоткеї для навігації по OOP-структурам

### Топ-10 для розуміння OOP

| Hotkey | Що робить | Коли використовувати |
|---|---|---|
| `Ctrl+B` (або `F12`) | **Go to Declaration** | Перейти до того, на чому курсор |
| `Ctrl+Alt+B` | **Go to Implementation** | Інтерфейс → реалізація |
| `Ctrl+U` | **Go to Base Symbol** | Override → базовий метод |
| `Ctrl+H` | **Type Hierarchy** | Дерево всіх класів-нащадків |
| `Ctrl+Alt+H` | **Call Hierarchy** | Хто викликає цей метод |
| `Alt+F7` | **Find Usages** | Усі місця, де клас/метод використовується |
| `Ctrl+Shift+I` | **Quick Definition** | Превью без переходу |
| `Ctrl+Q` | **Quick Documentation** | Hover-tooltip з XML doc |
| `Ctrl+F12` | **File Structure** | Структура поточного файлу |
| `Ctrl+E` | **Recent Files** | Перемикання між файлами |

### Спеціально для патернів

**Сценарій 1**: розібратися як працює `Composite` (ЛР3 завдання 4).
1. Відкрий `CompositePattern.cs`.
2. Постав курсор на `CrmModule` → `Ctrl+H` → побачиш `LeafModule` і `CompositeModule` як нащадків.
3. Постав курсор на `GetTotalPrice()` у `CrmModule` → `Ctrl+Alt+B` → меню "Implementations" → перейдеш до реалізації.
4. Постав курсор на `Add()` у `CompositeModule` → `Alt+F7` → побачиш усі місця, де модулі додаються в композит.

**Сценарій 2**: зрозуміти ланцюг Mediator-у (ЛР4).
1. Відкрий `MediatorPattern.cs`.
2. Постав курсор на `Send()` у `AirportTowerMediator` → `Ctrl+Alt+H` → "Calls of method" → побачиш ланцюг викликів.
3. Постав курсор на `AirportParticipant` → `Ctrl+H` → побачиш усіх 4 нащадків.

### Корисні хоткеї редактора

| Hotkey | Що робить |
|---|---|
| `Ctrl + Shift + Numpad -` | Згорнути все (collapse all regions) |
| `Ctrl + Shift + Numpad +` | Розгорнути все |
| `Ctrl + W` | Розширити виділення (intelligent select) |
| `Ctrl + Shift + W` | Звузити виділення |
| `Alt + Up/Down` | Переміщення між methods |
| `Ctrl + /` | Закоментувати рядок |
| `Ctrl + Shift + /` | Закоментувати блок `/* */` |
| `Ctrl + D` | Дублікат рядка |
| `Ctrl + Shift + Up/Down` | Переміщення рядка/блоку |

---

## 11. Color scheme — рекомендації

### Готові схеми, що добре підходять для C# та OOP-коду

| Схема | Стиль | Кому підходить |
|---|---|---|
| **Darcula** (default Rider) | Темна, нейтральна | Стандарт, нічого не зламається |
| **One Dark Pro** | Темна, м'які кольори | Найпопулярніша серед розробників |
| **Material Theme — Palenight** | Темна, фіолетовий акцент | Гарний для тривалої роботи |
| **Nord** | Темна, холодний синьо-сірий | Мінімалізм, втома очей низька |
| **GitHub Light** / **Solarized Light** | Світла | Якщо багато світла навколо |

### Як змінити

1. `File → Settings → Editor → Color Scheme → Scheme:` → вибери зі списку.
2. Або встанови Material Theme UI плагін (див. секцію 9) → буде ширший вибір.

### Мій топ-рекомендація

**Для захисту лабораторних** — стандартна **Darcula**:
- Усі викладачі звикли.
- Не виглядає "перевантажено".
- Усі рекомендації цього файлу налаштовані для неї.

**Для повсякденної роботи** — **One Dark Pro**: легше очам після 4 годин.

---

## 12. Як перевірити, що все працює

Після всіх налаштувань відкрий `SingletonPattern.cs` (з [Annotations.cs](../../../University-Repository/Year-2/Semester-2/OOA/LR/LR2/CreationalPatterns/Annotations.cs) + анотаціями). Перевір:

| Феча | Що бачиш |
|---|---|
| **Sticky Lines** | Скрол всередині `LogService` — заголовок класу залишається зверху |
| **Code Vision** | Над `LogService` написано `4 usages` (або скільки є) |
| **Gutter Icons** | Біля `Log()` методу — звичайно нічого; біля `Instance` — нічого |
| **Inlay Hints** | У `Log("Auth", "...")` показано `module: "Auth", message: "..."` |
| **Color Scheme** | `LogService` — як клас, `Instance` — як static property (italic) |
| **Highlight Usages** | Курсор на `_instance` → всі вживання у файлі підсвічені |
| **Method Separators** | Між `Log()` методом і `Instance` property — горизонтальна лінія |
| **Rainbow Brackets** | `if (_instance is null) { lock (_lock) { _instance ??= new(); } }` — кожна пара дужок свого кольору |
| **`[Applies]` Find Usages** | `Alt+F7` на `AppliesAttribute` → список усіх класів |

Якщо все це бачиш — ти готовий до захисту.

---

## Як це все допомагає на захисті

1. **Hover на класі** → tooltip з XML doc показує, які SOLID-принципи демонструє клас.
2. **Ctrl+H на CrmModule** → відкривається дерево нащадків (Leaf + Composite) — викладач бачить класичний Composite-патерн.
3. **Code Vision "2 inheritors"** → одразу видно, що клас є базовим.
4. **Gutter icons ↑** біля `Tick()` у `CleaningState` → ілюструє override.
5. **Rainbow Brackets у Decorator** — викладач бачить, скільки рівнів вкладено: `new AuditDecorator(new EncryptDecorator(new CompressDecorator(new PlainDoc())))` — 4 пари дужок 4-х кольорів.

---

## Швидкий чеклист — за 15 хвилин до захисту

- [ ] `Ctrl+Alt+S` → Color Scheme → налаштувати identifiers (5 хв).
- [ ] Editor → Code Vision → ввімкнути usages + inheritors (1 хв).
- [ ] Editor → Gutter Icons → ☑ all (1 хв).
- [ ] Editor → Sticky Lines → enable (30 сек).
- [ ] Editor → Inlay Hints → ввімкнути parameter names (1 хв).
- [ ] Install plugins: Rainbow Brackets, CodeGlance Pro, Indent Rainbow (5 хв з рестартом).
- [ ] Перевірити на `SingletonPattern.cs` (1 хв).

[[README|← Назад]] · [[Rider Highlight Setup|Custom Annotations]] · [[Захист Лабораторних|Захист →]]
