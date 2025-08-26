FitAI — статический лендинг (v1)
Дата: 2025-08-25

Содержимое архива:
• index.html — одностраничный сайт на Tailwind CDN (без сборки).
• / (больше файлов не требуется).

Как развернуть:
1) Откройте index.html локально — всё работает без сборки.
2) Загрузите index.html на любой хостинг (например, на статический хостинг S3, GitHub Pages, Vercel, Netlify).
3) Для подсчёта заявок подключите backend (FastAPI) или сервис формы.

Интеграция формы (коротко):
— В index.html найдите блок <form id="leadForm">.
— Замените обработчик JS на отправку через fetch:
    fetch('https://ВАШ-ДОМЕН/api/leads', {method:'POST', headers:{'Content-Type':'application/json'}, body: JSON.stringify(payload)})

UTM-метки:
— Поля utm_source / utm_medium / utm_campaign автоматически снимаются из URL и кладутся в hidden-поля формы.

Стиль:
— Палитра: лайм #84cc16 + графит/чёрный.
— Шрифт: Inter (Google Fonts).

Лицензия:
— Для внутренних нужд FitAI. Свободно модифицируйте.
