# Commit Conventions

В этом проекте мы используем **Conventional Commits** для всех коммитов. Это помогает делать историю коммитов понятной, структурированной и пригодной для автоматизации.

Официальная документация:  
- [Conventional Commits (English)](https://www.conventionalcommits.org/en/v1.0.0/)  
- [Conventional Commits (Русский)](https://www.conventionalcommits.org/ru/v1.0.0/)

---

## Основные типы коммитов

| Тип       | Описание                                                                                  | Пример сообщения                                  |
|-----------|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| **feat**  | Добавление нового функционала или компонента                                              | `feat: add search button`                        |
| **fix**   | Исправление ошибки                                                                        | `fix: correct header layout on mobile`           |
| **chore** | Настройка проекта, сборщик, зависимости, конфигурации                                     | `chore: setup Parcel and SCSS`                   |
| **docs**  | Изменения в документации                                                                  | `docs: add project README`                        |
| **style** | Форматирование кода, отступы, пробелы, не влияющее на функциональность                    | `style: format main.scss`                        |
| **refactor** | Рефакторинг кода без изменения функциональности                                        | `refactor: split button block into separate folder` |
| **test**  | Добавление или исправление тестов                                                         | `test: add unit tests for datepicker`            |
| **perf**  | Изменения, направленные на улучшение производительности                                   | `perf: optimize image loading`                   |
| **ci**    | Изменения, связанные с интеграцией и CI/CD (например GitHub Actions, сборка)              | `ci: update workflow for deployment`             |
| **build** | Изменения, влияющие на систему сборки или зависимости                                     | `build: update Parcel version`                   |
| **revert** | Отмена предыдущего коммита                                                               | `revert: feat: add old feature`                  |

---

## Правила

- Все сообщения **на английском**.
- Сообщение коммита должно быть написано строчными буквами.  
- Используется **императивная форма**: `add`, `fix`, `remove`, `update`.  
- Один коммит = одно логическое изменение.  
- Опционально после типа можно указать область изменения, например: `feat(button): add primary style`.  

## Scope (область)

Scope - это часть проекта (обычно компонент), к которой относится изменение.

Примеры:
- feat(button): add primary button styles
- fix(header): fix mobile layout alignment
- refactor(dropdown): simplify open/close logic