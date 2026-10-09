# Топ банков РФ и их API

**Презентация:** [russian-banks-api-research.pptx](./russian-banks-api-research.pptx) — 10 слайдов, клоны реальных макетов из шаблона Sber CIB

**Повторный аудит 09.10.2026:** капитализации, место ПСБ, модель доступа СберБизнес, уточнение FX/депозитов Сбера.

---

# Ресерч: топ банков РФ и их API

**Дата отчёта:** 8 октября 2026 · **повторный аудит метрик и API:** 9 октября 2026  
**Метод:** только публичные источники (сайты банков, developer portals, отчётность, рейтинги, материалы ЦБ/АФТ, котировки Мосбиржи). Неподтверждённое помечено как «не найдено публично».  
**Аудит:** [`internal/full-data-reaudit-2026-10-09.md`](../internal/full-data-reaudit-2026-10-09.md)

---

## 1. Топ банков РФ (метрики)

Ранжирование по **активам** (основной публичный критерий размера). НКЦ (клиринговая НКО) в топ-список банков не включена.

| # | Банк | Активы | Чистая прибыль | Основной капитал / аналог | Клиенты | Капитализация (рыночная) |
|---|------|--------|----------------|--------------------------|---------|--------------------------|
| 1 | **Сбербанк** | 66,18 трлн ₽ (1.07.2026, РИА) | 1 694 млрд ₽ РСБУ / ~1 706 млрд ₽ МСФО (2025) | Основной капитал ~6,8 трлн ₽ (дек 2025, РСБУ) | 110,7 млн розн. + 3,5 млн корп. (конец 2025) | **~5,95 трлн ₽** (SBER ао, screener окт. 2026); SBERP отдельно ~0,28 трлн |
| 2 | **ВТБ** | 36,41 трлн ₽ (1.07.2026, РИА) | 502,1 млрд ₽ МСФО (2025) | 1,79 трлн ₽ основной капитал (1.11.2025) | 30,3 млн активных розн. (конец 2025) | **~0,73 трлн ₽** (VTBR ~728 млрд, screener окт. 2026); конец 2025 было ~1,46 трлн |
| 3 | **Газпромбанк** | 17,66 трлн ₽ (1.07.2026, РИА) | 132,6 млрд ₽ МСФО (2025) | 1,18 трлн ₽ основной капитал (1.11.2025) | ~5,7 млн активных розн. (итог 2024) | **не найдено публично** (непубличная компания) |
| 4 | **Альфа-Банк** | 14,33 трлн ₽ (1.07.2026, РИА) | 229,9 млрд ₽ МСФО (2025) | 0,93 трлн ₽ основной капитал (1.11.2025) | >40 млн ФЛ + >2 млн ЮЛ (май 2025) | **не найдено публично** (не торгуется широко) |
| — | **ПСБ** | **спорно:** Brobank — 5-е место на 1.07.2026 (рост +5,67%); в PDF РИА 1.07.2026 **в топ-40 не найден**. На 1.01.2026 Brobank: ~9,46 трлн | −19,1 млрд МСФО / +33 млрд РСБУ (2025) | 0,62 трлн ₽ основной капитал (1.11.2025) | **не найдено публично** | **не найдено публично** |
| 5* | **Т-Банк** | 5,70 трлн ₽ (1.07.2026, РИА; 6-е с НКЦ / 5-е без НКЦ) | 122,1 млрд ₽ МСФО (2025, банк) | 0,50 трлн ₽ основной капитал (1.11.2025) | ~52,8 млн всего / ~34 млн активных (сент. 2025) | **~713 млрд ₽** — холдинг **Т-Технологии** (T/TCSG), 09.10.2026 |
| 6* | **Россельхозбанк** | 5,50 трлн ₽ (1.07.2026, РИА) | **не найдено публично** | 0,40 трлн ₽ основной капитал (1.11.2025) | **не найдено публично** | **не найдено** (госбанк) |
| 7* | **МКБ** | 4,96 трлн ₽ (1.07.2026, РИА) | **не найдено публично** | **не найдено** в топ-10 по капиталу Коммерсанта | **не найдено публично** | **~0,31 трлн ₽** (CBOM, screener окт. 2026) |
| 8* | **ДОМ.РФ** | 4,90 трлн ₽ (1.07.2026, РИА) | **не найдено публично** | **не найдено** в топ-10 по капиталу | **не найдено публично** | **не найдено** |
| 9* | **Совкомбанк** | 4,32 трлн ₽ (1.07.2026, РИА) | 53 млрд ₽ МСФО (2025) | 0,38 трлн ₽ основной капитал (1.11.2025) | ранее ~8+ млн ФЛ (2024) | **~0,22–0,24 трлн ₽** (SVCB, окт. 2026) |

