# Terminal

Каноническая документация находится в `docs/`.

Создание и редактирование через Docs Portal обрабатывает `.github/workflows/document-request.yml`: GitHub Issue подтверждается владельцем, встроенный GITHUB_TOKEN создаёт отдельную ветку, commit и Pull Request в main.

После merge изменения документации workflow уведомляет docs-portal. Без отдельного `DOCS_PORTAL_TOKEN` используется автоматическая проверка SHA порталом раз в 15 минут. Изменения только `src/**` не запускают notify workflow.

Опционально для немедленного dispatch: secret `DOCS_PORTAL_TOKEN` с Contents: write только для docs-portal и variable `DOCS_PORTAL_REPOSITORY=rossosss/docs-portal`.
