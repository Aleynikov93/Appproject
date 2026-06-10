# ✅ Чек-лист — Google Maps Places API

> **Проект:** [Appproject](https://github.com/Aleynikov93/Appproject) · **Тестировщик:** Алейников Сергей · **Дата:** Июнь 2026

---

## Навигация по документации

| Документ | Файл |
|---|---|
| 📋 Тест-план | [`docs/test_plan.md`](test_plan.md) |
| ✅ Чек-лист | `docs/checklist.md` ← вы здесь |
| 📊 Итоговый отчёт | [`docs/test_report.md`](test_report.md) |

---

## Шаг 1 — `POST /maps/api/place/add/json`

Создание локации `"Frontline house"` по адресу `"29, side layout, cohen 09"`

| # | Проверка | Метод `Cheking` | Ожидаемый результат | Статус |
|---|---|---|---|:---:|
| 1 | Статус код ответа | `check_status_code` | `200` | ✅ |
| 2 | Поле `status` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 3 | Поле `place_id` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 4 | Поле `scope` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 5 | Поле `reference` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 6 | Поле `id` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 7 | Значение `status` = `"OK"` | `check_json_value` | `"OK"` | ✅ |
| 8 | `place_id` не пустой, передаётся дальше | — | Не пустой | ✅ |

---

## Шаг 2 — `GET /maps/api/place/get/json?place_id={id}`

Получение созданной локации

| # | Проверка | Метод `Cheking` | Ожидаемый результат | Статус |
|---|---|---|---|:---:|
| 9 | Статус код ответа | `check_status_code` | `200` | ✅ |
| 10 | Поле `location` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 11 | Поле `accuracy` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 12 | Поле `name` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 13 | Поле `phone_number` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 14 | Поле `address` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 15 | Поле `types` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 16 | Поле `website` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 17 | Поле `language` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 18 | `address` = `"29, side layout, cohen 09"` | `check_json_value` | Совпадает | ✅ |

---

## Шаг 3 — `PUT /maps/api/place/update/json`

Обновление адреса на `"100 Lenina street, RU"`

```json
{ "place_id": "...", "address": "100 Lenina street, RU", "key": "qaclick123" }
```

| # | Проверка | Метод `Cheking` | Ожидаемый результат | Статус |
|---|---|---|---|:---:|
| 19 | Статус код ответа | `check_status_code` | `200` | ✅ |
| 20 | Поле `msg` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 21 | `msg` = `"Address successfully updated"` | `check_json_value` | Совпадает | ✅ |

---

## Шаг 4 — `GET /maps/api/place/get/json?place_id={id}`

Проверка, что адрес действительно обновился

| # | Проверка | Метод `Cheking` | Ожидаемый результат | Статус |
|---|---|---|---|:---:|
| 22 | Статус код ответа | `check_status_code` | `200` | ✅ |
| 23 | Поле `location` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 24 | Поле `accuracy` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 25 | Поле `name` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 26 | Поле `phone_number` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 27 | Поле `address` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 28 | Поле `types` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 29 | Поле `website` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 30 | Поле `language` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 31 | `address` = `"100 Lenina street, RU"` | `check_json_value` | Совпадает | ✅ |

---

## Шаг 5 — `DELETE /maps/api/place/delete/json`

Удаление локации

```json
{ "place_id": "..." }
```

| # | Проверка | Метод `Cheking` | Ожидаемый результат | Статус |
|---|---|---|---|:---:|
| 32 | Статус код ответа | `check_status_code` | `200` | ✅ |
| 33 | Поле `status` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 34 | Значение `status` = `"OK"` | `check_json_value` | `"OK"` | ✅ |

---

## Шаг 6 — `GET /maps/api/place/get/json?place_id={id}`

Проверка, что удалённая локация недоступна

| # | Проверка | Метод `Cheking` | Ожидаемый результат | Статус |
|---|---|---|---|:---:|
| 35 | Статус код ответа | `check_status_code` | `404` | ✅ |
| 36 | Поле `msg` присутствует | `check_json_token` | Есть в ответе | ✅ |
| 37 | `msg` содержит `"failed"` | `check_json_search_word_value` | Содержит | ✅ |

---

## Итого

| Всего проверок | ✅ Пройдено | ❌ Провалено | ⏭ Не выполнено | Результат |
|:---:|:---:|:---:|:---:|:---:|
| **37** | **37** | **0** | **0** | **✅ PASSED** |
