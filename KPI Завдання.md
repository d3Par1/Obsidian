---

kanban-plugin: board

---

## 🔴 Прострочено


## 🟠 Цей тиждень


## 🟡 Наступні 2 тижні

- [ ] Система управління розробкою як інструмент управління якістю @{2026-09-21}
  [[Tasks/Система управління розробкою як інструмент управління якістю]]

## ⚪ Пізніше


## 📥 Без дедлайну


## ✅ Виконано


**Complete**

%% kanban:settings
```
{
  "kanban-plugin": "board",
  "date-trigger": "@",
  "time-trigger": "@@",
  "date-format": "YYYY-MM-DD",
  "date-display-format": "DD MMM",
  "time-format": "HH:mm",
  "show-relative-date": true,
  "move-dates": true,
  "move-tags": true,
  "link-date-to-daily-note": false,
  "show-checkboxes": true,
  "show-add-list": true,
  "archive-with-date": true,
  "lane-width": 320,
  "date-colors": [
    {
      "isToday": false,
      "distance": 1,
      "unit": "days",
      "direction": "before",
      "color": "#ffffff",
      "backgroundColor": "#c0392b"
    },
    {
      "isToday": true,
      "color": "#ffffff",
      "backgroundColor": "#d35400"
    },
    {
      "isToday": false,
      "distance": 7,
      "unit": "days",
      "direction": "after",
      "color": "#ffffff",
      "backgroundColor": "#e67e22"
    },
    {
      "isToday": false,
      "distance": 14,
      "unit": "days",
      "direction": "after",
      "color": "#ffffff",
      "backgroundColor": "#b7950b"
    }
  ],
  "tag-colors": [
    {
      "tagKey": "#лаб",
      "color": "#ffffff",
      "backgroundColor": "#2980b9"
    },
    {
      "tagKey": "#практика",
      "color": "#ffffff",
      "backgroundColor": "#27ae60"
    },
    {
      "tagKey": "#курсова",
      "color": "#ffffff",
      "backgroundColor": "#8e44ad"
    },
    {
      "tagKey": "#тест",
      "color": "#ffffff",
      "backgroundColor": "#16a085"
    },
    {
      "tagKey": "#залік",
      "color": "#ffffff",
      "backgroundColor": "#c0392b"
    }
  ]
}
```
%%