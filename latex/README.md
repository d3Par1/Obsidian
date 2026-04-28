# LaTeX CV — Stepanenko Nazar

Дві версії CV у LaTeX, готові до компіляції в PDF.

## 📁 Файли

- `Stepanenko_Embedded_CV.tex` — для embedded / miltech / drone позицій
- `Stepanenko_FullStack_CV.tex` — для веб / full-stack позицій

Різниця тільки в:
- Назві позиції під ім'ям
- Порядку Skills та Projects
- Accent color (синій vs зелений — щоб візуально відрізнялись між собою)
- Domain interest і "In Progress" секціях

---

## 🚀 Як скомпілювати в PDF — Варіант 1: Overleaf (рекомендую)

**Час: 2 хвилини. Без жодного встановлення.**

1. Зайди на [https://www.overleaf.com](https://www.overleaf.com), зареєструйся (безкоштовно, можна через Google).
2. Натисни **New Project → Blank Project** → назви, наприклад, `Embedded_CV`.
3. У редакторі **повністю видали** дефолтний код (`Ctrl+A → Delete`).
4. Відкрий `Stepanenko_Embedded_CV.tex` у будь-якому редакторі (VS Code / Notepad), скопіюй увесь вміст (`Ctrl+A → Ctrl+C`).
5. Встав у Overleaf (`Ctrl+V`).
6. Натисни зелений **Recompile** (або `Ctrl+S`) — справа з'явиться preview PDF.
7. **Download → PDF** — готово.

Повтори те саме для `Stepanenko_FullStack_CV.tex` (новий проєкт).

### ⚠️ Якщо Overleaf видасть помилку щодо `fontawesome5`:
- У верхньому меню: **Menu → Compiler** → встанови **pdfLaTeX** (default).
- Якщо помилка лишається — заміни в `.tex`:
  ```latex
  \usepackage{fontawesome5}
  ```
  на
  ```latex
  \usepackage{fontawesome}
  ```
  І в коді заміни `\faMapMarker*` на `\faMapMarker` (без зірочки).

---

## 🛠 Варіант 2: Локально через Tectonic (single binary)

**Час: 5-10 хвилин. Один .exe файл, без 200+ MB MiKTeX.**

### Встановлення:
```powershell
# В PowerShell (Admin не треба):
winget install --id=TectonicTypesetting.Tectonic
```

Або вручну: завантажити [tectonic-x86_64-pc-windows-msvc.zip](https://github.com/tectonic-typesetting/tectonic/releases/latest), розпакувати, додати в PATH.

### Компіляція:
```bash
cd "D:\Obsidian Projects\KPI\KPI\latex"
tectonic Stepanenko_Embedded_CV.tex
tectonic Stepanenko_FullStack_CV.tex
```

Після першого запуску Tectonic стягне потрібні пакети (~50 MB) і збере PDF поряд з .tex.

---

## 🛠 Варіант 3: Локально через MiKTeX

**Час: 15-30 хвилин. Повний дистрибутив (~200 MB initially, до 5 GB після всіх пакетів).**

### Встановлення:
1. Зайди на [https://miktex.org/download](https://miktex.org/download).
2. Завантаж "Basic MiKTeX 64-bit Installer".
3. Запусти, обери "Install for me only", натиснь Next до кінця.
4. **Важливо:** при першій компіляції MiKTeX буде питати, чи стягнути відсутні пакети — відповідай **Yes** (це нормально).

### Компіляція через CLI:
```bash
cd "D:\Obsidian Projects\KPI\KPI\latex"
pdflatex Stepanenko_Embedded_CV.tex
pdflatex Stepanenko_FullStack_CV.tex
```

### Або через GUI:
- Відкрий `.tex` файл у TeXworks (поставиться разом з MiKTeX).
- Натисни зелену стрілку (Compile) — отримаєш PDF.

---

## ✏️ Що відредагувати перед компіляцією

В обох файлах поміняй:
- `@yourhandle` (Telegram) на свій реальний нік
- `linkedin.com/in/yourhandle` на свій LinkedIn URL після оновлення профілю
- (опціонально) додай номер телефону: між email і GitHub додай:
  ```latex
  \faPhone* \, +38 (063) XXX-XX-XX \quad
  ```

## 🎨 Як змінити accent color

У файлі знайди рядок:
```latex
\definecolor{accent}{HTML}{1F6FB2}    % Embedded — синій
\definecolor{accent}{HTML}{0A6E47}    % FullStack — темно-зелений
```

HEX-коди для популярних варіантів:
- `1F6FB2` — синій (як в Іллі)
- `0A6E47` — темно-зелений
- `8B0000` — темно-червоний (НЕ для miltech — асоціація)
- `2C3E50` — темно-синій (графітний)
- `333333` — антрацит (без кольору, мінімалізм)

## 🔠 Як змінити шрифт

За замовчуванням — **Computer Modern** (стандартний LaTeX шрифт). Якщо хочеш інший:

### Helvetica / Arial-style:
Додай у preamble (після `\documentclass`):
```latex
\usepackage{helvet}
\renewcommand{\familydefault}{\sfdefault}
```

### Modern (Inter, IBM Plex):
Потребує XeLaTeX замість pdfLaTeX:
```latex
% У Overleaf: Menu → Compiler → XeLaTeX
\usepackage{fontspec}
\setmainfont{Inter}    % або "IBM Plex Sans"
```

---

## 📤 Куди далі

Після того як отримав PDF:
1. **Перейменуй файл:** `Stepanenko_Nazar_Embedded_CV.pdf` (HR-friendly формат)
2. **Перевір ATS:** відкрий PDF, `Ctrl+A → Ctrl+C`, встав у Notepad — текст має йти у правильному порядку.
3. **Закинь у LinkedIn:** Profile → Featured → Add → Document → upload PDF.
4. **Подавай заявки** з відповідною версією під роль.

---

## ⚠️ Troubleshooting

### "Package fontawesome5 not found"
Overleaf: перейди на pdfLaTeX (Menu → Compiler).
Локально: `tlmgr install fontawesome5` (TeX Live) або через MiKTeX Console.

### "Undefined control sequence \faGithub"
Стара версія fontawesome. Заміни на `fontawesome` (без `5`) і всі `\faMapMarker*` → `\faMapMarker`.

### PDF виглядає поламано / зміщення
Перевір `\addtolength{...}{...}` margins. Інколи Overleaf інтерпретує по-іншому. Зменши `-0.6in` до `-0.4in`.

### Кириличні символи (наприклад, у "ТВ-43") не відображаються
В preamble додай:
```latex
\usepackage[utf8]{inputenc}
\usepackage[T2A]{fontenc}
\usepackage[ukrainian,english]{babel}
```
**Або** використовуй XeLaTeX замість pdfLaTeX (Overleaf: Menu → Compiler → XeLaTeX) — він підтримує UTF-8 і будь-які мови нативно.
