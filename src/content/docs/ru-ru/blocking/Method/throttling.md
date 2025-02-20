---
title: Ограничение скорости (Throttling)
description: 'Узнайте об ограничении скорости интернета.'
posted: 2024-09-21T21:00:00.000Z
---
### Ограничение скорости в интернет-цензуре
**Ограничение скорости** (Throttling) относится к преднамеренному замедлению интернет-скорости для определённых веб-сайтов или сервисов интернет-провайдером или властями. Этот метод часто используется для того, чтобы сделать доступ к определённым платформам неудобным или практически невозможным, не прибегая к их полной блокировке.

Признаки ограничения скорости включают:
- Веб-сайты загружаются необычно долго, несмотря на достаточную общую скорость интернета.
- Медиаэлементы, такие как видео, изображения или потоковый контент, сильно задерживаются или часто буферизуются.
- Значительные различия в производительности при доступе к одному и тому же веб-сайту или сервису через разные сети или инструменты (например, VPN).

Ограничение скорости часто реализуется с использованием аппаратного обеспечения для **глубокой проверки пакетов (DPI)**, которое может идентифицировать и ограничивать трафик для определённых сервисов на основе шаблонов данных, протоколов или доменных имён.

Общий способ ручной проверки на наличие ограничения скорости со стороны провайдера:
>
 - Найдите URL ресурса, который загружается медленно, например, видеофайла.
 - Откройте "Командную строку" (Windows) / Терминал (Linux, macOS).
 - Введите `curl -o output.bin -v https://example.com/video.mp4` и запомните скорость загрузки.
 - Введите `curl -o output.bin -v https://domain.name.of.the.website.com/video.mp4 -H ‘Host: example.com’` и проверьте, быстрее ли загрузка по сравнению с #3.

Интерпретация результатов:
>
 - Если запрос с заменённым доменом в #4 быстрее, чем запрос #3, это означает, что ограничение скорости применяется с использованием DPI, проверяя домен, к которому обращаются.
 - Если доступ к другому IP-адресу с использованием того же доменного имени восстанавливает скорость, это может означать, что ограничение скорости применяется на уровне IP-адреса, либо что соединение между вашим провайдером и хостом назначения просто медленное.

Решения для обхода:
>
 - VPN/Прокси.
 - (иногда) ПО для обхода DPI: [GoodbyeDPI](https://github.com/ValdikSS/GoodbyeDPI), [zapret](https://github.com/bol-van/zapret), [ByeDPI](https://github.com/hufrea/byedpi), [SpoofDPI](https://github.com/xvzc/SpoofDPI), [PowerTunnel](https://github.com/krlvm/PowerTunnel).

Регионы:
- Россия
- Туркменистан
- Казахстан
- Иран
- Китай
