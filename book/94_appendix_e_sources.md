# Приложение Д. Ключевые источники

Дата доступа ко всем источникам — 15 сентября 2026 года. Уровни доказательности: A — официальная документация, закон, решение суда, большое исследование с раскрытой методикой; B — несколько независимых источников; C — кейс или вендорский датасет с методикой; D — мнение; E — anecdotal. Полный список из 377 источников — в файле `sources.md` проекта.

## Правила почтовых провайдеров и доставляемость

- Email sender guidelines — Google, живой документ (требования с февраля 2024) — https://support.google.com/a/answer/81126 — требования ко всем и к массовым отправителям, запрет фейковых Re: и покупки адресов, Google не отслеживает open rate — A
- Email sender guidelines FAQ — Google, живой документ (ужесточение с ноября 2025) — https://support.google.com/mail/answer/14229414 — спам-рейт ниже 0,1% и никогда 0,3%, статус массового отправителя навсегда, отказы с ноября 2025 — A
- Gmail sending limits in Google Workspace — Google, обновлено 10.09.2026 — https://support.google.com/a/answer/166852 — 2 000 писем в сутки, 500 на пробном тарифе — A
- Sender Requirements & Recommendations — Yahoo, живой документ — https://senders.yahooinc.com/best-practices/ — SPF и DKIM, DMARC p=none, спам ниже 0,3%, отписка за 2 дня — A
- Outlook’s Requirements for High-Volume Senders — Microsoft, 02.04.2025 — https://techcommunity.microsoft.com/blog/microsoft-defender-for-office-365-blog/strengthening-email-ecosystem-outlook%E2%80%99s-new-requirements-for%C2%A0high%E2%80%90volume-senders/4399730 — SPF, DKIM и DMARC для отправителей от 5 000 писем в сутки с мая 2025 — A
- Exchange Online limits — Microsoft, 07.04.2026 — https://learn.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits — 10 000 получателей в сутки на ящик, лимиты тенанта — A
- RFC 9989 (DMARCbis) — IETF, 20.05.2026 — https://datatracker.ietf.org/doc/draft-ietf-dmarc-dmarcbis/ — новый стандарт DMARC, отмена RFC 7489 — A
- RFC 8058 One-Click Unsubscribe — IETF, январь 2017 — https://www.rfc-editor.org/rfc/rfc8058.html — механизм отписки в один клик — A
- M3AAWG Position on Cold Email — M3AAWG, ноябрь 2025 — https://www.m3aawg.org/M3AAWGPositionOnColdEmail — похожие домены, множество ящиков, обход лимитов и имитация вовлечённости недопустимы — A
- M3AAWG Sender Best Common Practices v4.0 — M3AAWG, август 2026 — https://www.m3aawg.org/sites/default/files/doc_files/m3aawg-sender-best-common-practices-aug-27-2026.pdf — прогрев около 6 недель реальной почтой, искусственный прогрев не рекомендован, поддомен вместо домена-двойника — A
- Spamhaus’ take on Cold Emailing — Spamhaus, 2025 — https://www.spamhaus.org/resource-hub/spam/spamhaus-take-on-cold-emailing-aka-spam/ — одноразовые домены, warm-up и фейковая вовлечённость как признаки спама, листинг — A/D
- Технические и административные требования к рассылкам — VK (Mail), дата не указана — https://help.mail.ru/developers/mailing_rules/technical/ — opt-in, пороги жалоб 1,1% → 0,3% — A
- Email Client Market Share — Litmus, отчёт за июль 2026 — https://www.litmus.com/email-client-market-share/ — Apple MPP затрагивает около 55–60% открытий — A

## Россия: Яндекс 360, ESP и данные

