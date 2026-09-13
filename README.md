# Fast Free VPN Subscription — raw list, TLS-verified, best-of-best

Автоматически обновляемая подписка бесплатных VPN-серверов в raw-формате (vless / vmess / trojan / ss / hysteria2). Серверы берутся из открытых агрегаторов (Epodonios, mahdibland), проверяются живым TCP-пробом, реальным TLS-рукопожатием и геолокацией стран. Всё собирается и заливается одной командой.

## 📡 Подписка (для Happ и любых v2ray-клиентов)

| Что | Ссылка |
|---|---|
| **TOP ELITE — 16 лучших** (TLS проверены, быстрейшие первыми) | `https://raw.githubusercontent.com/2014kirillsab-oss/sub/main/best.txt` |
| То же в base64-подписке | `https://raw.githubusercontent.com/2014kirillsab-oss/sub/main/sub.txt` |
| Все проверенные TLS (16) | `https://raw.githubusercontent.com/2014kirillsab-oss/sub/main/verified.txt` |
| Живые VLESS/Trojan (≈85) | `https://raw.githubusercontent.com/2014kirillsab-oss/sub/main/vless_trojan.txt` |
| Полный архив всех серверов (≈800) | `https://raw.githubusercontent.com/2014kirillsab-oss/sub/main/happ.txt` |
| Элита в JSON | `https://raw.githubusercontent.com/2014kirillsab-oss/sub/main/best.json` |
| Все серверы в JSON | `https://raw.githubusercontent.com/2014kirillsab-oss/sub/main/sub.json` |

## 🚀 Быстрый старт

1. Скопируй ссылку `best.txt` в буфер.
2. В Happ: *Настройки → Подписка → Добавить* → вставь ссылку → обновить.
3. Включи режим **TUN** (глобальный) и отключи IPv6 — иначе часть трафика уходит мимо туннеля.
4. Начинай с первого сервера (самый быстрый). Проверка выхода: `2ip.ru` — IP должен быть не российским.

Любой v2ray-клиент (v2rayNG, Shadowrocket, Clash и др.) принимает эти ссылки напрямую.

## 🏷 Метки в названиях серверов

- `⚡` — быстрый: реальное время TLS-рукопожатия ≤ 250 мс
- `🌍 Cloudflare / Fastly` — адрес за CDN: своей страны у сервера нет, флаг был бы враньём
- `🇩🇪 Германия`, `🇺🇸 США` … — реальная страна по IP (ipinfo.io) или имени хоста

## 🔄 Обновление в один клик

```
update.bat
```

Конвейер (`update_all.js`): скачивает свежие списки → выделяет новые серверы → замеряет задержку всех → геолоцирует новые IP → проверяет TLS-рукопожатия → собирает файлы → заливает на GitHub и печатает ссылки. Токен лежит в `token.txt` (не коммитится).

## ⚠️ Честные оговорки

- Это **бесплатные** серверы из открытых списков: они живут от часов до недель, умирают без предупреждения.
- "Живой порт + TLS" ≠ гарантия скорости: полосу не измерить без реального трафика.
- hysteria2 работает через UDP/QUIC — TCP-пробой не проверяется, в BEST не попадает.
- Подписка распространяется **как есть**, без каких-либо гарантий.

## 📄 Лицензия

MIT — см. [LICENSE](LICENSE). Списки серверов принадлежат их создателям.