\*Нумерация 5–9 — место **без НКЦ** по РИА 1.07.2026. ПСБ вынесен отдельно из‑за расхождения РИА vs Brobank.

### Источники метрик (даты)

- **Активы 1.07.2026:** [РИА Рейтинг — рейтинг банков по активам](https://riarating.ru/images/63030/05/630300556.pdf)
- **Активы 1.01.2026 (ПСБ и сверка):** [Brobank.ru PDF](https://brobank.ru/wp-content/uploads/2026/05/rejting-bankov-po-obemu-aktivov-po-itogu-2025-goda-1.pdf)
- **Основной капитал 1.11.2025:** [Коммерсантъ](https://www.kommersant.ru/doc/8270557)
- **Сбер (финрезультат):** [итоги 2025 РСБУ](https://www.sberbank.com/ru/investor-relations/groupresults/paosber_12month_reporting_for_investors), [МСФО Q4 2025](https://www.sberbank.com/ru/investor-relations/groupresults/ifrs_february26_reporting_for_the_4th_quarter)
- **Сбер (капитализация):** ~5,95 трлн ₽ SBER ао ([Investmint screener](https://investmint.ru/screener/), окт. 2026); SBERP отдельно
- **ВТБ:** [Коммерсантъ о прибыли 2025](https://www.kommersant.ru/doc/8462026); капитализация VTBR ~728 млрд ₽ (тот же screener, окт. 2026)
- **ГПБ:** [пресс-релиз МСФО 2025](https://www.gazprombank.ru/press/8059345/), [Finmarket](https://www.finmarket.ru/news/6589542)
- **Альфа:** [Коммерсантъ](https://www.kommersant.ru/doc/8603729) (17.04.2026)
- **Т-Банк (финрезультат):** [МЭЦ / отчётность МСФО 2025](https://mec-analytics.ru/media/news/ao-tbank-publikuet-rezultaty-po-msfo-za-2025-g-/)
- **Т-Технологии (капитализация):** [Investfunds / Мосбиржа](https://investfunds.ru/stocks/TKS-Holding-IPJSC/) — **712,9 млрд ₽** на 09.10.2026
- **МКБ / Совкомбанк (капитализация):** CBOM ~312 млрд, SVCB ~237 млрд (Investmint, окт. 2026)
- **ПСБ:** [Коммерсантъ](https://www.kommersant.ru/doc/8499718); место в активах — [Brobank H1 2026](https://brobank.ru/aktivy-bankov-v-pervoj-polovine-2026-goda/) vs отсутствие в PDF РИА
- **Совкомбанк (прибыль):** [VN.ru](https://vn.ru/news-sovkombank-zarabotal-za-2025-god-53-mlrd-rub-chistoy-pribyli-po-msfo/)

**Примечания**
- Активы по банковской отчётности (РИА) и по МСФО группы могут расходиться (пример ВТБ).
- **Капитализация «Т-Банка»** в гугле = капитализация холдинга **Т-Технологии** (T/TCSG), не юрлица АО «ТБанк».
- **ПСБ:** расхождение РИА (нет в топ-40 на 1.07.2026) vs Brobank (5-е место) — в таблице отмечено явно.
- **Исправления 09.10.2026:** капитализации Т/Сбер/ВТБ/МКБ/Совком; модель доступа СберБизнес; уточнение статусов FX/депозитов Сбера.

---

## 2. API / программный доступ по банкам

Легенда статусов:
- **есть** — есть документированный публичный API по сути категории (portal/docs, можно интегрировать);
- **частично** — только кусок категории, либо терминал/H2H/пилот/partner без полного self-serve API;
- **не найдено публично** — в открытых источниках подтверждения нет.

---

### 2.1. Сбербанк

**Порталы:** [Sber API overview](https://developers.sber.ru/docs/ru/sber-api/start/overview), [продуктовая страница](https://developers.sber.ru/portal/products/sber-api), [SberCIB Terminal](https://www.sberbank.ru/ru/legal/investments/globalmarkets/voperations)

**Модель доступа (важно):** Sber API продаётся **наборами**, ЛК живёт внутри **СберБизнес**:
| Набор | Для кого | Что внутри (кратко) |
|-------|----------|---------------------|
| **Компаниям** (бывш. Host2Host) | одна организация | платежи, выписки, депозиты/НСО, ВЭД, СБП, карты, эквайринг… |
| **Холдингам** | группа компаний | платежи/выписки/депозиты/ВЭД по дочерним (отдельные токены) |
| **Платформам** (бывш. B2BSaaS) | сервис поверх клиентов банка | платежи/выписки/СБП от имени клиентов платформы |
| **СберБизнес ID** | SSO | авторизация клиентов на сайте партнёра |
| **Кредит в корзине** | B2B-покупки в кредит | credit offers |

| Категория | Статус | Тип доступа | Документация / детали | Ограничения |
|-----------|--------|-------------|----------------------|-------------|
| **FX spot** | **есть*** | Sber API: поручения на покупку/продажу валюты (`CONVERSION_OPERATION_CURRENCY`) | [Conv currency](https://developers.sber.ru/docs/ru/sber-api/scenarios/ved/conv-currency/overview) | *Корп. конверсия, не CIB trading Terminal. Набор «Компаниям»; СберБизнес ID |
| **Brokerage (repo, bonds…)** | **не найдено публично** | — | Публичного Invest API (аналог T-Invest) **нет** | — |
| **Депозиты / FX swap / forward** | **частично** | **Депозиты+НСО = есть** в Sber API; **SWAP/FWD/NDF** — SberCIB Terminal (UI + заявленное API без публичной OpenAPI-спеки) | [Депозиты](https://developers.sber.ru/docs/ru/sber-api/scenarios/placement/deposit/overview) | Депозиты RUB/CNY/INR; sandbox есть |
| **Credits + rates (cap/floor)** | **частично** | «Кредит в корзине» / `GET_CREDIT_OFFERS`; **cap/floor treasury API нет** | [Credit offers](https://developers.sber.ru/docs/ru/sber-api/specifications/credit-offers/get-credit-offers) | Партнёрский набор |
| **Transactions** | **есть** | наборы Компаниям / Холдингам / Платформам | [Платежи](https://developers.sber.ru/docs/ru/sber-api/scenarios/transfers/payments/overview), [Выписки](https://developers.sber.ru/docs/ru/sber-api/scenarios/rko/statements/overview) | Клиент/пользователь **СберБизнес**; ЭП; scope в договоре |
| **Прочее** | **есть** | portal + тестовый стенд | ВЭД, карты, эквайринг, самозанятые, инкассация, СБП | Юрлица/ИП РФ |

---

### 2.2. ВТБ

**Порталы:** [developer.vtb.ru](https://developer.vtb.ru/), [Интеграционный Банк-Клиент](http://vtb.ru/krupnyj-biznes/raschety/distancionnoe-bankovskoe-obsluzhivanie/integracionnyj-bank-klient/), [eFX платформа](https://www.vtb.ru/krupnyj-biznes/elektronnaya-torgovlya-fx/), [sandbox платёжного шлюза](https://sandbox.vtb.ru/sandbox/ru/integration/api/rest.html)

| Категория | Статус | Тип доступа | Документация / детали | Ограничения |
|-----------|--------|-------------|----------------------|-------------|
| **FX spot** | **частично** | Казначейская eFX-платформа (терминал + STP), не публичный Open API | TOD/TOM/SPOT/SWAP на странице eFX; API-каталог portal за логином | Крупный бизнес / договор; публичной REST-спеки FX **не найдено** |
| **Brokerage** | **не найдено публично** | — | Публичного Invest/broker API ВТБ **не найдено** | — |
| **Депозиты / FX swap / forward** | **частично** | SWAP на eFX; депозиты как Open API **не найдены** | eFX: SWAP заявлен; депозитный API — **не найдено публично** | Клиент крупного бизнеса |
| **Credits + rates** | **не найдено публично** | — | — | — |
| **Transactions** | **есть** | H2H / ИБК (SOAP/XML, Host-to-Host); эквайринг REST | ИБК: платежи, выписки, статусы; [API эквайринга](https://sandbox.vtb.ru/sandbox/ru/integration/api/rest.html) | Расчётный счёт + ДБО; sandbox для платежей |
| **Прочее** | **частично** | Developer portal (регистрация), partner | Каталог API за аутентификацией; полный публичный перечень scopes **не опубликован** без входа | Корп./партнёр |

---

### 2.3. Газпромбанк

**Порталы / страницы:** [Host-to-host](https://www.gazprombank.ru/corporate/page/h2h/), [Open API курсов](https://www.gazprombank.ru/personal/page/openapi/), [АС API менеджмент](https://www.gazprombank.ru/special/a/API/)

| Категория | Статус | Тип доступа | Документация / детали | Ограничения |
|-----------|--------|-------------|----------------------|-------------|
| **FX spot** | **частично** | H2H: конверсионные операции; отдельный публичный FX trading API **не найден** | H2H ISO 20022: «выполнение конверсионных операций» | Корп. клиент; `transact_go@gazprombank.ru` |
| **Brokerage** | **не найдено публично** | — | — | — |
| **Депозиты / FX swap / forward** | **не найдено публично** | — | Как Open API — не найдено | — |
| **Credits + rates** | **не найдено публично** | — | — | — |
| **Transactions** | **есть** | H2H / API / клиентский модуль / Мультибанк | Рублёвые и валютные переводы, статусы, выписки, ВЭД, зарплата | Резидент РФ (на странице указан выбор резидентства); корп. договор |
| **Прочее** | **частично** | Публичный API **курсов валют и металлов**; partner API gateway | [openapi курсов](https://www.gazprombank.ru/personal/page/openapi/); GPB_API@gazprombank.ru | Курсы — по заявке + whitelist IP |

---

### 2.4. Альфа-Банк

**Порталы:** [developers.alfabank.ru](https://developers.alfabank.ru/), [Alfa API для бизнеса](https://alfabank.ru/sme/alfaapi/), [Альфа-Линк H2H](https://alfabank.ru/corporate/rko/h2h/), [Альфа-Инвестиции PRO API](https://alfadt.servicecdn.ru/alfadt/ad5/Alfa-Investments-Pro-API.pdf)

| Категория | Статус | Тип доступа | Документация / детали | Ограничения |
|-----------|--------|-------------|----------------------|-------------|
| **FX spot** | **частично** | H2H: поручение на конвертацию; Alfa API — валютные расчёты заявлены на продуктовых страницах | Альфа-Линк: конвертация, валютные ПП | Корп. клиент / H2H договор; sandbox на developer portal |
| **Brokerage** | **есть** | Open API через PRO-терминал (локальный WebSocket router + Bearer) | [PRO API PDF](https://alfadt.servicecdn.ru/alfadt/ad5/Alfa-Investments-Pro-API.pdf); рынок, заявки, счёт | Клиент Альфа-Инвестиций; API включается в терминале |
| **Депозиты / FX swap / forward** | **частично** | Продуктово заявлены депозиты/бивалютный депозит в экосистеме Alfa API; swap/forward API **не найдены** | [alfabank.ru/sme/alfaapi](https://alfabank.ru/sme/alfaapi/) | Юрлица; scopes по договору |
| **Credits + rates** | **частично** | Раздел «Кредиты» на developer portal; cap/floor **не найдено** | developers.alfabank.ru — продукт «Кредиты» | Партнёр / клиент |
| **Transactions** | **есть** | Partner + H2H + sandbox | Выписки, ПП, СБП, карты | Оферта на portal; sandbox → prod после успешных тестов |
| **Прочее** | **есть** | Alfa ID, справки, партнёрские интеграции | Portal с документацией и API Helper | РФ; для H2H — средний/крупный бизнес |

> **Важно:** каталог Open API Альфа-Банка **Беларусь** ([developerhub.alfabank.by](https://developerhub.alfabank.by/)) — отдельная юрисдикция; в матрицу РФ не смешивать.

---

### 2.5. ПСБ (Промсвязьбанк)

**Страницы:** [Host-to-Host / OpenAPI](https://www.psbank.ru/corporate/dbo/host-to-host)

| Категория | Статус | Тип доступа | Документация / детали | Ограничения |
|-----------|--------|-------------|----------------------|-------------|
| **FX spot** | **не найдено публично** | — | — | — |
| **Brokerage** | **не найдено публично** | — | — | — |
| **Депозиты / FX swap / forward** | **не найдено публично** (как API) | Депозиты — через ДБО UI | Публичной API-спеки депозитов нет | — |
| **Credits + rates** | **частично** | Partner / Open API пилоты (заявки на кредиты ЮЛ без визита — по заявлениям банка в СМИ 2024+) | Публичной полной спецификации endpoint’ов **не найдено** | Юрлица, клиент ПСБ |
| **Transactions** | **есть** | H2H: DirectBank (1С SOAP/XML) + банковский OpenAPI REST/JSON | Описание на psbank.ru/corporate/dbo/host-to-host | Счёт + PSB Corporate |
| **Прочее** | **частично** | Участие в пилотах Open Banking АФТ/ЦБ | [wiki.openbankingrussia.ru](https://wiki.openbankingrussia.ru/ru/specifications) | Пилотный режим стандартов |

---

### 2.6. Т-Банк

**Порталы:** [T-API Business](https://developer.tinkoff.ru/tapi/), [OpenAPI YAML](https://business.tbank.ru/openapi/docs/openapi.yaml), [T-Invest API](https://developer.tbank.ru/invest/intro/intro/), [GitHub investAPI](https://github.com/RussianInvestments/investAPI)

| Категория | Статус | Тип доступа | Документация / детали | Ограничения |
|-----------|--------|-------------|----------------------|-------------|
| **FX spot** | **частично** | Через T-Invest: валютные инструменты и торговля на бирже (не OTC treasury spot банка) | InstrumentsService/Currencies; Orders | Клиент Т-Инвестиций + токен; sandbox |
| **Brokerage** | **есть** | Публичный Open API (gRPC / REST / WebSocket) | Bonds, акции, ETF, фьючерсы, заявки, portfolio, market data; **отдельного repo-API не найдено** | Токен в ЛК; брокерский счёт |
| **Депозиты / FX swap / forward** | **частично** | Депозиты + овернайты в T-API Business; FX swap/forward treasury **не найдены** | Теги `Депозиты`, `Овернайты` в openapi.yaml; mTLS на secured-openapi | Юрлицо / бизнес-клиент |
| **Credits + rates** | **частично** | Партнёрские кредитные продукты, POS, автокредиты, заявки; cap/floor **не найдено** | Теги кредитных продуктов в openapi.yaml | Партнёрский договор |
| **Transactions** | **есть** | Публичный Open API + sandbox | Счета/выписки, платежи, СБП, номинальные счета | OAuth / OpenID; доступы по INN/KPP |
| **Прочее** | **есть** | Эквайринг, зарплата, самозанятые, ВЭД, гарантии, карты | Один из самых широких публичных каталогов | РФ; разные scopes |

---

### 2.7. Россельхозбанк

| Категория | Статус | Комментарий |
|-----------|--------|-------------|
| Все целевые категории | **не найдено публично** | Публичного developer portal / Open API каталога, сопоставимого со Сбером/Альфой/Т-Банком, **не обнаружено**. Возможны закрытые H2H/казначейские интеграции — без публичной документации. |

---

### 2.8. МКБ

| Категория | Статус | Комментарий |
|-----------|--------|-------------|
| **Transactions / Open Banking** | **частично** | Участие в среде Открытых банковских интерфейсов (ОБИ) ЦБ / АФТ (2022+); пилоты обмена по счетам ЮЛ. Публичного self-service portal с полным каталогом **не найдено**. |
| **FX / Brokerage / Deposits / Credits API** | **не найдено публично** | — |

Источник контекста: [опыт интеграции Open API адаптера МКБ](https://plusworld.ru/journal/2023/plus-9-2023/kak-my-integrirovali-open-api-adapter-v-kontur-banka-opyt-mkb/).

---

### 2.9. Банк ДОМ.РФ

| Категория | Статус | Комментарий |
|-----------|--------|-------------|
| **Open Banking / ипотечные заявки** | **частично** | Пилоты Открытых API (в т.ч. со Сравни / АФТ) для ипотечных сценариев. |
| **FX / Brokerage / Deposits / Credits rates / Transactions (публичный каталог)** | **не найдено публично** | Отдельного developer portal с treasury/payments API **не найдено**. |

---

### 2.10. Совкомбанк

| Категория | Статус | Комментарий |
|-----------|--------|-------------|
| **Credits (ипотека и др.)** | **частично** | Partner API-интеграции (напр. с платформами недвижимости); не публичный self-serve portal. |
| **Страхование (группа)** | **частично** | [API Совкомбанк Страхование](https://sovcomins.ru/commercial-business/partners/api-integraciia/) — partner REST. |
| **FX / Brokerage / Deposits / Transactions (банк)** | **не найдено публично** | Публичного банковского Open API каталога **не найдено**. |

---

### Контекст: Open Banking в РФ

Стандарты и спецификации ведутся через **Ассоциацию ФинТех** и материалы ЦБ ([wiki.openbankingrussia.ru](https://wiki.openbankingrussia.ru/ru/specifications), документы ЦБ по счетам/переводам). На момент ресерча внедрение носит в основном **пилотный / рекомендательный** характер; наличие «Open Banking» у банка ≠ публичный developer portal по всем treasury-категориям.

---

## 3. Сводная матрица: банк × категория API

Обозначения: ✅ есть (публично подтверждено) · ◐ частично · ❌ не найдено публично

| Банк | FX spot | Brokerage | Депозиты / FX swap / forward | Credits + rates | Transactions | Прочее (ключевое) |
|------|---------|-----------|------------------------------|-----------------|--------------|-------------------|
| **Сбербанк** | ✅ корп. conv API (*не CIB Terminal) | ❌ | ◐ депозиты/НСО ✅; swap/fwd только CIB | ◐ credit-in-cart; cap/floor ❌ | ✅ | Наборы Компаниям/Холдингам/Платформам + СберБизнес |
| **ВТБ** | ◐ eFX терминал/STP | ❌ | ◐ SWAP в eFX; депозиты API ❌ | ❌ | ✅ H2H + эквайринг | Developer portal (за логином) |
| **Газпромбанк** | ◐ конверсия в H2H | ❌ | ❌ | ❌ | ✅ H2H ISO20022 | Публичный API курсов |
| **Альфа-Банк** | ◐ H2H/API конвертация | ✅ PRO API | ◐ депозиты заявлены; swap/fwd ❌ | ◐ кредиты API; cap/floor ❌ | ✅ | Alfa ID, СБП, sandbox |
| **ПСБ** | ❌ | ❌ | ❌ | ◐ пилоты кредитов ЮЛ | ✅ H2H OpenAPI/DirectBank | Пилоты Open Banking |
| **Т-Банк** | ◐ биржевые валюты Invest | ✅ T-Invest (bonds+) | ◐ депозиты/овернайты; swap/fwd ❌ | ◐ партнёрские кредиты | ✅ T-API | Самый полный публичный каталог |
| **РСХБ** | ❌ | ❌ | ❌ | ❌ | ❌ | — |
| **МКБ** | ❌ | ❌ | ❌ | ❌ | ◐ Open Banking пилоты | — |
| **ДОМ.РФ** | ❌ | ❌ | ❌ | ◐ ипотечные Open API пилоты | ❌ | — |
| **Совкомбанк** | ❌ | ❌ | ❌ | ◐ partner (ипотека и др.) | ❌ | Страховые partner API |

---

## 4. Краткие выводы

1. **По активам (РИА 1.07.2026, без НКЦ):** Сбер → ВТБ → ГПБ → Альфа → Т-Банк → РСХБ → МКБ → ДОМ.РФ → Совкомбанк. **ПСБ:** Brobank держит его в топ-5, в PDF РИА на ту же дату — нет в топ-40.
2. **Капитализация (окт. 2026):** Сбер ~5,95 трлн (ао); Т-Технологии ~713 млрд; ВТБ ~0,73 трлн; МКБ ~0,31; Совком ~0,22–0,24.
3. **Зрелые публичные API:** Т-Банк (T-API + T-Invest), Сбер (Sber API внутри **СберБизнес**, наборы Компаниям/Холдингам/Платформам), Альфа (Alfa API + H2H + PRO).
4. **У Сбера** корп. FX-конверсия и депозиты — документированный Open API; swap/fwd и brokerage — нет как self-serve; CIB Terminal — отдельный канал.
5. **Treasury swap/fwd / repo / cap/floor** почти нигде не отданы в публичный self-serve API.
6. «Не найдено публично» ≠ отсутствие закрытых H2H/казначейских интеграций.

---

## 5. Список ключевых ссылок

| Ресурс | URL |
|--------|-----|
| РИА Рейтинг активы 1.07.2026 | https://riarating.ru/images/63030/05/630300556.pdf |
| Sber API overview | https://developers.sber.ru/docs/ru/sber-api/start/overview |
| Sber депозиты | https://developers.sber.ru/docs/ru/sber-api/scenarios/placement/deposit/overview |
| Sber FX conversion | https://developers.sber.ru/docs/ru/sber-api/scenarios/ved/conv-currency/overview |
| SberCIB Terminal | https://www.sberbank.ru/ru/legal/investments/globalmarkets/voperations |
| VTB Developer | https://developer.vtb.ru/ |
| VTB eFX | https://www.vtb.ru/krupnyj-biznes/elektronnaya-torgovlya-fx/ |
| GPB H2H | https://www.gazprombank.ru/corporate/page/h2h/ |
| Alfa Developers | https://developers.alfabank.ru/ |
| Alfa-Link H2H | https://alfabank.ru/corporate/rko/h2h/ |
| Alfa Invest PRO API | https://alfadt.servicecdn.ru/alfadt/ad5/Alfa-Investments-Pro-API.pdf |
| T-API | https://developer.tinkoff.ru/tapi/ |
| T-Invest | https://www.tbank.ru/invest/open-api/ |
| T-Invest docs | https://developer.tbank.ru/invest/intro/intro/ |
| PSB H2H | https://www.psbank.ru/corporate/dbo/host-to-host |
| Open Banking RU specs | https://wiki.openbankingrussia.ru/ru/specifications |