- Отправить много писем (Яндекс 360 для бизнеса) — Яндекс, дата не указана — https://yandex.ru/support/yandex-360/business/mail/ru/web/letter/create/send-many-letters — лимиты 300/1 000/10 000/50, досрочная блокировка однотипных КП, требования к честным рассылкам — A
- Общие условия использования сервисов Яндекс 360 — Яндекс, 14.09.2026 — https://yandex.ru/legal/360_termsofuse/ru/ — запрет массовых рассылок и обхода ограничений — A
- Правила Яндекс Рассылок — Яндекс, дата не указана — https://yandex.ru/support/yandex-360/business/send/ru/rules — запрет писем без согласия и на ролевые адреса — A
- Антиспам-политика Unisender — Unisender, дата не указана — https://www.unisender.com/ru/antispam/ — запрет открытых источников, double opt-in для коммерческих предложений — A
- АнтиСПАМ-политика DashaMail — DashaMail, дата не указана — https://dashamail.ru/antispam/ — базы из 2ГИС и купленные адреса считаются спамом — A
- Порядок доступа к сведениям ЕГРЮЛ и ЕГРИП — ФНС России, дата не указана — https://www.nalog.gov.ru/rn77/service/egrip2/access_order/ — массовый доступ 150 тыс. ₽ в год, поштучно бесплатно — A
- Открытые данные ФНС — ФНС России, дата не указана — https://www.nalog.gov.ru/opendata/ — бесплатные наборы данных с разрешением коммерческого использования — A
- Checko API — Checko, 2026 — https://checko.ru/integration/api — реквизиты, контакты, отчётность, госзакупки — A (описание вендора)
- Условия использования API hh.ru — HeadHunter, действующая редакция — https://dev.hh.ru/admin/developer_agreement — данные только для целей найма — A
- API Поиска по организациям — Яндекс, дата не указана — https://yandex.ru/dev/commercial/doc/ru/concepts/geosearch — цены, запрет сохранять данные — A

## Право

- 38-ФЗ «О рекламе», статья 18 — ФС РФ / КонсультантПлюс, редакция 04.08.2026 — https://www.consultant.ru/document/cons_doc_LAW_58968/f892dec1383709792452f18d36e7043306e2be0a/ — предварительное согласие, бремя доказывания, немедленное прекращение — A
- Решение АС Свердловской области по делу А60-12264/2023 — арбитражный суд, 16.05.2023 — https://sudact.ru/arbitral/doc/vzXzNbGegyVq/ — неперсонализированное письмо на email признано рекламой — A
- Решение АС г. Москвы по делу А40-128919/2023 — арбитражный суд, 08.09.2023 — https://sudact.ru/arbitral/doc/rLbVY9PKvpJw/ — штраф 100 тыс. ₽ за email-рекламу без согласия оставлен в силе — A
- КоАП РФ, статьи 13.11 и 14.3 — ФС РФ, редакция 26.07.2026 — https://www.consultant.ru/document/cons_doc_LAW_34661/ — штрафы за нарушения в сфере персональных данных и рекламы — A
- 152-ФЗ, статья 10.1 — ФС РФ, действующая редакция — https://www.consultant.ru/document/cons_doc_LAW_61801/591acc70f577873c1ee54765eda110b7a0271eaf/ — законность обработки общедоступных персональных данных доказывает обработчик — A
- Directive 2002/58/EC, Article 13 — ЕС, редакция 2009/136/EC — https://www.legislation.gov.uk/eudr/2002/58/article/13 — согласие и soft opt-in; правила для юрлиц задают государства — A
- GDPR, Article 21 — ЕС, 2016 — https://gdpr-info.eu/art-21-gdpr/ — право возражения против direct marketing — A
- CNIL: B to B — CNIL, дата не указана — https://www.cnil.fr/fr/cnil-direct/question/2002 — во Франции B2B-письма без согласия допустимы при связи с должностью и праве возразить — A
- UWG § 7 — Bundestag / BMJ, действующая редакция — https://www.gesetze-im-internet.de/uwg_2004/__7.html — email-реклама требует предварительного согласия и в B2B — A
- CAN-SPAM Act: A Compliance Guide for Business — FTC, индексация штрафа 17.01.2025 — https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business — B2B охвачен законом, отказ за 10 рабочих дней, штраф до $53 088 за письмо — A

## Бенчмарки, текст и цепочки

