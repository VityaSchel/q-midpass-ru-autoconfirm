# Автоподтверждение q.midpass.ru за 5 секунд

Скрипт для автоматического подтверждения свей заявки на загранпаспорт в консульстве России.

Мой скрипт написан на JS и puppeteer и хорош тем, что вам нужно посмотреть всего один файл, чтобы удостовериться, что он не наносит никакого вреда. Вообще весь код в одном маленьком файле. simply run index.ts.

> [!IMPORTANT]
> Я ищу работу! Если вы заинтересованы в моем найме, посетите [cv.hloth.dev](https://cv.hloth.dev), чтобы просмотреть мои резюме и CV.

## Запуск

1. Первый раз пишем `curl -fsSL https://bun.sh/install | bash`, затем `git clone https://github.com/VityaSchel/q-midpass-ru-autoconfirm && bun install` и вставляем API ключ от [https://rucaptcha.ru/](https://rucaptcha.ru/), почту и пароль от q.midpass.ru, а так же код страны и консульства (можно посмотреть в исходнике сайта) в файл **config.conf**

    Пример config.conf:
    ![Скриншот config.conf](https://i.imgur.com/WWoR8xR.png)

    Пример значений `COUNTRY` и `LOCATION` для config.conf:

    ```javascript
    COUNTRY=88655495-3b8c-f56d-5337-0f2743a7bfed # Грузия
    COUNTRY=feb5c602-1325-2704-d302-eb228cfbd2cb # США
    LOCATION=b8af6319-9d8d-5bd9-f896-edb8b97362d0 # Тбилиси
    LOCATION=ea52c900-b992-dc1f-960d-a0e02771622c # Нью-Йорк
    ```

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
