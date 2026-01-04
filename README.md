## Community App Store для Umbrel: как использовать

Community App Store (магазин приложений сообщества) для Umbrel позволяет разработчикам распространять приложения без публикации в официальном магазине.

### Шаги

1) Создайте свой репозиторий (например, на GitHub) и разместите в нём структуру Community App Store.

2) Задайте ID и имя вашего магазина приложений в файле `umbrel-app-store.yml`.
   В этом файле указываются два важных атрибута:
   - `id` — уникальный префикс для каждого приложения в вашем Community App Store.
     ID каждого приложения должен начинаться с ID магазина.
     Пример: если `id` магазина — `sparkles`, а приложение называется `hello world`,
     тогда ID приложения должен быть `sparkles-hello-world`.
   - `name` — имя Community App Store, которое будет отображаться в интерфейсе umbrelOS.

3) Создайте (или переименуйте) папку приложения так, чтобы её название совпадало с ID приложения.
   Пример: если `id` магазина — `whistles`, а приложение называется My Video Downloader,
   можно задать ID приложения `whistles-my-video-downloader` и назвать папку так же:
   `whistles-my-video-downloader`.

4) Заполните информацию о приложении в файле `whistles-my-video-downloader/umbrel-app.yml`.
   Эти данные отображаются в интерфейсе umbrelOS.

5) Добавьте нужные Docker-сервисы в `whistles-my-video-downloader/docker-compose.yml`.

6) Подключите ваш Community App Store в umbrelOS: добавьте URL вашего GitHub-репозитория
   через интерфейс umbrelOS (пример показан в демо-видео):

https://user-images.githubusercontent.com/10330103/197889452-e5cd7e96-3233-4a09-b475-94b754adc7a3.mp4
