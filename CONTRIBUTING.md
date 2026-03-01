# Разработка

Состав пакета расширений см. в [README](README.md).

## Предварительные требования

- Node.js 20+
- npm 9+
- VS Code 1.60.0+

## Подготовка окружения

```bash
# Клонируйте репозиторий
git clone https://github.com/yellow-hammer/vscode-1c-platform-extension-pack.git
cd vscode-1c-platform-extension-pack

# Установите зависимости
npm install
```

## Сборка расширения

```bash
# Упаковать расширение в VSIX файл
npm run package

# Или используйте vsce напрямую
npx vsce package
```

## Публикация

### Через GitHub Actions (рекомендуется)

1. **Убедитесь, что установлены секреты в GitHub**:
   - `VSCE_PAT` - Personal Access Token для VS Code Marketplace
   - `OVSX_TOKEN` - Access Token для Open VSX Registry

2. **Создайте релиз** одним из способов:

   **Способ 1: Через тег (автоматический)?**

   ```bash
   git tag v1.0.0
   git push origin v1.0.0
   ```

   **Способ 2: Через GitHub Actions UI (workflow_dispatch)**
   - Перейдите на вкладку "Actions" в репозитории
   - Выберите желаемый workflow
   - Нажмите на кнопку "Run workflow"
   - Заполните параметры версии и опции публикации

3. **GitHub Actions автоматически**:
   - Соберёт расширение
   - Создаст GitHub Release
   - Опубликует в VS Code Marketplace
   - Опубликует в Open VSX Registry

### Параметры Workflow

При использовании `workflow_dispatch` доступны следующие параметры:

- **version** (обязательный): Версия релиза (например, v1.0.0, v1.0.0-alpha.1)
- **skip_publish**: Пропустить публикацию в маркетплейсы (по умолчанию: false)
- **draft**: Создать draft релиз (по умолчанию: false)
- **prerelease**: Отметить как prerelease (по умолчанию: false)

## Нужные секреты на GitHub

### 1. VS Code Marketplace Token (VSCE_PAT)

1. Перейдите на [https://marketplace.visualstudio.com/manage/publishers/](https://marketplace.visualstudio.com/manage/publishers/)
2. Выберите издателя "yellow-hammer"
3. Нажмите на трёх точки меню
4. Выберите "Personal Access Tokens"
5. Создайте новый токен с правами:
   - `Publish`
   - `Manage`
6. Скопируйте токен
7. Добавьте токен в Settings → Secrets and variables → Actions (назовите его `VSCE_PAT`)

### 2. Open VSX Registry Token (OVSX_TOKEN)

1. Перейдите на [https://open-vsx.org/user/namespaces](https://open-vsx.org/user/namespaces)
2. Авторизуйтесь аккаунтом издателя
3. Перейдите в управление профилем
4. Создайте Access Token
5. Скопируйте токен
6. Добавьте токен в Settings → Secrets and variables → Actions (назовите его `OVSX_TOKEN`)

## Структура проекта

```txt
.
├── .github/
│   └── workflows/
│       └── release.yml       # GitHub Actions workflow для публикации
├── .vscode/
│   └── extensions.json       # Рекомендуемые расширения
├── CHANGELOG.md              # История изменений
├── LICENSE                   # MIT лицензия
├── package.json              # Конфигурация расширения
└── README.md                 # Документация
```

## Версионирование

Проект использует [Semantic Versioning](https://semver.org/):

- **MAJOR**: Несовместимые изменения (например, добавление/удаление расширений)
- **MINOR**: Добавление новых расширений с обратной совместимостью
- **PATCH**: Обновления документации, метаданные

## Соглашение о коммитах

Мы используем [Conventional Commits](https://www.conventionalcommits.org/ru/v1.0.0/). Используйте понятные сообщения коммитов, например: `docs(readme): обновить список расширений` или `fix(package): исправить состав extensionPack`.

## Лицензия

Внося вклад в проект, вы соглашаетесь с тем, что ваш вклад будет лицензирован под [MIT License](LICENSE).
