# 📖 Sharada Messenger API — GitHub Pages Documentation

Данная папка содержит полную спецификацию **OpenAPI 3.1.0** и интерактивный портал документации мессенджера **Sharada v1.4.3**, готовый к публикации на **GitHub Pages**.

---

## 📂 Структура файлов

- `index.html` — Интерактивный портал документации с поддержкой:
  - **Swagger UI** (интерактивный запуск запросов, тестирование, авторизация)
  - **Redoc** (структурированная документация в 3 колонки со схемами моделей)
  - **WebSocket Protocol Guide** (полное описание событий, WebRTC signaling звонков, whitelist)
  - **Security Architecture** (пароли Argon2id+Bcrypt v2, жизненный цикл 2FA, карантин версий `<= 1.4.2`)
- `openapi.yaml` — Полная спецификация API в формате YAML (OpenAPI 3.1.0)
- `openapi.json` — Полная спецификация API в формате JSON (OpenAPI 3.1.0)
- `.nojekyll` — Отключение Jekyll для корректной раздачи статических файлов на GitHub Pages

---

## 🚀 Как включить GitHub Pages в репозитории

### Вариант 1 (Простой — через ветку `main` и папку `/docs`):
1. Откройте ваш репозиторий на GitHub.
2. Перейдите в **Settings** (Настройки) $\to$ **Pages** (в боковом меню).
3. В блоке **Build and deployment**:
   - **Source**: выберите `Deploy from a branch`.
   - **Branch**: выберите `main` (или `master`) и папку `/docs`.
4. Нажмите **Save**.
5. Через 30 секунд документация будет доступна по адресу:
   `https://<ваш_юзернейм>.github.io/<имя_репозитория>/`

### Вариант 2 (Через GitHub Actions):
1. В настройках репозитория **Settings** $\to$ **Pages**.
2. В **Source** выберите **GitHub Actions**.
3. При каждом коммите в ветку `main` файл `.github/workflows/deploy-pages.yml` будет автоматически разворачивать свежую версию документации на GitHub Pages.

---

## 🧪 Локальный просмотр

Вы можете просмотреть документацию локально:
```bash
# С помощью любого локального веб-сервера, например:
npx serve docs
# или
python -m http.server 3000 --directory docs
```
После запуска перейдите по адресу [http://localhost:3000](http://localhost:3000).
