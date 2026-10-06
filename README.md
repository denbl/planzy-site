# planzy.ai

Сайт Planzy: одна страница и две юридические (`/privacy`, `/terms`). Чистый HTML без сборки, картинки и шрифты лежат в `assets/`.

## Как выкладывается

- Netlify, проект `planzy-ai` (команда AfterDot). Каждый пуш в `main` выкладывается сам.
- Главный адрес `planzy.ai`, `www.planzy.ai` перенаправляется на него.
- `help.planzy.ai` — бывший справочный центр Intercom. Старые ссылки на статьи из приложения перенаправляются на `/privacy` и `/terms` (`netlify.toml`).
- Плашка «Powered by Netlify» выключена в настройках проекта.

## DNS (GoDaddy)

- `@` A → `75.2.60.5`
- `www` CNAME → `planzy-ai.netlify.app`
- `help` CNAME → `planzy-ai.netlify.app`
- MX, TXT (SPF, подтверждения Google), `s1/s2._domainkey` (SendGrid) и `_…acm-validations.aws` не трогать: от них зависят почта и сертификат API.

## Что где

- Стена телефонов в первом экране: блок `.wall-cols` в `index.html`. Пять колонок, по три экрана в каждой; один и тот же экран не ставить в соседние колонки.
- Приложение только под iOS: все кнопки ведут на `https://apps.apple.com/app/id6499276047`.
- Тексты `/privacy` и `/terms` написаны по коду приложения (октябрь 2026). Издатель — Artem Ptashnik, контакт help@planzy.ai.
