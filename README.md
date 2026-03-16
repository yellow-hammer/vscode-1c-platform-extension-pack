# Пакет расширений для платформы 1С

[![OpenYellow](https://openyellow.openintegrations.dev/data/badges/1155465357.png)](https://openyellow.org/grid?filter=top&repo=1155465357)
[![telegram chat](resources/badges/telegram-chat.png)](https://t.me/wonder_yellow)
[![Ask DeepWiki](resources/badges/deepwiki-badge.png)](https://deepwiki.com/yellow-hammer/vscode-1c-platform-extension-pack)

Набор расширений VS Code для разработки на платформе 1С

## Включённые расширения

Пакет содержит следующие расширения (в порядке приоритета):

### 1. [1C: Platform tools](https://github.com/yellow-hammer/vscode-1c-platform-tools)

- **Издатель:** yellow-hammer
- **ID расширения:** `yellow-hammer.1c-platform-tools`
- **Marketplace:** [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=yellow-hammer.1c-platform-tools)
- **Open VSX:** [Open VSX Registry](https://open-vsx.org/extension/yellow-hammer/1c-platform-tools)

Инструменты разработки для экосистемы 1С: дерево команд, панель проектов, запуск конфигуратора и отладка, список дел, инициализация структуры проекта и работа с vrunner.

### 2. [1C: Platform Tools MCP](https://github.com/yellow-hammer/mcp-1c-platform-tools)

- **Издатель:** yellow-hammer
- **ID расширения:** `yellow-hammer.mcp-1c-platform-tools`
- **Marketplace:** [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=yellow-hammer.mcp-1c-platform-tools)
- **Open VSX:** [Open VSX Registry](https://open-vsx.org/extension/yellow-hammer/mcp-1c-platform-tools)

MCP-сервер для запуска команд 1C Platform Tools через агентов Cursor/VS Code. Требует установленного расширения 1C Platform Tools и включённого IPC.

### 3. [Language 1C (BSL)](https://github.com/1c-syntax/vsc-language-1c-bsl)

- **Издатель:** 1c-syntax
- **ID расширения:** `1c-syntax.language-1c-bsl`
- **Marketplace:** [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=1c-syntax.language-1c-bsl)
- **Open VSX:** [Open VSX Registry](https://open-vsx.org/extension/1c-syntax/language-1c-bsl)

Подсветка синтаксиса, автодополнение и поддержка языка 1С BSL (BSL Language Server): диагностика, навигация, форматирование.

## Установка

1. Установите пакет расширений из [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=yellow-hammer.1c-platform-extension-pack) или [Open VSX Registry](https://open-vsx.org/extension/yellow-hammer/1c-platform-extension-pack).
2. Все включённые расширения будут установлены автоматически.

## Требования

- Visual Studio Code версии 1.60.0 или выше

## Возможности

- **1C Platform Tools:** панель проектов 1С, дерево инструментов и избранное, команды запуска конфигуратора и отладки, список дел (TODO/FIXME), инициализация структуры проекта, интеграция с vrunner и onec-debug-adapter.
- **MCP:** вызов команд 1C Platform Tools из агентов (Cursor/VS Code) по протоколу MCP при включённом IPC.
- **Язык 1С (BSL):** подсветка синтаксиса, BSL Language Server (диагностика, переход к определению, форматирование, автодополнение).

## Участие в развитии

Для сообщений об ошибках или предложений по этому пакету расширений:

- [Репозиторий пакета расширений](https://github.com/yellow-hammer/vscode-1c-platform-extension-pack)

Для проблем с отдельными расширениями:

- [1C Platform Tools](https://github.com/yellow-hammer/vscode-1c-platform-tools/issues)
- [1C Platform Tools MCP](https://github.com/yellow-hammer/mcp-1c-platform-tools/issues)
- [Language 1C (BSL)](https://github.com/1c-syntax/vsc-language-1c-bsl/issues)

## Лицензия

MIT License. Подробности см. в файле [LICENSE](LICENSE).
