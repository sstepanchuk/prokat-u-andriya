# Прокат у Андрія

Статичний сайт для прокату гірськолижного спорядження на Красії.

## Структура

```
├── index.html      # Головна сторінка (SEO-оптимізована)
├── 404.html        # Сторінка помилки
├── CNAME           # Кастомний домен
├── robots.txt      # Інструкції для пошукових роботів
├── sitemap.xml     # Карта сайту
└── .github/workflows/deploy.yml  # Auto-deploy
```

## Локальна розробка

```bash
npx serve . -p 3000
```

## Деплой на GitHub Pages

Push в `main` → автоматичний деплой через GitHub Actions.

### Налаштування

1. **Settings** → **Pages** → Source: **GitHub Actions**

### 2. Підключення кастомного домену

1. У вашого реєстратора домену додайте DNS записи:
   - **A записи** (для apex домену `prokat-krasiya.com`):
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - **CNAME запис** (для `www`):
     ```
     www -> <username>.github.io
     ```

2. В GitHub Settings → Pages введіть ваш домен: `prokat-krasiya.com`
3. Увімкніть **Enforce HTTPS**

### 3. Перевірка

- Зачекайте 5-10 хвилин на пропагацію DNS
- Відкрийте `https://prokat-krasiya.com`

## SEO оптимізації

- ✅ Семантична HTML5 розмітка
- ✅ Schema.org JSON-LD (LocalBusiness)
- ✅ Open Graph та Twitter Cards
- ✅ Мета-теги для геолокації
- ✅ Канонічний URL
- ✅ robots.txt та sitemap.xml
- ✅ Оптимізовані alt-теги для зображень
- ✅ Preload критичних ресурсів
- ✅ Lazy loading для зображень

## Розмір

- **index.html**: ~25KB (все в одному файлі)
- **Без JavaScript фреймворків**
- **Без зовнішніх CSS файлів**
- Мінімальний vanilla JS для інтерактивності (~500 bytes)

## Оновлення контенту

Змініть домен у файлі `CNAME` на ваш власний перед деплоєм.

Оновіть наступні дані в `index.html`:
- Телефон: `+380666499206`
- Адреса
- URL в canonical та Open Graph
- Координати в Schema.org