- What are B2B cold email response rates? 2026 study — Belkins, обновлено 26.06.2026 — https://belkins.io/blog/cold-email-response-rates — 0,45% ответов на отправленное письмо, смена знаменателя, 1 200+ встреч на 7,5 млн писем — A
- Sales follow-up statistics in B2B: 2026 study — Belkins, обновлено 26.06.2026 — https://belkins.io/blog/sales-follow-up-statistics — 41,4% ответов на первое письмо, шаг 3 — пик встреч — A
- The State of Cold Email 2026 — Smartlead, первое полугодие 2026 — https://www.smartlead.ai/benchmarks/state-of-cold-email — медиана 1 ответ на 135 контактов — C
- Cold Email Benchmark Report 2026 — Instantly, 2026 (данные 2025) — https://instantly.ai/cold-email-benchmark-report-2026 — 3,43% ответов, верхний дециль от 10,7% — C
- I Analyzed 53M Cold Emails — Saleshandy, 2026 — https://www.saleshandy.com/blog/cold-email-statistics/ — мягкий CTA +78% позитивных ответов, follow-up 44% позитивных — C
- State of Email Outreach 2026 — Hunter, 2026 (данные 2025) — https://hunter.io/the-state-of-cold-email — трекинг открытий 4,4% против 7,4% без него, сегменты, три письма, отношение ЛПР к AI-текстам — C
- What Is a Realistic Cold Email Reply Rate? — ReplyLead, снимок 12.08.2026 — https://replylead.com/realistic-cold-email-reply-rate.html — как знаменатель и агрегация меняют цифру — C
- Does cold email even work any more? — Gong × Outbound Squad, дата не указана — https://www.gong.io/blog/does-cold-email-even-work-any-more-heres-what-the-data-says — 344 письма на встречу, питч до −57% ответов — C
- 4 data-backed ways to increase your email reply rate — Gong Labs, 07.07.2023 — https://www.gong.io/blog/4-data-backed-ways-to-increase-your-email-reply-rate-and-book-that-meeting — company-specific тема ×3 ответов у директоров, отраслевая персонализация +88% — C
- This surprising cold email CTA — Gong Labs, около 2020–2021 — https://www.gong.io/blog/this-surprising-cold-email-cta-will-help-you-book-a-lot-more-meetings — interest CTA лучший на холодной стадии — C

## ИИ и сигналы

- SDR Models, Motions & Metrics: 2025 — The Bridge Group, 06.02.2025 — https://www.bridgegroupinc.com/research/2025-sdr-models-metrics-report-the-bridge-group — AI SDR у 1% компаний — A
- 11x has been claiming customers it doesn’t have — TechCrunch, 24.03.2025 — https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have/ — провал автономного AI SDR — C
- AI vs Human Cold Emails — Saleshandy, 2026 — https://www.saleshandy.com/blog/ai-vs-human-cold-emails/ — AI 4,1%, человек 10,4%, гибрид 14,7% — C
- AI vs Human Recruiting Outreach — Pin, 2026 — https://www.pin.com/blog/ai-vs-human-recruiting-outreach-study/ — AI-письма 4,97% против 12,6% у написанных вручную — C
- vercel-labs/lead-agent — Vercel, 2025 — https://github.com/vercel-labs/lead-agent — пайплайн исследование → квалификация → черновик → одобрение человеком — A
- How to Measure Signal-Based Outreach — Unify, 2026 — https://www.unifygtm.com/explore/signal-based-outreach-metrics — сигнальные сценарии +73% ответов, классы ответов — C/D
- UserGems: New Hires Signal — UserGems, дата не указана — https://www.usergems.com/product/new-hires-signal — новые руководители в 2,5 раза открытее в первые 3 месяца — C

## Кейсы и Telegram

- Холодные email рассылки в B2B ещё как работают (EdBuro) — Respondo, 17.07.2023 — https://vc.ru/marketing/761532-holodnye-email-rassylki-v-b2b-eshe-kak-rabotayut-poprobovali-i-srazu-poluchili-28-celevyh-lidov — полная воронка от писем до договоров — C
- Холодный аутрич в B2B: как мы довели клиента до отчаяния (Sherpa Robotics) — Respondo, 14.05.2025 — https://vc.ru/id128425/1982841-kak-proval-holodnoj-b2b-rassylki-privel-k-uspehu-klienta — провал и исправление через сигнал и адресата — C
- Инфраструктура холодной рассылки для узкого B2B — Сайткрафт, 13.08.2026 — https://habr.com/ru/articles/1069906/ — воронка до квалифицированных лидов, лимиты и домены — C
- Каталог кейсов Coldy — Coldy, 2023–2026 — https://coldy.ai/case-studies — кейсы российских агентств с сигналами потребности — C/D
- EMAILMATRIX про маркетинг — EMAILMATRIX, 2022–2026 — https://t.me/emailmatrix — принципы email-маркетинга по своей базе — E
- ИИ × CRM | Дмитрий Банных — Inbox Marketing, 2018–2026 — https://t.me/emailcompetitors — две эпохи канала, ИИ в процессах агентства — E
