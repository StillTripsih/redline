# RedLine — состояние проекта

## 2026-11-22 · версия 3.3

- Источник: StillTripsih/redline, main 10efa63f5f5734bfbcbb48f4253d5eb8817e6088. Публикация GitHub Pages по прежнему адресу /redline/. Основной финансовый трекер не изменён.
- До начала/перерыва/конца отображаются часы:минуты без секунд. Убраны «Следующий рабочий день», «День завершён», нижний поясняющий текст и заголовок быстрых таймеров.
- Один круглый активный таймер; отдельные кнопки отмены и завершения. «Отойти» считает прошедшее время до возвращения, которое сохраняется в историю.
- Шесть видов перерыва, «Подумать» первым; общий таймер паузы, сигналы начала/завершения, нового интервала, начала работы, очередной паузы, каждых пяти минут, получаса для позы и часа для движения. Web Audio включается после взаимодействия; телефонный фоновый звук не гарантируется.
- Рабочие часы редактируются прокручиваемыми колёсами часов и минут. Кнопки основных действий и быстрых таймеров круглые, одного нейтрального стиля.
- Сохраняются redline_v3, история, активные таймеры, пользовательские поля, адрес и идентичность установленного приложения. Первая запись создаёт отдельную копию прежнего состояния. Повреждённое исходное хранилище не перезаписывается.
- Проверено: 15 автоматических тестов; синтаксис модулей. Реальное отображение/жесты/звуки на телефоне не проверены; браузерное тестирование не запускалось из-за существующего ограничения пользователя.

Публикация: дождаться сборки GitHub Pages и сверить файлы с локальной проверенной версией.

Публикация подтверждена: ef2c0b4496619642b547fabd8d0ae4dad49f9626; GitHub Pages run 45005793686 завершён успешно. index.html, style.css, app.mjs и core.mjs доступны HTTP 200 и совпадают с проверенными локальными файлами. Интерфейс и звук на реальном телефоне не проверены.

## 2026-11-22 — версия 3.4

- Sound icon opens a dedicated settings page: volume, voice, per-event enables and previews. Gear opens colours, break intervals, reminders and editable/reorderable custom break types. Third icon opens statistics. Brand/version and refresh moved into settings.
- Home work hours/date use the accent colour. Dial has twelve hour labels, absolute-time current/target markers and remaining-work arc, plus an independent running-timer ring. Animation uses timestamps; overdue breaks show increasing +HH:MM instead of a frozen 00:00. Before/after work the next start remains HH:MM.
- Statistics show exact recorded pause durations, preserve empty days, split midnight-crossing events, support date ranges, drag/pinch/keyboard pan/zoom, day selection and a complete chronological event list. Quick/cancelled events are now logged; previous records are retained.
- Preserves origin and redline_v3. Adds a separate before_34 snapshot without removing earlier backups. No financial-app source/data touched.
- Checked: 23 automated tests and JavaScript syntax. Actual mobile UI, gestures and foreground/background sound remain unverified due to the existing browser-testing restriction.

Версия 3.4 опубликована: 7f5906755965c1eab8190b00ec20b981b7ed0b9a; Pages run 45007147536 завершён успешно. HTML, CSS и все 5 модулей доступны HTTP 200 и совпадают с проверенными файлами. Реальное взаимодействие/звук/жесты на телефоне не проверены.

## 2026-11-22 — версия 3.5

- Два полудневных циферблата с рабочими секторами и динамическими значками воды, разминки и глаз. Прогноз сдвигается от действительного завершения пауз, в том числе поздних/долгих. Поддержано ночное расписание. Настройки типов/интервалов/длительности сохраняются отдельно от истории.
- Звук перемещён в настройки; настройки и статистика зеркально в верхнем ряду; дата и часы на одной линии. Звуковой движок повторно разблокируется после жестов, сигнал завершения не теряется при отсутствии готового контекста, очередь подтверждается после планирования звука.
- Личный API для Gemini, OpenAI или совместимого endpoint. Тест подключения до сохранения, отдельное хранение ключа. AI получает только сводку и явно введённые цели по нажатию. Проверяемые предложения настроек применяются отдельной кнопкой; неизвестные поля/изменения истории запрещены. Нет обещания поддержки любого протокола или CORS.
- Проверено: 31 тест, синтаксис модулей. Тесты AI/звука имитируют API и AudioContext; реальные ключи не использовались. Телефон, слышимость, жесты и фон не проверены под существующим запретом браузерных проверок.
- Ключ данных redline_v3 и адрес неизменны; дополнительная копия before_35, предыдущие копии сохранены. Другие проекты не менялись.

RedLine 3.5 размещён: 87e6eb47d842372a890263231f2824ef32bbce09; Pages run 45009247093 успешен. HTML, CSS и все 9 модулей HTTP 200 и совпадают с проверенными локальными файлами. Реальный провайдер с личным ключом, браузерный интерфейс и слышимость на телефоне не проверялись.

## 2026-11-22 — версия 3.6

- Replaced two side-by-side faces with one full-width face and two concentric rings. Current half sits outside with typed icons, inactive half is dimmed inside with dots. Swaps at noon/midnight; work arcs remain visible.
- Timer/countdown is centred in the face for all modes. Secondary live seconds and timestamp-derived values recover after tab suspension. Current-position marker refreshes at 250 ms; active pause, exercise and elapsed-away modes have distinct icon/colour/background/progress. Disabled extra start actions are hidden during an active timer.
- Settings are collapsed categories with backgrounds. Identity/update moved to the top. API form reduced to key + Google key link + verification; existing working connections are preserved. Advice/commands remain in an expandable section.
- Origin, storage key and history remain unchanged; before_36 snapshot added. Checked: 33 tests and module syntax; real phone UI/audio/API remain unverified under the existing browser-testing restriction.

Публикация 3.6 подтверждена: commit f1100ebe66b1dca58ea96f5e9c9f373d28713e5c, Pages run 45013246343 — success. Все 11 публичных файлов HTTP 200 и совпадают с локальными по SHA-256. 33 теста пройдены. Интерфейс и звук на настоящем телефоне не проверялись.

## 3.7
Главный экран закреплён в viewport, настройки прокручиваются только вертикально без полос. Иконки пауз вынесены на внешнюю невидимую орбиту; подпись половин удалена, легенда — три иконки. Прогресс паузы круговой, красный фон. Добавлен WAV-аудиоплеер с Web Audio fallback и явная диагностика, без утверждения о фактической слышимости. Хранилища сохранены; before_37. Телефон не проверялся.
