<div align="center">

# AndroidDemo - телефон «Волна»

**Телефон «Волна» - Android-телефон в духе One UI 7, который целиком работает в браузере: экран блокировки, домашний экран, шторка уведомлений с быстрыми настройками, недавние приложения и работающие программы. Без сервера, без интернета, без картинок и шрифтов из настоящей системы.**

[**▶ Открыть онлайн →**](https://alexalesha.github.io/AndroidDemo/) &nbsp;·&nbsp; [English version of this file](README.md)

[![Status](https://img.shields.io/badge/status-stable-brightgreen)](#) [![CI](https://github.com/ALEXalesha/AndroidDemo/actions/workflows/ci.yml/badge.svg)](https://github.com/ALEXalesha/AndroidDemo/actions/workflows/ci.yml) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE) [![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML) [![Website](https://img.shields.io/badge/Website-open-0A84FF?logo=googlechrome&logoColor=white)](https://alexalesha.github.io/AndroidDemo/) [![Built with Claude Code](https://img.shields.io/badge/Built_with-Claude_Code-D97757?logo=claude&logoColor=white)](https://claude.com/claude-code)

Код, тесты и документация этого проекта написаны Claude (Anthropic) в Claude Code. Идеи, проверка и решения - Алексей.

</div>

> Фан-концепт интерфейса. Не связан с Samsung и Google и не одобрен ими. One UI - товарный знак Samsung Electronics; Android - товарный знак Google LLC.

![Экран блокировки](docs/screens/lock.png)

![Домашний экран](docs/screens/home.png)

![Быстрые настройки](docs/screens/quick-settings.png)

## Что умеет

- Шторка с быстрыми настройками и яркостью, всплывающие уведомления открывают свою программу, недавние приложения (смахнуть вверх и задержать или долгое нажатие на полоску) с кнопкой «Закрыть все».
- Программы: Телефон (экран звонка с таймером и журнал), Сообщения, Контакты, Почта, Интернет (встроенные страницы), Галерея (снимки камеры и картинки из файлов), Камера, Калькулятор, Часы (мировые часы, будильники, таймер, секундомер), Календарь, Заметки, Музыка (синтезированные мелодии), Погода, Настройки и «Мои файлы» (IndexedDB).
- Сохраняются настройки, обои, заметки, будильники, события, переписка, фото, журнал звонков и прочитанные письма; программы в фоне стоят на паузе.
- **Игры:** десять игр сборника [Hub](https://github.com/ALEXalesha/ALEXalesha.github.io) открываются
  в окне: «Кубический мир», «Блоксити», «Операция: Периметр», Horizon Drift, «Дино-бег», «Прыг-скок»,
  «Огненные джунгли», «Космический стрелок», «Блоки» и «Судоку». Каждая - свой репозиторий: на
  GitHub Pages окно загружает `../../<репозиторий>/` того же сайта (например,
  [AlexMine](https://alexalesha.github.io/AlexMine/)). У себя положите клоны игр рядом с этим
  репозиторием. Игра в свёрнутом или неактивном окне стоит на паузе (протокол - в
  `_os-shared/README.md`).


Телефон лежит в `oneui7/`, собирается из `oneui7/src/` командой `node oneui7/src/build.js`. `index.html` в корне просто открывает его.


## Запуск у себя

Откройте `index.html` или `oneui7/index.html` в Chrome или Edge.

## Проверки

Законы Playwright в `tests/` открывают страницу по файловому адресу в безголовом Chromium, по
одной за раз:

```
npm install
npx playwright install chromium
npm test
```

Проверки окон игр идут, только если репозитории игр лежат рядом с этим, иначе они пропускаются.
Захват мыши в проверках всегда поддельный. Кадры выше сняты в безголовом браузере скриптом кадров сборника Hub.

## История

Телефон сделан в сборнике [Hub](https://github.com/ALEXalesha/ALEXalesha.github.io) (папки `web/oneui7` и `web/_os-shared`), там он же открывается из Хаба. Здесь он лежит с историей коммитов, начиная после первого «сырого» импорта (в нём ещё были чужие бренды); стартовая страница, таблица отдельно опубликованных игр и проверки добавлены для этой публикации.

## Лицензия

MIT, см. [LICENSE](LICENSE).
