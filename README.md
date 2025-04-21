# Автоподтверждение q.midpass.ru за 5 секунд (Грузия)

Для тех, кому лень раз в 24 часа заходить на сайт и подтверждать свою заявку на загранпаспорт в консульстве России в Тбилиси, уже есть много автоматических инструментов.

Мой скрипт написан на JS и puppeteer и хорош тем, что вам нужно посмотреть всего один файл, чтобы удостовериться, что он не наносит никакого вреда. Вообще весь код в одном маленьком файле. simply run index.ts.

> [!IMPORTANT]
> Я ищу работу! Если вы заинтересованы в моем найме, посетите [cv.hloth.dev](https://cv.hloth.dev), чтобы просмотреть мои резюме и CV.

## Запуск

1. Первый раз пишем `curl -fsSL https://bun.sh/install | bash`, затем `git clone https://github.com/VityaSchel/q-midpass-ru-autoconfirm && bun install` и вставляем API ключ от [https://rucaptcha.ru/](https://rucaptcha.ru/) и почту и пароль от q.midpass.ru в файле **config.conf**

    Пример config.conf:
    ![Скриншот config.conf](https://i.imgur.com/WWoR8xR.png)

2. Далее раз в сутки пишем `bun start`

Иногда сайт может начать говниться и выкинуть такую ошибку:
![qmidpass ошибка бот](https://i.imgur.com/SyqEDe1.png)
Тогда скрипт это поймет и предупредит в консоли

## Про остальные файлы

.gitignore — чтобы в репозиторий не попадали всякие генерируемые файлы
package.json и bun.lockb — чтобы установить зависимости
tsconfig.json — чтобы линтился код

## Поддержать

[hloth.dev/donate](https://hloth.dev/donate)
