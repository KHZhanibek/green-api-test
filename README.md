# GREEN-API — тестовая HTML-страница

HTML-страница для проверки методов [GREEN-API](https://green-api.com.kz/docs/):

- `getSettings`
- `getStateInstance`
- `sendMessage`
- `sendFileByUrl`

## Быстрый старт

1. Создайте инстанс в [личном кабинете GREEN-API](https://console.green-api.com/) (тариф «Разработчик»).
2. Отсканируйте QR-код в WhatsApp и дождитесь статуса `authorized`.
3. Скопируйте `idInstance` и `ApiTokenInstance` из кабинета.
4. Откройте `index.html` в браузере или опубликуйте страницу (см. ниже).
5. Введите параметры подключения и по очереди нажмите кнопки методов.
6. Ответ API отображается в поле **«Ответ методов»** (только чтение).

### sendMessage

- `chatId` — номер получателя в формате `79991234567@c.us` (для группы — `...@g.us`).
- `message` — текст сообщения.

Для проверки можно отправить сообщение себе (номер, привязанный к инстансу).

### sendFileByUrl

- `chatId` — идентификатор чата.
- `urlFile` — прямая ссылка на файл (например, изображение).
- `fileName` — имя с расширением (`photo.jpg`).
- `caption` — подпись (необязательно).

Пример URL файла из документации:

`https://storage.yandexcloud.net/green-api.com/logo/Logo_GREEN-API.jpg`

## Публикация на GitHub

```bash
cd green-api-test
git init
git add index.html README.md
git commit -m "Add GREEN-API test HTML page"
git branch -M main
git remote add origin https://github.com/<ваш-логин>/green-api-test.git
git push -u origin main
```

## Публикация страницы в Интернете (GitHub Pages)

1. В репозитории на GitHub: **Settings → Pages**.
2. **Source**: Deploy from branch.
3. **Branch**: `main`, папка `/ (root)`.
4. Сохраните — через 1–2 минуты страница будет доступна по адресу:

   `https://<ваш-логин>.github.io/green-api-test/`

Укажите эту ссылку при сдаче тестового задания.

## Короткое видео для сдачи

Рекомендуемый сценарий (1–3 минуты):

1. Личный кабинет: инстанс в статусе авторизован.
2. Открытие опубликованной HTML-страницы.
3. Ввод `idInstance` и `ApiTokenInstance` (токен можно частично закрыть).
4. Нажатие **getSettings** и **getStateInstance** — ответ в поле внизу.
5. **sendMessage** — сообщение приходит в WhatsApp.
6. По желанию — **sendFileByUrl**.

## Ссылки

- [Документация GREEN-API](https://green-api.com.kz/docs/)
- [getSettings](https://green-api.com.kz/docs/api/account/GetSettings/)
- [getStateInstance](https://green-api.com.kz/docs/api/account/GetStateInstance/)
- [sendMessage](https://green-api.com.kz/docs/api/sending/SendMessage/)
- [sendFileByUrl](https://green-api.com.kz/docs/api/sending/SendFileByUrl/)
