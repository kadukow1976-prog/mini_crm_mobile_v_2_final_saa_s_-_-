# MiniCRM Mobile (PWA)

Мини‑CRM в стиле MIUI для мастерской: список клиентов, поиск, карточка клиента, список «ресурсов» (ссылки). Данные хранятся локально (localStorage). Приложение можно установить на Android как PWA и запускать офлайн.

## Структура
```
ugraremkomp-pwa-v1/
  index.html
  manifest.webmanifest
  service-worker.js
  icons/
    icon-192.png
    icon-512.png
```

## Быстрый старт (локально)
Откройте `index.html` в Chrome. Для установки как PWA используйте простой http-сервер (например, `python -m http.server 8080`) и зайдите на `http://localhost:8080/`.

## Деплой на GitHub Pages
1. Создайте репозиторий, добавьте эти файлы в корень.
2. Включите GitHub Pages (Settings → Pages → Deploy from branch → `main` / `/`).
3. Откройте страницу репозитория — появится публичный URL.
4. Откройте на Android в Chrome → меню → «Добавить на главный экран».

## Деплой на Netlify
Перетащите папку в Netlify Drop или подключите репозиторий. Бандлеры не требуются.

## Офлайн
`service-worker.js` кэширует «оболочку» приложения, так что после первого посещения приложение открывается без интернета.

## Демо‑данные
Кнопка «＋ Демо» — заполнит список клиентов и ресурсов примерами.

## Данные
- Клиенты: `localStorage["mini_crm_clients_v1"]`
- Ресурсы: `localStorage["mini_crm_resources_v1"]`
