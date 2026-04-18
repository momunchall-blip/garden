# 🌸 Han's Garden & Ria Cafe — Restaurant Website

<div align="center">

![Han's Garden](https://img.shields.io/badge/Han's%20Garden-Ria%20Cafe-f2c4ce?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHRleHQgeT0iMjAiIGZvbnQtc2l6ZT0iMjAiPvCfjonPgDwvdGV4dD48L3N2Zz4=)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Ready-brightgreen?style=for-the-badge&logo=github)

**Готовый сайт для корейского ресторана — без фреймворков, без сборщиков, чистый HTML/CSS/JS**

[🌐 Demo](https://your-username.github.io/hans-garden) · [🐛 Issues](../../issues) · [⭐ Star](../../stargazers)

</div>

---

## ✨ Возможности

| Раздел | Описание |
|--------|----------|
| 🏠 **Главная** | Hero с анимированными лепестками сакуры, логотип, соцсети |
| 🍜 **Основное меню** | Карточки блюд, фильтр по категориям, поиск, острота, теги |
| 🥂 **Барное меню** | Отдельный раздел с коктейлями, винами, корейскими напитками |
| 🛒 **Корзина** | Добавление блюд, счётчик, модалка «Показать официанту» |
| 🎉 **Банкет** | Форма бронирования → отправка заявки прямо в WhatsApp |
| ⭐ **Отзывы** | 5 звёзд, быстрые теги по оценке, список отзывов |
| 📍 **О нас** | Адрес, часы работы, контакты, ссылка на карту |
| 🔐 **Админ-панель** | Управление меню, фото блюд, заявки, отзывы |

### 🛠 Технически
- **Без зависимостей** — чистый HTML + CSS + Vanilla JS
- **LocalStorage** — все изменения в меню сохраняются
- **Адаптивный** — мобильная навигация снизу, корректная вёрстка
- **3 языка** — RU / EN / KG переключение на лету
- **WhatsApp интеграция** — заявки на банкет идут прямо в мессенджер
- **Загрузка фото** — base64 прямо в браузере, без бэкенда

---

## 🚀 Деплой на GitHub Pages (бесплатный хостинг)

### Шаг 1 — Форкни репозиторий

Нажми кнопку **Fork** в правом верхнем углу страницы.

### Шаг 2 — Настрой под себя

Открой эти файлы и замени данные:

**`index.html`** — контакты и соцсети:
```html
<!-- Строка ~28: ссылка на Instagram -->
<a href="https://instagram.com/ТВОЙ_АККАУНТ" ...>

<!-- Строка ~29: номер WhatsApp (только цифры, без +) -->
<a href="https://wa.me/996XXXXXXXXX" ...>
```

**`js/app.js`** — строка 1:
```js
const WHATSAPP_NUMBER = '996XXXXXXXXX'; // твой номер без +
```

**`js/app.js`** — пароль админ-панели (поищи `hans2025`):
```js
if(document.getElementById('adminPass').value === 'ТВОЙ_ПАРОЛЬ'){
```

**Название ресторана** — в `index.html` найди и замени `Han's Garden & Ria Cafe`.

### Шаг 3 — Включи GitHub Pages

1. Перейди в **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / **(root)**
4. Нажми **Save**
5. Через 1–2 минуты сайт появится на `https://USERNAME.github.io/REPO-NAME`

### Шаг 4 — Добавь логотип (опционально)

Положи файл `logo.png` в папку `img/` — он автоматически появится в шапке и на главной.

---

## 🖥 Запуск локально

### VS Code + Live Server (рекомендуется)
```bash
# 1. Клонируй репозиторий
git clone https://github.com/your-username/hans-garden.git
cd hans-garden

# 2. Открой в VS Code
code .

# 3. Установи расширение Live Server
# 4. Правой кнопкой на index.html → "Open with Live Server"
```

### Python
```bash
cd hans-garden
python -m http.server 8080
# Открой http://localhost:8080
```

### Node.js
```bash
cd hans-garden
npx serve .
```

---

## 🔐 Вход в админ-панель

Admin-панель **скрыта** из навигации. Два способа попасть:

1. **URL**: добавь `#admin-secret-2025` в конец адреса сайта
   ```
   https://your-site.github.io/hans-garden/#admin-secret-2025
   ```
2. **Футер**: внизу страницы есть еле видимый символ `⚙` — кликни по нему

**Пароль по умолчанию:** `hans2025` (смени в `js/app.js`)

### Возможности админ-панели

- ➕ Добавлять новые блюда и напитки
- ✏️ Редактировать название, цену, описание, острота, теги
- 📷 Загружать фото блюд прямо из браузера
- 🗑 Удалять позиции из меню
- 🥂 Управлять барным меню отдельно
- 🎉 Просматривать заявки на банкет, подтверждать их
- ⭐ Просматривать и удалять отзывы

---

## 📁 Структура проекта

```
hans-garden/
├── index.html          ← вся HTML-разметка
├── css/
│   └── style.css       ← все стили (переменные, компоненты, медиа)
├── js/
│   └── app.js          ← вся логика (меню, корзина, отзывы, админ)
├── img/
│   └── logo.png        ← логотип (добавь сам)
└── README.md
```

---

## ⚙️ Кастомизация

### Меню по умолчанию
Дефолтные блюда находятся в `js/app.js` в массиве `defaultDishes`. Если localStorage пустой — загружаются они.

### Цвета
Все цвета через CSS-переменные в `css/style.css`:
```css
:root {
  --sakura: #f2c4ce;      /* основной розовый */
  --deep-rose: #c4687a;   /* акцентный цвет кнопок */
  --bark: #5c3d3d;        /* тёмно-коричневый текст */
  --cream: #fdf6f0;       /* фон страницы */
}
```

### График работы
Найди в `index.html` раздел `page-about` и в `footer` — замени часы на свои.

### Банкет → WhatsApp
Заявки отправляются на номер из переменной `WHATSAPP_NUMBER` в `js/app.js`.

---

## 📱 Скриншоты

> Положи скриншоты в папку `img/screenshots/` и раскомментируй строки ниже

<!--
| Главная | Меню | Корзина |
|---------|------|---------|
| ![home](img/screenshots/home.png) | ![menu](img/screenshots/menu.png) | ![cart](img/screenshots/cart.png) |

| Отзывы | Банкет | Админ |
|--------|--------|-------|
| ![reviews](img/screenshots/reviews.png) | ![banquet](img/screenshots/banquet.png) | ![admin](img/screenshots/admin.png) |
-->

---

## 🤝 Использование

Можешь использовать этот шаблон для любого ресторана или кафе. Просто замени:
- Название заведения
- Контакты и соцсети
- Меню и цены
- Логотип
- Цвета (при желании)

---

## 📄 Лицензия

MIT — делай что хочешь, просто не удаляй этот README 🌸

---

<div align="center">
Сделано с ❤️ для Han's Garden & Ria Cafe · Бишкек, Кыргызстан
</div>
