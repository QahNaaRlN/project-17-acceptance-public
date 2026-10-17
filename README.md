# CMS GitHub acceptance fixture

Synthetic public fixture for CMS GitHub PR/CI acceptance.
This repository contains test data only, without application code or credentials.

Workflow `Acceptance` запускает проверку `Acceptance check` для pull request и
push в main. Содержимое `acceptance-state.txt` управляет результатом:
`pass` — успех, любое другое значение — ошибка.

После отдельного разрешения на внешние действия можно создать тестовый PR,
изменять этот файл между pass/fail, наблюдать каждый новый SHA из CMS, вернуть
pass, слить PR и наблюдать отдельный CI итогового коммита. Для наблюдения pending
нужно привязать PR до начала очередного запуска и обновить факты, пока проверка
выполняется. Длительные искусственные задержки в workflow не добавлены.

Для нового репозитория нужно отдельно подтвердить repository ID, базовую ветку,
точное имя проверки, SHA, на котором GitHub публикует Check Run, и app ID издателя.

This branch is used to observe PR state and exact commit checks from CMS.
