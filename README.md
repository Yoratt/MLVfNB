> [!NOTE]
> Данный сайт больше не актуален, так как в Telegram добавили [расширенное форматирование](https://telegram.org/blog/watch-apps-and-more/ru#do-neprilichiya-rasshirennoe-formatirovanie-teksta-dlya-botov) для ботов.

---

### Markdown & Latex Viewer for Nikitendo's bots
# Сократитель сообщений с форматированием

Это специальный сайт для предпросмотра форматированного текста сообщения. Здесь можно сохранять текстовые сообщения, которые поддерживают Markdown и LaTeX.


Сайт: https://gamesinprism-preview.vercel.app



Создайте сообщение через API-запрос POST [`/api/messages`](https://gamesinprism-preview.vercel.app/api/messages) с токеном авторизации (заголовок `x-api-token`. Например: `X-API-Token: ABCD...YZ`) и содержанием POST-запроса типа такого:

    { body: '[Анализ: Режим помощника активирован. Пользователь запрашивает вычисление логарифма.]', author: 'коннор' }

Для получения токена обратитесь в [Службу поддержки](t.me/YorattSupportBot).

Вы получите такой ответ:

    { url: 'https://gamesinprism-preview.vercel.app/OGI3gESs', slug: 'OGI3gESs' }
    
После этого вы получите короткую ссылку вроде:
https://gamesinprism-preview.vercel.app/OGI3gESs

При открытии ссылки отображается красиво отформатированный текст с поддержкой формул и кода — как на Markdown, но с математикой.


Разработанно для проекта «Чат в призме субъективности».


---

Устаревшая версия сайта: https://yoratt.github.io/MLVfNB/

Алгоритм работы:

    LZString.compressToEncodedURIComponent('[Активация электротехнического протокола. Анализ соотношения электрических и механических углов.]')

Затем через параметр `t`:

    yoratt.github.io/MLVfNB?t=FAbUC...mzg+CAA
