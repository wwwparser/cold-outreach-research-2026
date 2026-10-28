# Источники

_Дата доступа ко всем источникам — 2026-09-15. Уровни: A — официальная документация / закон / суд / большое first-party исследование; B — несколько независимых источников; C — кейс или вендорский датасет с методикой; D — мнение; E — anecdotal. Цитаты и контекст — в доказательных конспектах `data/research/*.md`._

## Ключевые источники

| Название | URL | Автор / организация | Дата публикации | Тип | Уровень | Что подтверждает |
|---|---|---|---|---|---|---|
| Email sender guidelines | https://support.google.com/a/answer/81126 | Google | живой документ (требования с 02.2024) | официальная документация | A | требования ко всем и к bulk-отправителям; запрет фейковых Re:/Fwd:, покупки адресов; Google не отслеживает open rate |
| Email sender guidelines FAQ | https://support.google.com/mail/answer/14229414 | Google | живой документ (enforcement с 11.2025) | официальная документация | A | спам <0,1% / 0,3%; bulk ≈5 000/сутки навсегда; отказы с 11.2025; one-click только для маркетинговых писем |
| Gmail sending limits in Google Workspace | https://support.google.com/a/answer/166852 | Google | обновлено 2026-09-10 | официальная документация | A | 2 000 писем/сутки, trial 500 |
| Sender Requirements & Recommendations | https://senders.yahooinc.com/best-practices/ | Yahoo | живой документ | официальная документация | A | SPF+DKIM, DMARC p=none, спам <0,3%, отписка за 2 дня |
| Outlook’s Requirements for High-Volume Senders | https://techcommunity.microsoft.com/blog/microsoft-defender-for-office-365-blog/strengthening-email-ecosystem-outlook%E2%80%99s-new-requirements-for%C2%A0high%E2%80%90volume-senders/4399730 | Microsoft | 2025-04-02 (обн. 2025-04-30) | официальный блог | A | SPF/DKIM/DMARC для 5 000+/сутки с 05.05.2025 |
| Exchange Online limits / Tenant Outbound Email Limits | https://learn.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits | Microsoft | 2026-04-07; блог TERRL обн. 2026-08-13 | официальная документация | A | 10 000 получателей/сутки на ящик; квоты новых тенантов с 14.09.2026 |
| RFC 9989 (DMARCbis) | https://datatracker.ietf.org/doc/draft-ietf-dmarc-dmarcbis/ | IETF | 2026-05-20 | стандарт | A | отмена RFC 7489, удаление pct, тег t |
| RFC 8058 One-Click Unsubscribe | https://www.rfc-editor.org/rfc/rfc8058.html | IETF | 2017-01 | стандарт | A | механизм List-Unsubscribe-Post |
| M3AAWG Position on Cold Email | https://www.m3aawg.org/M3AAWGPositionOnColdEmail | M3AAWG | 2025-11 | отраслевая позиция | A | lookalike-домены, множество ящиков, обход лимитов, имитация engagement — недопустимы |
| M3AAWG Sender Best Common Practices v4.0 | https://www.m3aawg.org/sites/default/files/doc_files/m3aawg-sender-best-common-practices-aug-27-2026.pdf | M3AAWG | 2026-08 | отраслевой BCP | A | прогрев ~6 недель реальной почтой; «Artificial warming practices are not recommended and may be illegal»; поддомен вместо cousin-домена |
| Spamhaus’ take on Cold Emailing | https://www.spamhaus.org/resource-hub/spam/spamhaus-take-on-cold-emailing-aka-spam/ | Spamhaus | 2025 | позиция оператора блоклистов | A/D | throwaway-домены, warm-up-инструменты, листинг за ловушки |
| Технические и административные требования (рассылки) | https://help.mail.ru/developers/mailing_rules/technical/ | VK (Mail) | не указана | официальная документация | A | opt-in, Precedence: bulk, пороги жалоб 1,1%→0,3% |
| Отправить много писем (Яндекс 360 для бизнеса) | https://yandex.ru/support/yandex-360/business/mail/ru/web/letter/create/send-many-letters | Яндекс | не указана | официальная документация | A | лимиты 300/1 000/10 000/50; блокировка шаблонных КП раньше лимита; требования к честным рассылкам |
| Общие условия использования сервисов Яндекс 360 | https://yandex.ru/legal/360_termsofuse/ru/ | Яндекс | 2026-09-14 | оферта | A | запрет массовых рассылок (п. 1.19) и обхода ограничений |
| Правила Яндекс Рассылок | https://yandex.ru/support/yandex-360/business/send/ru/rules | Яндекс | не указана | официальная документация | A | запрет писем без согласия и на ролевые адреса |
| Антиспам-политика Unisender | https://www.unisender.com/ru/antispam/ | Unisender | не указана | AUP | A | double opt-in для КП; запрет открытых источников |
| 38-ФЗ «О рекламе», ст. 18 | https://www.consultant.ru/document/cons_doc_LAW_58968/f892dec1383709792452f18d36e7043306e2be0a/ | ФС РФ / КонсультантПлюс | ред. 04.08.2026 | закон | A | предварительное согласие, бремя доказывания, немедленное прекращение |
| Решение АС Свердловской обл. по делу А60-12264/2023 | https://sudact.ru/arbitral/doc/vzXzNbGegyVq/ | Арбитражный суд | 2023-05-16 | суд | A | неперсонализированное письмо на email — реклама |
| Решение АС г. Москвы по делу А40-128919/2023 | https://sudact.ru/arbitral/doc/rLbVY9PKvpJw/ | Арбитражный суд | 2023-09-08 | суд | A | штраф 100 тыс. ₽ за email-рекламу без согласия оставлен в силе |
| КоАП РФ ст. 13.11 и 14.3 | https://www.consultant.ru/document/cons_doc_LAW_34661/ | ФС РФ | ред. 26.07.2026 | закон | A | штрафы за ПДн (с 30.05.2025) и рекламу |
| 152-ФЗ ст. 15 и 10.1 | https://www.consultant.ru/document/cons_doc_LAW_61801/591acc70f577873c1ee54765eda110b7a0271eaf/ | ФС РФ | действующая | закон | A | согласие для продвижения; доказывание законности обработки общедоступных ПДн |
| Directive 2002/58/EC, Art. 13 | https://www.legislation.gov.uk/eudr/2002/58/article/13 | EU | ред. 2009/136/EC | закон | A | согласие / soft opt-in; юрлица — на усмотрение государств |
| GDPR Art. 6, 14, 21, Recital 47 | https://gdpr-info.eu/art-21-gdpr/ | EU | 2016 | закон | A | законный интерес, уведомление об источнике, право возражения |
| CNIL: B to B prospection | https://www.cnil.fr/fr/cnil-direct/question/2002 | CNIL | не указана | регулятор | A | B2B без согласия при связи с должностью и праве возразить |
| UWG § 7 | https://www.gesetze-im-internet.de/uwg_2004/__7.html | Bundestag / BMJ | действующая | закон | A | согласие на email-рекламу и в B2B |
| CAN-SPAM Act: A Compliance Guide for Business | https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business | FTC | индексация штрафа 17.01.2025 | регулятор | A | B2B охвачен; opt-out ≤10 рабочих дней; до $53,088 за письмо |
| B2B cold email response rates (2026 study) | https://belkins.io/blog/cold-email-response-rates | Belkins | обн. 2026-06-26 | first-party исследование | A | 0,45% reply на отправленное; смена знаменателя; 1 200+ встреч на 7,5 млн писем |
| Sales follow-up statistics (2026 study) | https://belkins.io/blog/sales-follow-up-statistics | Belkins | обн. 2026-06-26 | first-party исследование | A | 41,4% ответов на 1-е письмо; шаг 3 — пик встреч |
| The State of Cold Email 2026 | https://www.smartlead.ai/benchmarks/state-of-cold-email | Smartlead | H1 2026 | вендорский отчёт | C | медиана 1 ответ на 135 контактов |
| Cold Email Benchmark Report 2026 | https://instantly.ai/cold-email-benchmark-report-2026 | Instantly | 2026 (данные 2025) | вендорский отчёт | C | 3,43%; верхний дециль ≥10,7%; 58% ответов на шаг 1 |
| I Analyzed 53M Cold Emails | https://www.saleshandy.com/blog/cold-email-statistics/ | Saleshandy | 2026 | вендорский отчёт | C | мягкий CTA +78% позитивных; follow-up 44% позитивных |
| State of Email Outreach 2026 | https://hunter.io/the-state-of-cold-email | Hunter | 2026 (данные 2025) | вендорский отчёт + опрос | C | трекинг 4,4% против 7,4%; сегменты; 3 письма; 69% ЛПР против AI-текста |
| What Is a Realistic Cold Email Reply Rate? | https://replylead.com/realistic-cold-email-reply-rate.html | ReplyLead | снимок 2026-08-12 | кейс с методологией | C | влияние знаменателя и агрегации |
| Does cold email even work any more? | https://www.gong.io/blog/does-cold-email-even-work-any-more-heres-what-the-data-says | Gong × Outbound Squad | не указана | вендорские данные | C | 344 письма на встречу; питч −57% |
| 4 data-backed ways to increase reply rate | https://www.gong.io/blog/4-data-backed-ways-to-increase-your-email-reply-rate-and-book-that-meeting | Gong Labs | 2023-07-07 | вендорские данные | C | company-specific ×3 у директоров; отраслевая +88% |
| This surprising cold email CTA | https://www.gong.io/blog/this-surprising-cold-email-cta-will-help-you-book-a-lot-more-meetings | Gong Labs | ~2020–2021 | вендорские данные | C | interest CTA лучший на холодной стадии |
| Email Client Market Share | https://www.litmus.com/email-client-market-share/ | Litmus | отчёт за 07.2026 | отраслевая телеметрия | A | MPP ~55–60% открытий |
| SDR Models, Motions & Metrics: 2025 | https://www.bridgegroupinc.com/research/2025-sdr-models-metrics-report-the-bridge-group | The Bridge Group | 2025-02-06 | опрос 351 компании | A | AI SDR у 1% компаний; квоты встреч |
| 11x has been claiming customers it doesn’t have | https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have/ | TechCrunch | 2025-03-24 | расследование | C | провал автономного AI SDR |
| AI vs Human Cold Emails | https://www.saleshandy.com/blog/ai-vs-human-cold-emails/ | Saleshandy | 2026 | вендорский эксперимент | C | AI 4,1% / человек 10,4% / гибрид 14,7% |
| vercel-labs/lead-agent | https://github.com/vercel-labs/lead-agent | Vercel | 2025 | открытый код | A | пайплайн research → qualify → draft → approve в Slack |
| Порядок доступа к ЕГРЮЛ и ЕГРИП | https://www.nalog.gov.ru/rn77/service/egrip2/access_order/ | ФНС России | не указана | официальная документация | A | 150 тыс. ₽/год массовый доступ; поштучно бесплатно |
| Условия использования API hh.ru | https://dev.hh.ru/admin/developer_agreement | HeadHunter | действующая | условия | A | данные только для целей найма |
| Кейсы Respondo / Coldy (подборка) | https://coldy.ai/case-studies | Coldy, Respondo | 2023–2026 | вендоры о клиентах | C/D | сигнал потребности, «кто отвечает за…», домены-двойники и прогрев в практике РФ |


## Полный список (377 уникальных URL, сгруппировано по доказательным конспектам)


### Право и compliance (РФ, ЕС, Франция, Германия, США) (60)

| Название | URL | Организация / автор | Дата публикации | Дата доступа | Тип | Что подтверждает |
|---|---|---|---|---|---|---|
| 38-ФЗ «О рекламе», ст. 18 | https://www.consultant.ru/document/cons_doc_LAW_58968/f892dec1383709792452f18d36e7043306e2be0a/ | ФС РФ / КонсультантПлюс | ред. 04.08.2026 | 2026-09-15 | Закон (A) | Согласие, бремя доказывания, прекращение, автоматическая рассылка |
| 38-ФЗ, ст. 18.1 | https://www.consultant.ru/document/cons_doc_LAW_58968/2c4537e4796f6ff8b2736ed1b0d4fef08e14458e/ | ФС РФ / КонсультантПлюс | ред. 04.08.2026 | 2026-09-15 | Закон (A) | Пометка «реклама», erid |
| 38-ФЗ, ст. 3 | https://legalacts.ru/doc/federalnyi-zakon-ot-13032006-n-38-fz-o/glava-1/statja-3/ | ФС РФ (зеркало) | действующая | 2026-09-15 | Закон (A) | Понятие рекламы |
| 38-ФЗ, перечень редакций | https://base.garant.ru/12145525/ | ГАРАНТ | изм. по 04.08.2026 | 2026-09-15 | Правовая база (A) | Актуальность редакции |
| Постановление Пленума ВАС № 58, п. 15 | https://www.consultant.ru/document/cons_doc_LAW_137349/ | ВАС РФ | 08.10.2012 | 2026-09-15 | Судебное разъяснение (A) | Email-адресат, форма согласия |
| Кировское УФАС, ответы на вопросы | http://kirov.new.fas.gov.ru/p/questions/6194 | ФАС России | 29.04.2020 | 2026-09-15 | Разъяснение (A) | Галочка в форме — ненадлежащее согласие |
| Письмо ФАС АЦ/4624 | https://www.consultant.ru/document/cons_doc_LAW_68032/260ba67a24178ef0b16e0a7b6817cb0c0ce71325/ | ФАС России | 05.04.2007, утратило силу | 2026-09-15 | Разъяснение (A, историческое) | Неопределённый круг лиц |
| Письмо ФАС АД/45557/18 | https://www.garant.ru/products/ipo/prime/doc/71872842/ | ФАС России | 20.06.2018, утратило силу | 2026-09-15 | Разъяснение (A, историческое) | Адресный список не исключает рекламу |
| ФАС: статус разъяснения 2018 | https://fas.gov.ru/documents/640008 | ФАС России | отменено 02.12.2022 | 2026-09-15 | Регулятор (A) | Недействующий статус |
| Письмо ФАС МШ/109196-ПР/22 | https://legalacts.ru/doc/pismo-fas-rossii-ot-02122022-n-msh109196-pr22-o-napravlenii/ | ФАС России | 02.12.2022 | 2026-09-15 | Разъяснение (A) | Перечень отменённых разъяснений |
| АС Свердловской обл., А60-12264/2023 | https://sudact.ru/arbitral/doc/vzXzNbGegyVq/ | Арбитражный суд | 16.05.2023 | 2026-09-15 | Суд (A) | Неперсонализированное email — реклама |
| АС г. Москвы, А40-128919/2023 | https://sudact.ru/arbitral/doc/rLbVY9PKvpJw/ | Арбитражный суд | 08.09.2023 | 2026-09-15 | Суд (A) | Штраф 100 тыс. руб. за email без согласия |
| Московское УФАС, дело 077/05/18-15526/2020 | https://www.tenderguru.ru/fas/3471 | ФАС (агрегатор) | 16.12.2020 | 2026-09-15 | Решение УФАС (A/C) | Критерий указания получателя |
| КоАП РФ ст. 14.3 | https://www.consultant.ru/document/cons_doc_LAW_34661/2d50fc1c4013ea9ab20b8b2666c1650b1dc4c982/ | ФС РФ | ред. 26.07.2026 | 2026-09-15 | Закон (A) | Штрафы за рекламу |
| КоАП РФ ст. 13.11 | https://www.consultant.ru/document/cons_doc_LAW_34661/1f421640c6775ff67079ebde06a7d2f6d17b96db/ | ФС РФ | ред. 26.07.2026 | 2026-09-15 | Закон (A) | Штрафы за ПДн |
| КоАП 13.11, ГАРАНТ (дата изменений) | https://base.garant.ru/12125267/b369434ee740927935cc6f0a04242543/ | ГАРАНТ | с 30.05.2025 (420-ФЗ) | 2026-09-15 | Правовая база (A) | Дата вступления новых штрафов |
| 152-ФЗ ст. 3 | https://sudact.ru/law/federalnyi-zakon-ot-27072006-n-152-fz-o/glava-1/statia-3/ | ФС РФ (зеркало) | действующая | 2026-09-15 | Закон (A) | Понятие ПДн |
| 152-ФЗ ст. 6 | https://sudact.ru/law/federalnyi-zakon-ot-27072006-n-152-fz-o/glava-2/statia-6/ | ФС РФ (зеркало) | действующая | 2026-09-15 | Закон (A) | Законные интересы оператора |
| 152-ФЗ ст. 10.1 | https://www.consultant.ru/document/cons_doc_LAW_61801/591acc70f577873c1ee54765eda110b7a0271eaf/ | ФС РФ / КонсультантПлюс | действующая | 2026-09-15 | Закон (A) | Общедоступные ПДн, бремя доказывания |
| 152-ФЗ ст. 15 | https://sudact.ru/law/federalnyi-zakon-ot-27072006-n-152-fz-o/glava-3/statia-15/ | ФС РФ (зеркало) | действующая | 2026-09-15 | Закон (A) | Согласие для продвижения товаров |
| 152-ФЗ ст. 18 | https://sudact.ru/law/federalnyi-zakon-ot-27072006-n-152-fz-o/glava-4/statia-18/ | ФС РФ (зеркало) | действующая | 2026-09-15 | Закон (A) | Уведомление при получении данных не от субъекта |
| ГАРАНТ: email и ПДн | https://www.garant.ru/consult/business/1723024/ | ГАРАНТ.РУ | н/д | 2026-09-15 | Консультация (B/C) | Позиция РКН и судов (А40-139096/2022) |
| ГАРАНТ: рекламные рассылки и ПДн | https://www.garant.ru/article/1523544/ | ГАРАНТ.РУ | н/д | 2026-09-15 | Статья (D) | ФИО в письме, практика УФАС |
| «ЭЖ»: Руководство ФАС и РКН | https://www.eg-online.ru/article/476959/ | «Экономика и жизнь» | н/д | 2026-09-15 | Статья (D) | Email по клиентской базе, маркировка |
| eLama: маркировка 2026 | https://elama.ru/blog/yurist-pro-nyuansy-zakona-omarkirovke-reklamy-obotvetstvennosti-samoreklame-islozhnyh-formatah/ | eLama | 2026 | 2026-09-15 | Статья (D, фрагмент в выдаче) | Email вне маркировки по разъяснениям 2023 года |
| Контур.Компас | https://kontur.ru/compass/spravka-compass/44380-privlechenie_klientov_pismami | СКБ Контур | н/д | 2026-09-15 | Статья (D) | Кейс СПб УФАС B2B, письмо ФАС ДФ/98054/19 |
| АГ: ВС о согласии за скидку | https://www.advgazeta.ru/novosti/verkhovnyy-sud-priznal-zakonnym-poluchenie-soglasiya-na-reklamnuyu-rassylku-v-obmen-na-skidku/ | «Адвокатская газета» | 2026 | 2026-09-15 | Новость (C) | Определение ВС № 309-ЭС26-2103 |
| ФАС: что признаётся рекламой | https://fas.gov.ru/news/32269 | ФАС России | 2022 | 2026-09-15 | Регулятор (A) | Контекст ст. 18.1 |
| Directive 2002/58/EC, Art. 13 | https://www.legislation.gov.uk/eudr/2002/58/article/13 | EU (зеркало legislation.gov.uk) | в ред. 2009/136/EC, снимок на 31.12.2020 | 2026-09-15 | Закон (A) | Согласие, soft opt-in, юрлица |
| OEIL 2017/0003(COD) | https://oeil.secure.europarl.europa.eu/oeil/popups/ficheprocedure.do?reference=2017/0003(COD | European Parliament | отозван 06.10.2025 | 2026-09-15 | Официальный реестр (A) | Отзыв ePrivacy Regulation |
| Hunton: отзыв ePrivacy Regulation | https://www.hunton.com/privacy-and-cybersecurity-law-blog/european-commission-withdraws-eprivacy-regulation-and-ai-liability-directive-proposals | Hunton Andrews Kurth | 02.2025 | 2026-09-15 | Статья (D) | Директива продолжает действовать |
| EDRi | https://edri.org/our-work/the-eprivacy-regulation-proposal-has-been-withdrawn-but-the-fight-for-your-privacy-is-far-from-over/ | EDRi | 2025 | 2026-09-15 | Статья (D) | Отзыв проекта |
| Bird & Bird: Digital Omnibus | https://www.twobirds.com/en/capabilities/practices/digital-rights-and-assets/european-digital-strategy-developments/privacy-and-data-protection/eprivacy-regulation | Bird & Bird | на 19.02.2026 | 2026-09-15 | Статья (D) | Статус Omnibus |
| GDPR Art. 6 | https://gdpr-info.eu/art-6-gdpr/ | EU (зеркало) | OJ L 119, 04.05.2016 | 2026-09-15 | Закон (A) | Законный интерес |
| GDPR Recital 47 | https://gdpr-info.eu/recitals/no-47/ | EU (зеркало) | 2016 | 2026-09-15 | Закон (A) | Direct marketing как законный интерес |
| GDPR Art. 14 | https://gdpr-info.eu/art-14-gdpr/ | EU (зеркало) | 2016 | 2026-09-15 | Закон (A) | Информирование при сборе не у субъекта |
| GDPR Art. 21 | https://gdpr-info.eu/art-21-gdpr/ | EU (зеркало) | 2016 | 2026-09-15 | Закон (A) | Право возражения |
| EDPB Guidelines 1/2024 | https://www.edpb.europa.eu/public-consultations/guidelines-12024-on-processing-of-personal-data-based-on-article-61f-gdpr_en | EDPB | 10.2024 | 2026-09-15 | Регулятор (A, только факт) | Наличие руководства |
| CNIL Direct: B to B | https://www.cnil.fr/fr/cnil-direct/question/2002 | CNIL | н/д | 2026-09-15 | Регулятор (A) | B2B opt-out при связи с профессией |
| CNIL: opt-in / opt-out | https://www.cnil.fr/fr/cnil-direct/question/opt-opt-out-ca-veut-dire-quoi | CNIL | н/д | 2026-09-15 | Регулятор (A) | Определения |
| CNIL: la prospection commerciale | https://www.cnil.fr/fr/la-prospection-commerciale | CNIL | 2026 | 2026-09-15 | Регулятор (A) | Частные лица — согласие, профессионалы — возражение |
| CNIL: prospection par courrier électronique | https://www.cnil.fr/fr/la-prospection-commerciale-par-courrier-electronique-sms-mms-et-automate-dappel | CNIL | 10.06.2026 | 2026-09-15 | Регулятор (A) | Общие правила email |
| Village de la Justice | https://www.village-justice.com/articles/prospection-commerciale-par-mail-btob-peut-vraiment-contenter-opt-out,46443.html | Village de la Justice (автор-юрист) | н/д | 2026-09-15 | Статья (D) | B2B-доктрина CNIL не в Директиве |
| UWG § 7 | https://www.gesetze-im-internet.de/uwg_2004/__7.html | Bundestag / BMJ | действующая | 2026-09-15 | Закон (A) | Согласие на email, исключение для клиентов |
| UWG § 8 | https://www.gesetze-im-internet.de/uwg_2004/__8.html | Bundestag / BMJ | действующая | 2026-09-15 | Закон (A) | Требования о прекращении, кто их заявляет |
| UWG § 20 | https://www.gesetze-im-internet.de/uwg_2004/__20.html | Bundestag / BMJ | действующая | 2026-09-15 | Закон (A) | Штрафы только за телефон |
| BGH I ZR 218/07 (dejure) | https://dejure.org/dienste/vernetzung/rechtsprechung?Gericht=BGH&Datum=20.05.2009&Aktenzeichen=I%20ZR%20218/07 | BGH (аннотация) | 20.05.2009 | 2026-09-15 | Суд, вторичный пересказ (B) | Одно письмо без согласия |
| windweiss.de | https://www.windweiss.de/aktuelles/bgh-urteil-email-werbung-abmahnung/ | Kanzlei Windweiss | 2025 | 2026-09-15 | Статья (D) | Обзор практики BGH, Abmahnung |
| Legalano: BGH I ZR 208/12 | https://legalano.com/de/blog/bgh-i-zr-208-12-empfehlungs-email/ | Legalano | н/д | 2026-09-15 | Статья (D/B) | Empfehlungs-E-Mail |
| openjur: BGH VI ZR 225/17 | https://openjur.de/u/2111609.html | BGH (зеркало; фрагмент в выдаче) | 10.07.2018 | 2026-09-15 | Суд (B) | Реклама в сервисном письме |
| vzbv: BGH VI ZR 109/23 | https://www.vzbv.de/urteile/zum-dsgvo-schadensersatz-fuer-werbe-e-mails | vzbv | 28.01.2025 | 2026-09-15 | Пересказ решения (B) | Компенсация по GDPR без доказанного ущерба не присуждается |
| 15 U.S.C. § 7702 | https://www.law.cornell.edu/uscode/text/15/7702 | US Congress (LII) | действующая | 2026-09-15 | Закон (A) | Определение коммерческого письма |
| 15 U.S.C. § 7704 | https://www.law.cornell.edu/uscode/text/15/7704 | US Congress (LII) | действующая | 2026-09-15 | Закон (A) | Тема, заголовки, отягчающие нарушения |
| 15 U.S.C. § 7706 | https://www.law.cornell.edu/uscode/text/15/7706 | US Congress (LII) | действующая | 2026-09-15 | Закон (A) | Иски штатов, $250 за письмо |
| 15 U.S.C. § 7707 | https://www.law.cornell.edu/uscode/text/15/7707 | US Congress (LII) | действующая | 2026-09-15 | Закон (A) | Вытеснение законов штатов |
| 16 CFR § 1.98 | https://www.law.cornell.edu/cfr/text/16/1.98 | FTC (LII) | штрафы после 17.01.2025 | 2026-09-15 | Регламент (A) | $53,088 |
| 16 CFR § 316.3 | https://www.law.cornell.edu/cfr/text/16/316.3 | FTC (LII) | действующая | 2026-09-15 | Регламент (A) | Primary purpose |
| Federal Register 2025-01361 | https://www.federalregister.gov/documents/2025/01/17/2025-01361/adjustments-to-civil-penalty-amounts | FTC | 17.01.2025 | 2026-09-15 | Официальная публикация (A) | Индексация 2025 года |
| Пресс-релиз FTC об индексации 2025 | https://www.ftc.gov/news-events/news/press-releases/2025/02/ftc-publishes-inflation-adjusted-civil-penalty-amounts-2025 | FTC | 02.2025 | 2026-09-15 | Регулятор (A) | $51,744 → $53,088 |
| Cal. B&P Code § 17529.5 | https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=17529.5 | California Legislature | Stats. 2005, Ch. 247 | 2026-09-15 | Закон штата (A) | $1,000 за письмо при обмане |

### Deliverability: официальные требования, протоколы, warm-up, объёмы, база (36)

| Название | URL | Организация / автор | Дата публикации | Дата доступа | Тип | Что подтверждает |
|---|---|---|---|---|---|---|
| Email sender guidelines | https://support.google.com/a/answer/81126?hl=en | Google | не указана | 2026-09-15 | официальная документация (A) | требования для всех и для 5000+, спам 0,1/0,3%, PTR, TLS, DKIM ≥1024, рост объёма, запреты по контенту, квоты по домену и IP |
| Email sender guidelines FAQ | https://support.google.com/mail/answer/14229414?hl=en | Google | не указана (enforcement с ноября 2025) | 2026-09-15 | официальная документация (A) | определение bulk, постоянный статус, коды ошибок, one-click только для promo, 48 часов, alignment, новые домены |
| Postmaster Tools dashboards | https://support.google.com/mail/answer/14668346?hl=en | Google | не указана | 2026-09-15 | официальная документация (A) | Compliance status v2, как считается спам-рейт, deliverability analysis |
| Sender requirements & Postmaster Tools FAQ | https://knowledge.workspace.google.com/admin/gmail/sender-requirements-and-postmaster-tools-faq | Google | не указана | 2026-09-15 | официальная документация (A) | Postmaster для проверки соответствия, DMARC p=none |
| Gmail sending limits in Google Workspace | https://support.google.com/a/answer/166852?hl=en | Google | обновл. 2026-09-10 | 2026-09-15 | официальная документация (A) | 2000/сутки, trial 500, получатели в сутки, $100 и 75 дней |
| Spam and abuse policy in Gmail | https://knowledge.workspace.google.com/admin/gmail/spam-and-abuse-policy-in-gmail | Google | обновл. 2026-09-10 | 2026-09-15 | политика (A) | блокировка пользователя или домена за спам |
| Gmail Program Policies | https://www.google.com/gmail/about/policy/ | Google | не указана | 2026-09-15 | политика (A) | запрет unsolicited commercial mail, multiple accounts, автоматизации интерфейса |
| Google Cloud Acceptable Use Policy (RU-версия для Workspace: workspace.google.com/terms/use_policy/) | https://cloud.google.com/terms/aup | Google | не указана | 2026-09-15 | политика (A) | запрет спама, обхода ограничений, «evade filtering capabilities» |
| Sender FAQs | https://senders.yahooinc.com/faqs/ | Yahoo | не указана | 2026-09-15 | официальная документация (A) | bulk-порог не раскрыт, DKIM 1024/2048, CFL, всплески, факторы репутации |
| Strengthening Email Ecosystem: Outlook’s Requirements for High-Volume Senders | https://techcommunity.microsoft.com/blog/microsoft-defender-for-office-365-blog/strengthening-email-ecosystem-outlook%E2%80%99s-new-requirements-for%C2%A0high%E2%80%90volume-senders/4399730 | Microsoft | 2025-04-02, обновл. 2025-04-30 | 2026-09-15 | официальный блог (A) | 5000+/сутки: SPF, DKIM, DMARC; 5.7.515; 10 lookups; чистка списков |
| Outlook.com Postmaster | https://substrate.office.com/ip-domain-management-snds/postmaster | Microsoft | не указана | 2026-09-15 | официальная документация (A) | с 05.05.2025 Junk, отказ «shortly» |
| Policies, Practices, and Guidelines | https://substrate.office.com/ip-domain-management-snds/Postmaster/Policies | Microsoft | не указана | 2026-09-15 | политика (A) | NDR-правила, rDNS, запрет namespace mining, DMARC (рекомендован p=reject) |
| Services for Senders and ISPs | https://substrate.office.com/ip-domain-management-snds/Postmaster/Services | Microsoft | не указана | 2026-09-15 | официальная документация (A) | SNDS, JMRP (72 часа) |
| Exchange Online limits | https://learn.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits | Microsoft | 2026-04-07 | 2026-09-15 | официальная документация (A) | RRL 10 000, 30 сообщений/мин, TERRL, onmicrosoft 100, bulk — через сторонних провайдеров |
| Introducing Exchange Online Tenant Outbound Email Limits | https://techcommunity.microsoft.com/blog/exchange/introducing-exchange-online-tenant-outbound-email-limits/4372797 | Microsoft | февраль 2025, обновл. 2026-08-13 | 2026-09-15 | официальный блог (A) | формула TERRL, trial 500, квоты новых тенантов с 14.09.2026 |
| Exchange Online to introduce External Recipient Rate Limit | https://techcommunity.microsoft.com/blog/exchange/exchange-online-to-introduce-external-recipient-rate-limit/4114733 | Microsoft | апрель 2024, пометка об отмене 2026-01-06 | 2026-09-15 | официальный блог (A) | исходный план ERR 2000; счёт по получателям |
| Exchange Online canceling the Mailbox External Recipient Rate Limit | https://techcommunity.microsoft.com/blog/exchange/exchange-online-canceling-the-mailbox-external-recipient-rate-limit/4483498 | Microsoft | январь 2026 | 2026-09-15 | официальный блог (A) | ERR отменён, RRL и TERRL без изменений |
| Технические и административные требования | https://help.mail.ru/developers/mailing_rules/technical/ | VK (Mail) | не указана | 2026-09-15 | официальная документация (A) | Precedence: bulk, rDNS, SPF/DKIM/DMARC, opt-in, пороги жалоб, 550 user not found, ловушки |
| Условия использования Постмастера | https://help.mail.ru/developers/postmaster/use/ | VK (Mail) | редакция 14.12.2022 | 2026-09-15 | условия (A) | FBL: удалять жалобщиков, нет приоритета в поддержке |
| Постмастер Mail.ru / Защита домена | https://postmaster.mail.ru/security/ | VK (Mail) | не указана | 2026-09-15 | официальная страница (A) | SPF, DKIM, DMARC, статистика и FBL |
| Отправить много писем + Требования Яндекса к честным рассылкам | https://yandex.ru/support/yandex-360/business/mail/ru/web/letter/create/send-many-letters | Яндекс | не указана | 2026-09-15 | официальная документация (A) | лимиты 300/1000/50, досрочная блокировка шаблонных писем, обязательные требования к рассылкам |
| RFC 7208 SPF | https://www.rfc-editor.org/rfc/rfc7208.html | IETF | апрель 2014 | 2026-09-15 | стандарт (A) | лимит 10 DNS-lookup |
| RFC 8301 DKIM crypto update | https://www.rfc-editor.org/rfc/rfc8301.html | IETF | январь 2018 | 2026-09-15 | стандарт (A) | ключи от 1024 (MUST), от 2048 (SHOULD) |
| RFC 7489 DMARC | https://www.rfc-editor.org/rfc/rfc7489.html | IETF | март 2015 | 2026-09-15 | стандарт, отменён (A) | relaxed и strict alignment |
| RFC 9989 DMARC (DMARCbis) | https://datatracker.ietf.org/doc/draft-ietf-dmarc-dmarcbis/ | IETF | 2026-05-20 | 2026-09-15 | стандарт (A) | Proposed Standard, отмена 7489 и 9091, тег t, удаление pct |
| RFC 8058 One-Click Unsubscribe | https://www.rfc-editor.org/rfc/rfc8058.html | IETF | январь 2017 | 2026-09-15 | стандарт (A) | механизм List-Unsubscribe-Post |
| M3AAWG Sender Best Common Practices v4.0 | https://www.m3aawg.org/sites/default/files/doc_files/m3aawg-sender-best-common-practices-aug-27-2026.pdf | M3AAWG | август 2026 | 2026-09-15 | отраслевой BCP (A) | прогрев около 6 недель, искусственный прогрев, поддомены против cousin-доменов, NDR-правило 2 раза за 2 недели, WHOIS, appending, cold email |
| M3AAWG Position on Cold Email v1.0 | https://www.m3aawg.org/M3AAWGPositionOnColdEmail | M3AAWG | ноябрь 2025 | 2026-09-15 | отраслевая позиция (A) | lookalike и multiple accounts, обход лимитов, искусственное engagement, маркеры cold email |
| Spamhaus’ take on Cold Emailing…AKA spam | https://www.spamhaus.org/resource-hub/spam/spamhaus-take-on-cold-emailing-aka-spam/ | Spamhaus | 2025 (точная дата не извлечена) | 2026-09-15 | позиция оператора блоклистов (A/D) | throwaway-домены, warm-up и фейковое engagement, листинг за ловушки |
| Spamhaus Glossary (Snowshoe) | https://www.spamhaus.org/glossary/ | Spamhaus | не указана | 2026-09-15 | глоссарий оператора блоклистов (A) | определение snowshoe |
| Spamtraps – fix the problem, not the symptom | https://www.spamhaus.com/resource-center/spamtraps-fix-the-problem-not-the-symptom/ | Spamhaus | не указана | 2026-09-15 | best practice оператора (A) | типы ловушек, wildcard-домены, role-адреса, dead-address ловушки |
| Amazon SES Sending review process FAQs | https://docs.aws.amazon.com/ses/latest/dg/faqs-enforcement.html | AWS | не указана | 2026-09-15 | официальная документация ESP (A для SES) | bounce 2/5/10%, жалобы 0,1/0,5% |
| GMass’s Email Warmup System Is Shutting Down | https://www.gmass.co/blog/warmup-shutting-down/ | GMass | 2023-01-19, обновл. 2023-02-06 | 2026-09-15 | блог сервиса (D) | закрытие warm-up по требованию Google (по словам GMass), 80 000 ящиков |
| What is the Warm Up Cool Off Period | https://helpcenter.smartlead.ai/en/articles/182-what-is-the-warm-up-cool-off-period | Smartlead | февраль 2024 («as of Feb 24») | 2026-09-15 | справка вендора (D) | масштаб warm-up-пула: 25 млн писем в день |
| Cold Email Sending Limits: Data from 2 Million Emails | https://howmanycoldemailsperday.com/blog/cold-email-sending-limits-data/ | Sales.co | 2026-01-28, обновл. 2026-02-01 | 2026-09-15 | маркетинговый блог вендора (E) | вендорские объёмы и ротация доменов; расходится с M3AAWG и Spamhaus |
| Understand role-based email addresses | https://help.klaviyo.com/hc/en-us/articles/17976334449947 | Klaviyo | не указана | 2026-09-15 | политика ESP (D) | блокировка технических role-адресов |

### Яндекс 360, Mail.ru, российские ESP, enrichment по российским компаниям (57)

| Название | URL | Организация / автор | Дата публикации | Дата доступа | Тип | Что подтверждает |
|---|---|---|---|---|---|---|
| ЕГРЮЛ ФНС (egrul.nalog.ru) | https://www.nalog.gov.ru/rn77/service/egrip2/access_order/ |  |  | 2026-09-15 |  |  |
| Прозрачный бизнес ФНС | https://pb.nalog.ru/about.html |  |  | 2026-09-15 |  |  |
| Открытые данные ФНС | https://www.nalog.gov.ru/opendata/ |  |  | 2026-09-15 |  |  |
| ГИРБО / БФО | https://bo.nalog.gov.ru/ |  |  | 2026-09-15 |  |  |
| API-ФНС / DaMIA / ofdata | https://api-fns.ru/ |  |  | 2026-09-15 |  |  |
| Checko | https://checko.ru/integration/api |  |  | 2026-09-15 |  |  |
| Rusprofile | https://www.rusprofile.ru/ |  |  | 2026-09-15 |  |  |
| Контур.Фокус API | https://focus.kontur.ru/site/price/api-group/counteragent |  |  | 2026-09-15 |  |  |
| СПАРК-Интерфакс | https://spark-interfax.ru/integration |  |  | 2026-09-15 |  |  |
| hh.ru API | https://dev.hh.ru/admin/developer_agreement |  |  | 2026-09-15 |  |  |
| SuperJob API | https://api.superjob.ru/ |  |  | 2026-09-15 |  |  |
| ЕИС zakupki.gov.ru | https://zakupki.gov.ru/epz/opendata/search/results.html |  |  | 2026-09-15 |  |  |
| Каталоги Экспоцентра | https://catalog.expocentr.ru/ |  |  | 2026-09-15 |  |  |
| API Поиска по организациям Яндекс | https://yandex.ru/dev/commercial/doc/ru/concepts/geosearch |  |  | 2026-09-15 |  |  |
| 2ГИС Places API | https://docs.2gis.com/api/search/places/overview |  |  | 2026-09-15 |  |  |
| Детекторы CMS (iTrack, PR-CY, enterno) | https://itrack.ru/whatcms/ |  |  | 2026-09-15 |  |  |
| DealRocket / Контур.Компас / ExportBase / Trigga | https://dealrocket.ru/ |  |  | 2026-09-15 |  |  |
| Отправить много писем (customers) | https://yandex.ru/support/yandex-360/customers/mail/ru/web/letter/create/send-many-letters | Яндекс | не указана | 2026-09-15 | A | Лимиты личной почты |
| Общие условия Яндекс 360 | https://yandex.ru/legal/360_termsofuse/ru/ | Яндекс | 14.09.2026 | 2026-09-15 | A, оферта | Запрет массовых рассылок (п. 1.19), блокировки (п. 3.1) |
| DKIM-подпись | https://yandex.ru/support/yandex-360/business/admin/ru/domains/dns/dkim | Яндекс | не указана | 2026-09-15 | A | Настройка DKIM |
| SPF-запись | https://yandex.ru/support/yandex-360/business/admin/ru/domains/dns/spf | Яндекс | не указана | 2026-09-15 | A | SPF-значение |
| Блог 360: письма не в спам | https://360.yandex.ru/blog/guides/kak-sdelat-chtoby-vashi-pisma-ne-popadali-v-spam-sovetuet-ekspert-yandeks-360/ | Яндекс 360 | не указана | 2026-09-15 | A/D | Покупные базы для холодных рассылок вредят |
| Яндекс Рассылки: О сервисе | https://yandex.ru/support/yandex-360/business/send/ru/ | Яндекс | не указана | 2026-09-15 | A | Требования MX/SPF/DKIM, только администратор |
| Яндекс Рассылки: Ограничения | https://yandex.ru/support/yandex-360/business/send/ru/limits | Яндекс | не указана | 2026-09-15 | A | Тарифные и общие лимиты |
| Яндекс Рассылки: Правила | https://yandex.ru/support/yandex-360/business/send/ru/rules | Яндекс | не указана | 2026-09-15 | A | Согласие, запрет ролевых адресов, блокировки |
| Лендинг Яндекс Рассылок | https://360.yandex.ru/business/email-sending/ | Яндекс | не указана | 2026-09-15 | A | Нет API, соответствие 152-ФЗ, ошибка в лимите |
| Письмо похоже на спам | https://yandex.ru/support/yandex-360/customers/mail/ru/bounces/other/message-rejected-under-suspicion-of-spam | Яндекс | не указана | 2026-09-15 | A | Тексты bounce при спам-фильтре |
| Email Soldiers: Яндекс Рассылки 2026 | https://emailsoldiers.ru/blog/yandeks-rassylki-dlya-biznesa | Email Soldiers | 2026 | 2026-09-15 | D | Цены, поведение Яндекса при скачках |
| Хабр: IMAP/SMTP только с тарифом | https://habr.com/ru/news/1042832/ | Хабр (пользователь) | 2026 | 2026-09-15 | B/E | Письмо Яндекса, отключение 03.07.2026 |
| ispmanager: IMAP/SMTP без тарифа | https://www.ispmanager.ru/news/yandeks-i-mailru-zakryvaet-imap-i-smtp-bez-tarifa-kak-zabrat-pochtu-na-svoj-server-i-ne-platit-za-to-chto-ranshe-bylo-besplatno | ispmanager | 2026 | 2026-09-15 | B | 29.06 Яндекс, 12.06 VK WorkSpace |
| Metaratings | https://cybersport.metaratings.ru/news/mail-ru-i-yandeks-pochta-ogranichat-besplatnyy-dostup-cherez-storonnie-klienty/ | Metaratings | 09.06.2026 | 2026-09-15 | B | Дата анонса ограничений |
| Postbox: квоты и лимиты | https://yandex.cloud/ru/docs/postbox/concepts/limits | Yandex Cloud | не указана | 2026-09-15 | A (сниппет) | 1 письмо в секунду |
| Postbox: сервис | https://yandex.cloud/ru/services/postbox | Yandex Cloud | не указана | 2026-09-15 | A (сниппет) | 2 000 бесплатно, 10 млн в день |
| vc.ru: блокировка Postbox | https://vc.ru/marketing/2161704-problemy-s-pochtoj-rassylkoj-na-yandex-cloud-postbox | пользователь vc.ru | 2025–2026 | 2026-09-15 | E | Блок за рассылку без согласия |
| VK Почта: получатели | https://help.mail.ru/vkmail/letters/create/to/ | VK | не указана | 2026-09-15 | A | 30 получателей |
| Mail.ru: ошибки отправки | https://help.mail.ru/developers/errors/ | VK | не указана | 2026-09-15 | A | Часовой лимит, 421/550 |
| Mail.ru: общие положения | https://help.mail.ru/developers/mailing_rules/general/ | VK | не указана | 2026-09-15 | A | Запрет купленных баз, 5 % невалидных, разделение IP |
| Соглашение Почты Mail | https://help.mail.ru/legal/terms/mail/ua/ | VK | ред. 02.07.2026 | 2026-09-15 | A | Запрет спама и мультирегистрации |
| Постмастер Mail.ru | https://postmaster.mail.ru/ | VK | не указана | 2026-09-15 | A | Сервис работает |
| VK WorkSpace Рассылки | https://vc.ru/marketing/2890218-novyj-instrument-dlya-massovyh-rassylok-v-vk-workspace | vc.ru | 2026 | 2026-09-15 | D | 5 000 ₽ в месяц |
| MailerMail: Постофис закрыт | https://mailermail.ru/guides/yandex-postoffice/ | MailerMail | 2025–2026 | 2026-09-15 | B | Закрытие 11.09.2020 |
| Unisender Антиспам | https://www.unisender.com/ru/antispam/ | Unisender | не указана | 2026-09-15 | A | Запрет открытых источников, double opt-in для КП |
| Sendsay Антиспам | https://sendsay.ru/about/antispam | Sendsay | не указана | 2026-09-15 | A | Запрет парсинга и покупки списков |
| DashaMail Антиспам | https://dashamail.ru/antispam/ | DashaMail | не указана | 2026-09-15 | A | Запрет баз из 2ГИС и купленных |
| NotiSend Антиспам | https://notisend.ru/terms/antispam/ | NotiSend | не указана | 2026-09-15 | A | Запрет купленных баз и парсинга |
| Altcraft Антиспам | https://altcraft.com/ru/antispam-policy | АльтКрафт | не указана | 2026-09-15 | A | Запрет парсинга и купленных баз |
| enKod Антиспам | https://enkod.io/antispam-policy/ | enKod | не указана | 2026-09-15 | A | Запрет купленных баз, хранение согласий |
| Coldy | https://coldy.ai/ | Coldy | 2026 | 2026-09-15 | D | Холодные базы, прогрев, эмуляция ручной отправки |
| Respondo: прогрев | https://respondo.ru/email-warmup | Respondo | 2026 | 2026-09-15 | D | Объёмы прогрева, SMTP-блок у новых ящиков Яндекса |
| Клерк: ГИРБО | https://www.klerk.ru/buh/articles/497008/ | Клерк | 2020 | 2026-09-15 | B | Бесплатно по компании, 200 тыс. ₽ в год |
| Контур.Фокус API цены | https://toolfox.ru/services/s/kontur-focus-api | ToolFox | 2026 | 2026-09-15 | B/D | От 96 тыс. ₽ в год |
| Хабр: HH закрыл публичный API вакансий | https://habr.com/ru/news/1069286/ | Хабр | 2026 | 2026-09-15 | B | 403 с апреля 2026 |
| Xago: закрытие API hh | https://xago.ru/blog/zakrytie-api-hh/ | Xago | 2026 | 2026-09-15 | B | Закрытие соискательского API 15.12.2025 |
| ProRecruitment: HH API для работодателя | https://prorecruitment.ru/blog/hh-api-dlya-rabotodatelya | ProRecruitment | 2026 | 2026-09-15 | C | 50 запросов в сутки (п. 10.6.1) |
| Хабр: zakupki SOAP | https://habr.com/ru/articles/869934/ | Хабр | 2024–2025 | 2026-09-15 | B/C | Закрытие FTP, токен |
| Условия бесплатного API Яндекс Карт | https://yandex.ru/dev/commercial/doc/ru/ | Яндекс | не указана | 2026-09-15 | A | Запрет сохранения в базу/Excel |
| Trigga: обзор ЛПР-сервисов | https://trigga.ru/blog/b2b-bazyi-i-servisyi-poiska-kontaktov-lpr-obzor-10-platform-2026 | Trigga | 2026 | 2026-09-15 | D | Покрытие РФ у Apollo, список РФ-сервисов |

### Бенчмарки, метрики, цепочки, open rate (47)

| Название | URL | Организация / автор | Дата публикации | Дата доступа | Тип | Что подтверждает |
|---|---|---|---|---|---|---|
| Best Time To Send B2B Emails (2026 Study) | https://belkins.io/blog/best-time-to-send-email | Belkins / Vladyslav Podoliako | обновлено 2026-06-26 | 2026-09-15 | first-party исследование | день и время, определения reply и meeting rate |
| The key B2B cold outreach benchmarks 2025 | https://belkins.io/resources/b2b-cold-outreach-benchmarks | Belkins + Reply.io, Expandi, Nooks | 2025 | 2026-09-15 | лендинг отчёта (gated) | выборка 16,5M писем |
| LinkedIn: Belkins 16.5M retelling | https://www.linkedin.com/posts/harm-linnecke_what-are-b2b-cold-email-response-rates-activity-7387048744640499712-JjiE | Harm Linnecke | 2025 | 2026-09-15 | пересказ (сниппет) | 5,8% (2024), 6,8% (2023) по старой методологии |
| Cold Email Response Rates: B2B Benchmarks | https://instantly.ai/blog/cold-email-reply-rate-benchmarks/ | Instantly | обновлено 2026-07-01 | 2026-09-15 | блог вендора | формула reply ÷ delivered |
| Email Tracking Pixels & Deliverability | https://instantly.ai/blog/email-tracking-and-deliverability-why-tracking-pixels-can-hurt-your-inbox-placement/ | Instantly | не указана | 2026-09-15 | блог вендора | мнение о пикселях, пороги bounce |
| Cold Email Subject Lines for Follow-Ups | https://instantly.ai/blog/cold-email-subject-lines-for-follow-ups-how-to-re-engage-without-being-pushy/ | Instantly | не указана | 2026-09-15 | блог вендора | рекомендации thread / new thread |
| The State of Cold Email 2026 | https://www.smartlead.ai/benchmarks/state-of-cold-email | Smartlead | 2026 (H1 2026) | 2026-09-15 | first-party отчёт (JS, сниппет) | 1:135 = 0,74%, 850M+ |
| Cold email reply rate: what's good and what's broken | https://www.smartlead.ai/blog/cold-email-reply-rate | Smartlead / Wajahat Ali | 2026 | 2026-09-15 | блог вендора | топ-10% 1:38; автоответы и OOO |
| LinkedIn: Smartlead 850M breakdown | https://www.linkedin.com/posts/timyakubson_smartlead-analyzed-850-million-cold-emails-activity-7488929112091336704-J5J0 | Tim Yakubson | 2026 | 2026-09-15 | пересказ | 64% ответов в первый час |
| Cold Email Best Practices | https://outreachbloom.com/cold-email-best-practices/ | Outreachbloom | 2026 | 2026-09-15 | агрегатор | определения знаменателей разных отчётов |
| I Analyzed 53M Cold Emails | https://www.saleshandy.com/blog/cold-email-statistics/ | Saleshandy | 2026 (после июня) | 2026-09-15 | first-party отчёт | 3,7%, positive, follow-up 44%, bounce, время, мультиканал |
| Cold Email Resources (Help Center) | https://help.hunter.io/en/articles/12098638-cold-email-resources | Hunter | не указана | 2026-09-15 | справка (сниппет) | выборка 31M+ |
| How to master cold email (85M) | https://www.gong.io/resources/guides/how-to-master-cold-email-get-the-data-backed-guide-based-on-85-million-emails | Gong | не указана | 2026-09-15 | gated-гайд | только заявка на выборку |
| 7 tips for the perfect follow-up email | https://www.gong.io/blog/7-tips-for-writing-the-perfect-follow-up-sales-email-according-to-science | Gong Labs | не указана | 2026-09-15 | блог с данными | 304 174 follow-up писем, фразы против встреч |
| The Cold Email Benchmark Report | https://lavender.ai/blog/the-cold-email-benchmark-report | Lavender | выборка на 2026-02-04 | 2026-09-15 | first-party отчёт | исключение OOO и bounce, 231 818 писем |
| 5 Takeaways from Our Latest Cold Email Benchmark Report | https://lavender.ai/blog/5-takeaways-from-our-latest-cold-email-benchmark-report | Lavender | 2026 | 2026-09-15 | блог | выборка, сегментные выводы |
| We Analyzed 12 Million Outreach Emails | https://backlinko.com/email-outreach-study | Backlinko (Semrush) × Pitchbox | 2019 | 2026-09-15 | исследование | 8,5%, +65,8% от follow-up, среда |
| Only 1 of 8 Outreach Emails Receive a Reply | https://www.prnewswire.com/news-releases/only-1-of-8-outreach-emails-receive-a-reply-new-study-by-pitchbox-and-backlinko-finds-300833306.html | Pitchbox / Backlinko | 2019 | 2026-09-15 | пресс-релиз | дата и контекст исследования |
| Cold Email Statistics for 2026 | https://snov.io/blog/cold-email-statistics/ | Snov.io | 2026 | 2026-09-15 | блог с данными | трекинг 1,08 против 2,36; 27,7% open |
| What Is a Realistic Cold Email Reply Rate? | https://replylead.com/realistic-cold-email-reply-rate.html | ReplyLead | снимок 2026-08-12, проверено 2026-09-09 | 2026-09-15 | кейс агентства с методологией | влияние знаменателя и агрегации |
| why cold email open rates lie | https://www.lemlist.com/blog/cold-email-open-rates | lemlist / Rémi | 2025-11-27, обновлено 2026-08-10 | 2026-09-15 | блог вендора | пиксель +15% спама; Apple 64,66% (через Litmus) |
| lemcoach: Cold email benchmarks and metrics | http://help.lemlist.com/en/articles/13942005-lemcoach-cold-email-benchmarks-and-metrics-what-good-looks-like | lemlist | 2026 | 2026-09-15 | справка вендора | определение positive, нормы |
| Best Practices for Reviewing Your Outreach Sequences | https://support.outreach.io/support/solutions/articles/159000426250-best-practices-for-reviewing-your-outreach-sequences | Outreach / Nick Hart | не указана | 2026-09-15 | справка вендора | 2,9% email reply, top-line ≥12%, bounce <2,8% |
| KPIs and Benchmarks for Measuring Cadence Success | https://champions.salesloft.com/cadence-best-practices-93/kpis-and-benchmarks-for-measuring-cadence-success-226 | Salesloft Community | не указана | 2026-09-15 | сообщество вендора | reply 3–6%, bounce 2% |
| State of Cold Email 2026 (Mailshake) | https://mailshake.com/blog/the-state-of-cold-email-2025/ | Mailshake | 2026 | 2026-09-15 | опрос | 508 респондентов, 1–4% |
| Cold Email Statistics Based on Sending Over 20M Cold Emails | https://woodpecker.co/blog/cold-email-statistics/ | Woodpecker | не указана | 2026-09-15 | агрегатор вендора | пример перепечатки и путаницы источников |
| Cold Email Statistics (QuickMail) | https://quickmail.com/cold-email/statistics | QuickMail | не установлена | 2026-09-15 | сниппет | распределение кампаний по reply |
| Apollo Tolly report press release | https://www.prnewswire.com/news-releases/new-report-apolloio-exceeds-industry-benchmarks-for-data-quality-and-cold-email-outreach-302737035.html | Apollo.io / The Tolly Group | 2026-04-08 | 2026-09-15 | заказное исследование | 2,37% meeting на 384 контактах |
| Cold Email Benchmarks by Industry | https://www.cleverly.co/blog/cold-email-benchmarks-by-industry | Cleverly | 2026 | 2026-09-15 | агрегатор | пример цифр без источника (40–60% positive) |
| Cold Email Conversion Rate | https://reachoutly.com/cold-email/conversion-rate/ | Reachoutly | 2026 | 2026-09-15 | агрегатор / кейс | непроверенные ссылки на Salesforge и Martal |
| Cold Email Statistics 2026: A Source-First Benchmark Guide | https://overloop.com/blog/cold-email-statistics | Overloop | 2026 | 2026-09-15 | методический гайд | чек-лист сопоставимости бенчмарков |
| Email sender guidelines | https://support.google.com/a/answer/81126 | Google | живой документ (требования с 2024) | 2026-09-15 | официальная документация | требования к отправителям на Gmail |
| Email sender guidelines FAQ | https://support.google.com/a/answer/14229414 | Google | живой документ | 2026-09-15 | официальная документация | spam rate <0,1% / 0,3%, 5 000/день, 48 ч отписка |
| Sender Best Practices | https://senders.yahooinc.com/best-practices/ | Yahoo | живой документ | 2026-09-15 | официальная документация | spam rate <0,3%, отписка за 2 дня |
| Outlook’s New Requirements for High‐Volume Senders | https://techcommunity.microsoft.com/blog/microsoftdefenderforoffice365blog/strengthening-email-ecosystem-outlook’s-new-requirements-for-high‐volume-senders/4399730 | Microsoft | апрель 2025 (обновлено 29.04.2025) | 2026-09-15 | официальный блог | SPF/DKIM/DMARC для 5 000+/день с 5.05.2025 |
| Safe Links in Microsoft Defender for Office 365 | https://learn.microsoft.com/en-us/defender-office-365/safe-links-about | Microsoft Learn | живой документ | 2026-09-15 | официальная документация | переписывание ссылок и проверка в момент клика |
| Email Client Market Share | https://www.litmus.com/email-client-market-share/ | Litmus | отчёт за июль 2026 | 2026-09-15 | отраслевая телеметрия | MPP ~55–60% открытий, Gmail image cache |
| Apple’s Mail Privacy Protection Knowledge Center | https://www.litmus.com/apple-mail-privacy-protection-resources | Litmus | не указана | 2026-09-15 | отраслевой ресурс | более 50% открытий на устройствах с MPP |
| Email Client Market Share in October 2021 | https://www.litmus.com/blog/email-client-market-share-october-2021 | Litmus | 2021 | 2026-09-15 | отраслевая телеметрия | дата запуска MPP 20.09.2021, 14,35% |
| Mail Privacy Protection & Privacy | https://www.apple.com/legal/privacy/data/en/mail-privacy-protection/ | Apple | живой документ | 2026-09-15 | официальная документация | назначение MPP |
| Gmail deploys image proxy servers | https://www.wordtothewise.com/2013/12/gmail-deploys-image-proxy-servers/ | Word to the Wise | декабрь 2013 | 2026-09-15 | технический блог | Gmail image proxy, трекинг первого открытия |
| Exploring the growing impact of NHI | https://www.m3aawg.org/blog/exploring-the-growing-impact-of-nonhuman-interactions-nhi-on-email-send-metrics | M3AAWG Senders Committee | 2020 | 2026-09-15 | отраслевая организация | NHI при security-сканировании |
| NHI document (PDF) | https://www.m3aawg.org/sites/default/files/doc_files/nhi_nov_2020_doc.pdf | M3AAWG | ноябрь 2020 | 2026-09-15 | отраслевой документ (текст не извлёкся) | ссылка на первоисточник |
| Non-Human Interactions creating unexpected Click Events | https://support.clickdimensions.com/hc/en-us/articles/45259921619213-Non-Human-Interactions-creating-unexpected-Click-Events | ClickDimensions | обновлено апрель 2026 | 2026-09-15 | справка вендора | Safe Links июнь 2023; M3AAWG <10% B2C |
| Over 50% of Email Clicks Are Not Human | https://omnivery.com/blog/nhi-is-getting-worse | Omnivery | 2026 | 2026-09-15 | блог вендора (проприетарные данные) | B2B ~75% NHI-кликов |
| How to Detect Bot Clicks in Email Marketing | https://mailchimp.com/resources/bot-clicks-in-email-marketing/ | Mailchimp | не указана | 2026-09-15 | сниппет | ~1 из 5 кликов боты |
| Do tracking pixels directly cause emails to be marked as spam | https://www.suped.com/learn/email-deliverability/do-tracking-pixels-directly-cause-emails-to-be-marked-as-spam | Suped | не указана | 2026-09-15 | мнение (сниппет) | контраргумент о пикселях |

### Первое письмо, темы, CTA, персонализация, follow-up (35)

| Название | URL | Организация / автор | Дата публикации | Дата доступа | Тип | Что подтверждает |
|---|---|---|---|---|---|---|
| What's the Best Word Count & Length for Cold Emails | https://hunter.io/blog/cold-email-word-count/ | Hunter | ~2024 (данные 2022–2024) | 2026-09-15 | Вендор, first-party, 34 млн писем | Длина 20–39 слов, плоская кривая, критика Boomerang |
| This surprising cold email CTA | https://www.gong.io/blog/this-surprising-cold-email-cta-will-help-you-book-a-lot-more-meetings | Gong Labs | н/д (~2020–21) | 2026-09-15 | Вендор, 304 174 письма | Interest CTA против specific и open-ended |
| Analyzing Cold Email Statistics | https://www.gong.io/blog/cold-email-stats | Gong | н/д | 2026-09-15 | Вендор | «Длинные» 30–150 слов, ROI −15%, «Thoughts» −20%, «I never heard back» −14%, «Hope all is well» +24% |
| 4 effective ways to boost your email reply rate | https://www.gong.io/blog/4-data-backed-ways-to-increase-your-email-reply-rate-and-book-that-meeting | Gong Labs | 07.07.2023 | 2026-09-15 | Вендор, 30 000+ писем, 250+ компаний | Уровни персонализации по ролям |
| 6 Proven Cold Email Strategies (examples) | https://www.gong.io/blog/cold-email-examples | Gong | н/д | 2026-09-15 | Подборка кейсов | Реальные темы (фейковый Re:, хобби, подарок) |
| The Data-Backed Cold Email Formula | https://www.30mpc.com/newsletter/the-data-backed-cold-email-formula-the-exact-words-length | 30 Minutes to President's Club | н/д | 2026-09-15 | Вендор/медиа, данные Gong 85M+ | Оффер +28%, проблемы +20%, соцдоказательство +41%, персонализация ×5 |
| 4 Data-Backed Subject Lines | https://www.30mpc.com/newsletter/4-data-backed-subject-lines-to-get-your-cold-emails-opened | 30MPC | н/д | 2026-09-15 | Вендор/медиа, данные Gong | 1–4 слова, lowercase, пустая тема −12% ответов, salesy −17.9% |
| Data says: The Shorter, the Better | https://lavender.ai/blog/best-length-cold-email | Lavender | н/д | 2026-09-15 | Вендор | 25–50 слов, фреймворк Context |
| Cold Email 101 | https://lavender.ai/blog/cold-email-101 | Lavender | ~2023 | 2026-09-15 | Вендор | Читаемость +67%, мобильность +83%, фреймворк, примеры тем, советы без ссылок/изображений |
| How to Write Cold Email Subject Lines | https://lavender.ai/blog/cold-email-subject-line-tips | Lavender | н/д | 2026-09-15 | Вендор | Вопросы −56%, числа −46%, Title Case, 2 слова, Salesloft −12% |
| How to Build a Cold Email Personalization Process | https://lavender.ai/blog/how-to-build-a-cold-email-personalization-process | Lavender | н/д | 2026-09-15 | Вендор | Salesloft +50–250% (вторично), «Congrats on the funding» |
| Debunking Gong's "longer cold email" myth | https://www.linkedin.com/posts/williamallred_finally-if-you-follow-gong-youve-probably-activity-7361029146396831745-Bi7r | Will Allred (Lavender), LinkedIn | ~2025 | 2026-09-15 | Экспертный пост | Длинное предложение −17%, спор с Gong |
| 7 Tips for Getting More Responses to Your Emails | https://blog.boomerangapp.com/2016/02/7-tips-for-getting-more-responses-to-your-emails-with-data/ | Boomerang | 02.2016 | 2026-09-15 | Вендор, 40M+ писем (не cold) | 50–125 слов, 3-й класс, 1–3 вопроса, 3–4 слова в теме, лесть |
| B2B Cold Email Subject Lines and Engagement (2025 Study) | https://belkins.io/blog/b2b-cold-email-subject-line-statistics | Belkins + Reply.io | 06.08.2025 | 2026-09-15 | Агентство/вендор, 5.5 млн писем 2024 | Персонализация темы 3%→7%, 2–4 слова, вопросы, регистр, числа |
| Email-аутрич – исследование и бенчмарки | https://habr.com/ru/articles/918424/ | Хабр (перевод Belkins/Reply.io/Expandi) | 2025 | 2026-09-15 | Вторичный перевод | Изображения, вложения (Reply.io), follow-up 2023–24, длина темы |
| 2x Your Reply Rate: Personalized First Lines | https://instantly.ai/blog/2x-your-reply-rate/ | Instantly | н/д | 2026-09-15 | Вендор, без методики | ×2 от первых строк, примеры ИИ-комплиментов |
| Do images hurt cold email deliverability? | https://www.lemlist.com/blog/images-cold-email-deliverability | lemlist | 27.11.2025 (обн. 10.08.2026) | 2026-09-15 | Вендор | Изображение +~20%, GIF хуже, ~120 слов |
| Email Subject Lines: 10 Data Findings | https://www.yesware.com/blog/email-subject-lines/ | Yesware | н/д (исследование 2021) | 2026-09-15 | Вендор, 115M / 1.2M / 262K | Числа +45%, вопросы +10%, 1–5 слов, Re:/Fwd:, примеры тем |
| Breaking Up is Hard: Sales Breakup Emails | https://www.yesware.com/blog/sales-breakup-email/ | Yesware | н/д | 2026-09-15 | Вендорский блог | Пересказ HubSpot 33% |
| The Power of Breakup Emails | https://blog.hubspot.com/sales/the-power-of-breakup-emails-templates-to-close-the-loop | HubSpot | н/д | 2026-09-15 | Блог, anecdote | 33% ответов на breakup (одна команда), темы breakup |
| 17 Best Cold Email Subject Lines | https://close.com/blog/cold-email-subject-lines | Close | н/д | 2026-09-15 | Вендорский блог, без данных | Шаблоны тем |
| Follow Up Email: Guide for B2B Sales Teams (2026) | https://overloop.com/blog/follow-up-email | Overloop | 20.05.2026 | 2026-09-15 | Вендорский блог, собственные данные без методики | Стадии follow-up, breakup 8–15% (со ссылкой на Mailshake), конкретное время +30% |
| Гайд: как составить цепочку холодных писем B2B | https://trigga.ru/blog/autrich-kak-stroit-tsepochki-chto-pisat-v-pismah-i-kakoj-interval-vyibrat | Trigga | 06.02.2026 | 2026-09-15 | Вендорский блог (RU) | 4 вида пингов, break-up до 12%, RU-шаблон темы |
| Video in Motion Benchmark Report | https://www.vidyard.com/video-in-motion-benchmark-report/ | Vidyard | н/д (~2026) | 2026-09-15 | Маркетинг вендора | Видео «5x», кейс 78% |
| CAN-SPAM Act: A Compliance Guide for Business | https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business | FTC | ред. 01.2024 | 2026-09-15 | Официальная документация | Запрет обманных тем, B2B не исключение, штраф $53,088 |
| RE: Misleading Subject Lines | https://www.litmus.com/blog/misleading-subject-lines | Litmus | н/д (2+ года) | 2026-09-15 | Отраслевой блог | Типы обманных тем, Litmus×Fluent, штраф Avis/Budget C$30 млн |
| Распространяя рекламу по сетям электросвязи, не заручившись согласием… | https://fas.gov.ru/publications/18830 | ФАС России | 24.07.2019 | 2026-09-15 | Официальный источник | ч. 1 ст. 18 38-ФЗ, штраф 50 000 ₽ за email-рекламу |
| Most people do not realize when a personal message was written by AI | https://theconversation.com/most-people-do-not-realize-when-a-personal-message-they-receive-was-written-by-ai-study-finds-278874 | The Conversation (академ. авторы) | ~2026 | 2026-09-15 | Академический эксперимент, 1 300+ чел. | Штраф за раскрытие ИИ; без раскрытия ИИ не подозревают |
| Is writing with AI at work undermining your credibility? | https://news.ufl.edu/2025/08/writing-ai-work/ | University of Florida (Cardon & Coman, IJBC) | 08.2025 | 2026-09-15 | Рецензируемое исследование, 1 100 чел. | Искренность 40–52% против 83% при высокой доле ИИ |
| Polished yet impersonal: AI-written emails | https://www.hiig.de/en/unintended-consequences-of-ai-written-emails/ | HIIG | н/д | 2026-09-15 | Академический блог (обзор) | Формульный тон ИИ раздражает — мнение с обзором литературы (D) |
| Write Cold Emails That Convert (Reply Research) | https://reply.io/write-better-cold-emails/ | Reply.io | н/д | 2026-09-15 | Вендор (загрузился только вводный блок) | Бенчмарк 3.02% reply; детальные данные взяты через Хабр |
| Reddit: I tested AI written cold emails against human | https://www.reddit.com/r/salesdevelopment/comments/1sk965x/i_tested_ai_written_cold_emails_against_human/ | Reddit | ~2026 | 2026-09-15 | Anecdotal (только сниппет) | ИИ-персонализация −30–40% (E) |
| Reddit: AI personalization is actively ruining cold email | https://www.reddit.com/r/salesdevelopment/comments/1rqgpa6/unpopular_opinion_ai_personalization_is_actively/ | Reddit | ~2026 | 2026-09-15 | Anecdotal (только сниппет) | Отказ от кастомных первых строк (E) |
| lemlist Help: Cold email best practices | http://help.lemlist.com/en/articles/4452701-cold-email-best-practices-to-increase-reply-rates | lemlist | н/д | 2026-09-15 | Документация вендора (только сниппет) | Не ставить calendar link в первое письмо (D) |
| 5 types of bump emails | https://www.linkedin.com/posts/jasondbay_5-types-of-bump-emails-to-double-your-cold-activity-7323678832618606593-ZmDh | Jason Bay, LinkedIn | ~2025 | 2026-09-15 | Экспертный пост (только сниппет) | Типы bump (D) |

### AI в outreach и signal-based outreach (57)

| Название | URL | Организация / автор | Дата публикации | Дата доступа | Тип | Что подтверждает |
|---|---|---|---|---|---|---|
| 11x has been claiming customers it doesn't have | https://techcrunch.com/2025/03/24/a16z-and-benchmark-backed-11x-has-been-claiming-customers-it-doesnt-have/ | TechCrunch | 2025-03-24 | 2026-09-15 | Расследование | Отток 70–80% по словам сотрудников, спорный ARR, логотипы ZoomInfo и Airtable, галлюцинации |
| 11x CEO Hasan Sukkar steps down | https://techcrunch.com/2025/05/05/11x-ceo-hasan-sukkar-steps-down/ | TechCrunch | 2025-05-05 | 2026-09-15 | Новость | Смена CEO после расследования |
| When AI SDR Claims Don't Hold Up | https://salesmotion.io/blog/ai-sdr-claims-scrutiny-what-buyers-should-verify | Salesmotion | 2025 | 2026-09-15 | Вендорский блог | Реакция рынка и VC на 11x |
| SDR Models, Motions & Metrics 2025 | https://www.bridgegroupinc.com/research/2025-sdr-models-metrics-report-the-bridge-group | The Bridge Group | 2025-02-06 | 2026-09-15 | Опрос 351 компании | AI SDR у 1%; 60% SDR на квоте |
| First Year Using Agentforce | https://www.salesforce.com/news/stories/first-year-agentforce-customer-zero/ | Salesforce | ≈2025 | 2026-09-15 | Вендорский self-report | 43 тыс. лидов, $1,7 млн; 30% → <10% «не знаю»; уроки по данным и guardrails |
| Customer Agent and Prospecting Agent pricing | https://www.hubspot.com/company-news/hubspots-customer-agent-and-prospecting-agent-now-you-pay-when-the-task-is-complete | HubSpot | апрель (год не указан) | 2026-09-15 | Пресс-релиз | $1 за рекомендованный лид; +57% активаций |
| How Regie.ai Achieved 48% Positive Email Replies | https://www.regie.ai/customers/reputation | Regie.ai | не указана | 2026-09-15 | Вендорский кейс | 7% reply, 48% позитивных |
| ‘Stop hiring humans’ AI ad sparks backlash | https://nypost.com/2025/06/21/us-news/stop-hiring-humans-ai-ad-sparks-backlash-in-nyc/ | NY Post | 2025-06-21 | 2026-09-15 | Журналистика | Кампания Artisan <$50 тыс., выручка ~$5 млн |
| Anti-Case Study: Strive's Churn From Warmly | https://www.warmly.ai/p/blog/anti-case-study-strives-churn-from-warmly | Warmly | ≈2023 | 2026-09-15 | Вендорский негативный кейс | 1 встреча за 6 месяцев |
| Selling Smarter Part 2: AI SDRs | https://sapphireventures.com/blog/selling-smarter-part-2-ai-sdrs-and-the-future-of-prospecting/ | Sapphire Ventures | ≈2024–2025 | 2026-09-15 | Мнение VC | Ошибки AI-персонализации |
| The AI SDR is dead, long live the AI SDR | https://www.commonroom.io/blog/common-room-ai-agent-pipeline-generation/ | Common Room | ≈2025 | 2026-09-15 | Вендорский блог | Отток 50–70% «из AI-поиска»; архитектура из трёх агентов |
| AI SDR reality check 2026 | https://ziellab.com/post/ai-sdr-what-works-after-the-hype-2026-guide | Ziellab | 2026 | 2026-09-15 | Агентский блог | Некорректно подтверждённые цифры (E); гибридные поды |
| AI SDR or Repackaged Spam? | https://alleyoop.io/ai-sdr-or-repackaged-spam | Alleyoop | 2026 | 2026-09-15 | Агентский блог | Круговое цитирование цифр; «AI drafts, a human approves» |
| Gartner Predicts AI Agents Will Outnumber Sellers 10 to 1 | https://www.channel-impact.com/gartner-predicts-ai-agents-will-outnumber-sellers-10-to-1/ | Gartner (перепечатка Channel Impact) | 2026-07-28 | 2026-09-15 | Прогноз + опрос 210 CSO | Менее 40% продавцов увидят рост продуктивности |
| Gartner: 67% of B2B Buyers Prefer a Rep-Free Experience | https://www.demandgenreport.com/industry-news/news-brief/gartner-67-of-b2b-buyers-prefer-a-rep-free-experience/52142/ | Gartner (перепечатка Demand Gen Report) | 2026-03 | 2026-09-15 | Опрос ~650 покупателей | 67% без продавца; 45% использовали AI |
| AI GTM flash survey | https://www.scalevp.com/blog/ai-gtm-flash-survey-how-marketing-teams-are-actually-using-ai | Scale Venture Partners | ≈2024 | 2026-09-15 | Опрос 63 руководителей | ~5% перестроили функцию, ~20% видят сильный эффект |
| Sales Reps Trust AI to Write Their Emails… | https://www.captivateiq.com/multiplier/stories/sales-reps-trust-ai-to-write-their-emails-they-dont-trust-it-to-run-their-pipeline | CaptivateIQ | 2026 | 2026-09-15 | Вендорский опрос | 81% используют AI; 22% не доверяют точности |
| HubSpot 2025 State of Sales Report | https://blog.hubspot.com/sales/hubspot-sales-strategy-report | HubSpot | 2025 | 2026-09-15 | Опрос 1 000 продавцов | 8% не используют AI; соцсети дают лучший отклик на холодный outreach |
| AI vs Human Recruiting Outreach | https://www.pin.com/blog/ai-vs-human-recruiting-outreach-study/ | Pin | 2026 | 2026-09-15 | Вендорские данные 4 млн+ писем | AI 4,97% против человека 12,6%; канал важнее; 45% проходят проверку; затухание по шагам |
| AI vs. Human Email Writing | https://prospectory.ai/resources/ai-email-writing-vs-human-study/ | Prospectory | не указана | 2026-09-15 | Вендорский эксперимент 10 тыс. писем | 8,2% против 11,7%; C-level; гибрид; скорость ответа |
| AI vs Human Cold Emails | https://www.saleshandy.com/blog/ai-vs-human-cold-emails/ | Saleshandy | 2026 | 2026-09-15 | Вендорский эксперимент 12 тыс. писем | 4,1% / 10,4% / 14,7%; спам-флаги |
| State of LinkedIn Outreach H2 2026 | https://expandi.io/state-of-linkedin-outreach-h2-2026/ | Expandi | 2026-06 | 2026-09-15 | Вендорские данные 13,2 млн запросов | AI-персонализация −12% acceptance; 5+ сообщений хуже; CSV = Sales Navigator |
| State of Email Outreach 2026 | https://hunter.io/the-state-of-cold-email | Hunter | 2026 | 2026-09-15 | Вендорские данные + опрос | Quick question, трекинг, сегменты, 3 письма, 69% против AI, правка +18% |
| B2B Cold Email Response Rates (2026 Study) | https://belkins.io/blog/cold-email-response-rates | Belkins | 2026-06-26 | 2026-09-15 | Агентские данные 7,5 млн писем | 0,45% на отправленные; падение 0,50 → 0,40; смена знаменателя |
| Sales Follow-Up Statistics (2026 Study) | https://belkins.io/blog/sales-follow-up-statistics | Belkins | 2026-06-26 | 2026-09-15 | Агентские данные | Follow-up дают 58,6% ответов; шаг 3 — больше всего встреч |
| Cold Email Benchmark Report 2026 | https://instantly.ai/cold-email-benchmark-report-2026 | Instantly | 2026 (данные 2025) | 2026-09-15 | Вендорские данные | 3,43% reply; 58% на первом шаге; 4–7 касаний; <80 слов |
| Does cold email even work any more? | https://www.gong.io/blog/does-cold-email-even-work-any-more-heres-what-the-data-says | Gong × Outbound Squad | не указана | 2026-09-15 | Вендорские данные 28 млн+ | 344 письма на встречу; питч −57%; «Do not talk about AI» |
| We measured the ROI of AI in sales | https://www.gong.io/blog/we-measured-the-roi-of-ai-in-sales-heres-how-it-really-impacts-your-deals | Gong Labs | ≈2024 | 2026-09-15 | Вендорские данные 1 млн сделок | +50% win rate при выполнении AI-задач (корреляция) |
| Avoid this tempting cold email mistake | https://www.gong.io/blog/avoid-this-tempting-cold-email-mistake-at-all-costs | Gong Labs | ≈2020 | 2026-09-15 | Вендорские данные 132 552 письма | ROI-язык −15% |
| Shoppers aren't impressed by AI-generated marketing | https://www.emarketer.com/content/shoppers-aren-t-impressed-by-ai-generated-marketing | eMarketer / Klaviyo | 2026 | 2026-09-15 | Опрос 8 000 потребителей | Доверие к видимому AI: 7% растёт, 31% падает |
| AI Slop Is Costing Your Sales Team | https://sbigrowth.com/insights/ai-slop-is-costing-your-sales-team-more-than-you-think | SBI | ≈2026 | 2026-09-15 | Консалтинг | Quality gate из 5 вопросов, выборочные проверки |
| AI Outreach Statistics 2026 | https://www.hausadvisors.com/blog/ai-outreach-statistics-2026 | Haus Advisors | 2026-06 | 2026-09-15 | Компиляция | Пример некорректного переноса исследования |
| Sales Statistics 2026: 28 Verified | https://fluidcrm.io/blog/sales-statistics/ | FluidCRM | 2026-08 | 2026-09-15 | Проверка статистик | 42 часа (HBR); interest-CTA 30% против 15% (Gong); разоблачение фейковых цифр |
| Email sender guidelines | https://support.google.com/mail/answer/81126?hl=en | Google | актуальная | 2026-09-15 | Официальная документация | Спам-жалобы <0,3%; one-click unsubscribe |
| Cold Email Subject Lines | https://outreachbloom.com/cold-email-subject-lines/ | OutreachBloom | 2026 | 2026-09-15 | Агентский блог | «Re:» как трюк; баг с пустым полем подстановки; критика цифр Belkins |
| Data Waterfalls | https://www.clay.com/blog/data-waterfalls | Clay | не указана | 2026-09-15 | Вендорский блог | Покрытие 30% → 80% |
| Forrester TEI (Bombora) | https://bombora.com/blog/forrester-tei-report-2022/ | Bombora / Forrester Consulting | 2022 | 2026-09-15 | Заказной TEI, 1 организация | +18% конверсии, ROI 342% |
| How to Measure Signal-Based Outreach | https://www.unifygtm.com/explore/signal-based-outreach-metrics?639a0fac_page=1 | Unify | 2026 | 2026-09-15 | Вендорский гайд | +73% ответов; ×2 при 4+ сигналах; метрики и классы ответов; кейсы Perplexity и CandorIQ |
| This Year in Performance | https://www.unifygtm.com/blog/this-year-in-performance | Unify | конец 2025 | 2026-09-15 | Вендорский self-report | $27 млн пайплайна по сигналам; 22% конверсии |
| Signals a Company Is Ready to Buy | https://www.unifygtm.com/explore/signals-company-ready-to-buy | Unify | 2026 | 2026-09-15 | Вендорский гайд | Технографика: эвристика, устаревание |
| UserGems: Metadata case | https://www.usergems.com/customers/metadata | UserGems | не указана | 2026-09-15 | Вендорский кейс | Цикл 60 против 143 дней; 25% базы устарело |
| UserGems: New Hires Signal | https://www.usergems.com/product/new-hires-signal | UserGems | не указана | 2026-09-15 | Вендорская страница | В 2,5 раза выше открытость в первые 3 месяца (660 тыс.+ проспектов) |
| How to track job changes | https://www.usergems.com/blog/track-job-changes | UserGems | ≈2022 | 2026-09-15 | Вендорский блог | Уровни отслеживаемых контактов (контекст) |
| Job Change Signals: The Pipeline Math | https://salesmotion.io/blog/job-change-signals-pipeline | Salesmotion | 2026 | 2026-09-15 | Вендорский блог | Champify: 37% против 19% (вторично) |
| Select the right buying signals | https://www.commonroom.io/blog/select-the-right-buying-signals/ | Common Room | ≈2024 | 2026-09-15 | Вендорский блог | Порог 3–5% signal-to-meeting |
| Common Room customers | https://www.commonroom.io/customers/ | Common Room | не указана | 2026-09-15 | Вендорские отзывы | +50% reply, дубли 3% → 0,3% (без методологии) |
| Signal-Based Outbound Guide | https://growleads.io/blog/signal-based-outbound/ | Growleads | 2026 | 2026-09-15 | Агентский фреймворк | 3–5 сигналов; веса × затухание × ICP; порог 80-й перцентиль |
| RB2B homepage FAQ | https://www.rb2b.com/ | RB2B | актуальная | 2026-09-15 | Вендорская документация | Person-level только США; согласие для глобального company ID |
| Visitor identification & GDPR | https://www.leadinfo.com/en/blog/visitor-identification-on-b2b-websites-does-company-data-fall-under-gdpr/ | Leadinfo | не указана | 2026-09-15 | Юридическая позиция вендора | Company-level на основании legitimate interest |
| GDPR website visitor identification 2026 | https://happierleads.com/blog/gdpr-website-visitor-identification-eu-rules-2026 | Happierleads | 2026 | 2026-09-15 | Юридическая позиция вендора | Person-level требует согласия; Германия строже |
| Privacy Class Action Spotlight | https://www.proskauer.com/blog/privacy-class-action-spotlight-latest-wave-of-wiretap-class-actions-continues-despite-dismissals-as-plaintiffs-try-new-approaches | Proskauer | ≈2023–2024 | 2026-09-15 | Анализ юрфирмы | Иски CIPA против identity resolution |
| Email marketing without consent | https://www.srd-rechtsanwaelte.de/en/blog/email-marketing-without-consent | SRD Rechtsanwälte | не указана | 2026-09-15 | Юридическое мнение | UWG §7(2): согласие нужно и в B2B |
| Is Cold Email Legal in Germany? | https://overloop.com/blog/b2b-cold-email-germany-gdpr-compliance | Overloop | 2026 | 2026-09-15 | Вендорский юридический обзор | OLG München 29 U 857/12 |
| TeamLink overview | https://www.linkedin.com/help/sales-navigator/answer/a101027/teamlink-overview | LinkedIn | актуальная | 2026-09-15 | Официальная документация | Функция тёплых интро, тарифы |
| vercel-labs/lead-agent | https://github.com/vercel-labs/lead-agent | Vercel | 2025 | 2026-09-15 | Открытый код и документация | Пайплайн research → qualify → email → одобрение в Slack |
| Building Production-Ready AI Agents (Vercel talk) | https://www.zenml.io/llmops-database/building-production-ready-ai-agents-for-internal-workflow-automation | ZenML (конспект доклада Vercel) | 2025 | 2026-09-15 | Кейс | 15–25 мин на лид; персонализация остаётся за людьми |
| B2B Buyer Experience Report 2025 (announcement) | https://revcity.6sense.com/home/discussion/2302/the-b2b-buyer-experience-report-2025-links-inside | 6sense | 2025-11 | 2026-09-15 | Анонс исследования | Выборка 4 510 покупателей (цифры отчёта не прочитаны) |

### Кейсы cold outreach (85)

| Название | URL | Организация / автор | Дата публикации | Дата доступа | Тип | Что подтверждает |
|---|---|---|---|---|---|---|
| Холодные email рассылки в B2B еще как работают: 28 целевых лидов | https://vc.ru/marketing/761532-holodnye-email-rassylki-v-b2b-eshe-kak-rabotayut-poprobovali-i-srazu-poluchili-28-celevyh-lidov | Respondo / EdBuro | 2023-07-17 | 2026-09-15 | вендор о клиенте | RU01: 650 компаний, 1841 письмо, 53 ответа, 28 лидов |
| Заработали 1 700 000 рублей с помощью холодной B2B-рассылки | https://vc.ru/marketing/2666778-kak-zarabotat-1-700-000-rublej-s-holodnoj-b2b-rassylkoj | Respondo / EdBuro | 2025-12-25 | 2026-09-15 | вендор о клиенте | RU01: 18 встреч, 2 договора, 1,7 млн ₽ при затратах 169 тыс. ₽ |
| EdBuro + Respondo: интервью | https://respondo.ru/cases/edburo | Respondo | н/д | 2026-09-15 | вендор о клиенте | RU01: цепочка и конверсия 8,15% |
| Дерзкая холодная рассылка с конверсией 20% | https://vc.ru/marketing/833069-derzkaya-holodnaya-rassylka-s-konversiei-20-kak-my-sdelali-3-prodazhi-v-krupnye-b2b-kompanii | Respondo | 2023-09-12 | 2026-09-15 | вендор о себе | RU02: дословные 5 писем, ответы по шагам, 3 сделки |
| Кейс с конверсией 13,6% (Alter) | https://vc.ru/marketing/805623-tozhe-dumaete-chto-konversiya-10-s-holodnyh-rassylok-v-b2b-prodazhah-eto-chto-to-nerealnoe-derzhite-keis-s-136 | Respondo / Alter | 2023-08-23 | 2026-09-15 | вендор о клиенте | RU03: 2889 писем, 140 ответов, 75 лидов; колл-центр хуже |
| 81 лид за месяц (CORRECT) | https://vc.ru/marketing/854451-kak-holodnaya-rassylka-pomogla-it-kompanii-naladit-prodazhi-v-top-30-otraslevyh-korporacii-81-lid-za-mesyac | Respondo / CORRECT | 2023-09-27 | 2026-09-15 | вендор о клиенте | RU04: 1024 компании, 196 ответов, целевые по шагам |
| Продажи ПО в компании с выручкой от 1 млрд | https://respondo.ru/cases/correct | Respondo | н/д | 2026-09-15 | вендор о клиенте | RU04: 5 писем через 2 дня, рекомендации |
| 700 целевых лидов в B2B | https://vc.ru/marketing/899250-700-celevyh-lidov-v-b2b-s-holodnyh-rassylok-serezno-da | Respondo | 2023-11-01 | 2026-09-15 | вендор о клиенте | RU05: 65 тыс. писем, 1214 ответов, 727 лидов, ROMI 250%; провал бесплатного аудита |
| 100 лидов и 8 потенциальных сделок (Nova) | https://vc.ru/marketing/1845494-holodnye-pisma-dlya-b2b-prodazh-kak-poluchit-100-lidov-i-8-potencialnyh-sdelok-na-milliony-s-pomoshyu-autricha | Respondo / Nova | 2025-03-19 | 2026-09-15 | вендор о клиенте | RU06: 3 кампании, 9389 писем, 17%/11,7%, лид 670 ₽ |
| Холодный аутрич в B2B: как мы довели клиента до отчаяния | https://vc.ru/id128425/1982841-kak-proval-holodnoj-b2b-rassylki-privel-k-uspehu-klienta | Respondo / Sherpa Robotics | 2025-05-14 | 2026-09-15 | вендор о клиенте | RU07: провал (<1%, баунс 12%) и исправление (~4%, 3 сделки) |
| Кейс Sherpa Robotics (интервью) | https://respondo.ru/cases/sherparpa | Respondo | н/д | 2026-09-15 | вендор о клиенте | RU07: 1000 компаний, цена лида 10 тыс. → 2 тыс. ₽ |
| Реанимировали базу: 305 лидов, 13 клиентов | https://vc.ru/marketing/2970627-kholodnaya-rassylka-dlya-reaktivatsii-bazy | Respondo / БИБИ КАР РУС | 2026-06-09 | 2026-09-15 | вендор о клиенте | RU08: реактивация, 5 писем, 305 лидов, 13 контрактов |
| Продажи крупным клиентам через холодные рассылки (TargetAI) | https://vc.ru/marketing/2712115-prodazhi-krupnym-klientam-cherez-holodnye-rassylki | Respondo / TargetAI | 2026-01-30 | 2026-09-15 | вендор о клиенте | RU09: 2–3 письма + мессенджер, 2–5% ответов, 30–40 из 100 встреч в продажу |
| Эффективность холодных рассылок: 7% конверсии (Completo) | https://vc.ru/marketing/1665855-effektivnost-holodnyh-rassylok-kak-dostich-7-konversii-v-lid-keis-b2b-agentstva-completo | Respondo / Completo | 2024-11-29 | 2026-09-15 | вендор о клиенте | RU10: 916 компаний, 3410 писем, 111 ответов, 65 лидов |
| Холодная B2B рассылка с конверсией 12% | https://respondo.ru/cases/completo | Respondo | н/д | 2026-09-15 | вендор о клиенте | RU10: ответы по шагам, принципы писем |
| Email-outreach для B2B (кейс Completo) | https://www.completo.ru/cases/email-outreach-dlya-b2b-kak-rasshirit-klientskuyu-bazu-s-pomoshchyu-kholodnoy-rassylki/ | Completo | н/д | 2026-09-15 | агентство о себе | RU10: 9 встреч, 2 предварительных согласия; длинные письма не сработали |
| Холодная email-рассылка B2B: кейс с конверсией 7% | https://uniseller.io/blog/kholodnye-pisma-b2b-1000-pisem-2-kontrakta/ | Uniseller | 2026-05-27 | 2026-09-15 | пересказ третьей стороны (SEO) | Вторичный пересказ RU10, как отдельный кейс не учтён |
| Служба доставки получает 50–60 лидов в месяц | https://respondo.ru/cases/courierist | Respondo / «Курьерист» | н/д | 2026-09-15 | вендор о клиенте | RU11: письмо «кто у вас отвечает за логистику?», 1259 ответов, ROI 1:7 |
| Запуск холодных продаж для Nutnet | https://respondo.ru/cases/nutnet | Respondo | н/д | 2026-09-15 | вендор о клиенте | RU12: >50 откликов, ICP по обороту |
| Логистическая компания: 55 лидов, 2 сделки | https://respondo.ru/cases/logistic | Respondo | н/д | 2026-09-15 | вендор о клиенте | RU13: 11 026 писем, 169 ответов, 55 лидов; своя база 7% против 3% |
| 6 пилотов для автоматизатора импорта | https://respondo.ru/cases/mycustoms | Respondo / MyCustoms | н/д | 2026-09-15 | вендор о клиенте | RU14: 985 компаний, ответы по шагам, 6 пилотов |
| CyberFirst: холодный email-аутрич в ИБ | https://timeweb.com/ru/community/articles/kak-it-kompaniyam-nahodit-klientov-v-informacionnoy-bezopasnosti-s-pomoshchyu-holodnogo-email-autricha | Respondo (Timeweb Community) | н/д | 2026-09-15 | вендор о клиенте | RU15: 1015 компаний, 3941 письмо, 82 ответа, 24 лида |
| Холодные рассылки для кибербезопасности | https://respondo.ru/cases/cyberfirst | Respondo | н/д | 2026-09-15 | вендор о клиенте | RU15: сбор базы по вакансиям |
| Интегратор 1С и Bitrix: 28 лидов | https://coldy.ai/case-studies/1c-bitrix-outreach-case | Coldy / «Поток B2B» | н/д | 2026-09-15 | вендор о клиенте | RU16: дословные письма; длинные и короткие не сработали |
| 3D-визуализация: 17 клиентов с выставок | https://coldy.ai/case-studies/3d-visualization-exhibitions-cold-outreach | Coldy / Polza | 2026-01-14 | 2026-09-15 | вендор о клиенте | RU17: 4 письма, 0,2% и 0,38% в лиды |
| 82 лида на лабораторное оборудование | https://coldy.ai/case-studies/82-leads-lab-equipment-email-outreach | Coldy / Polza | н/д | 2026-09-15 | вендор о клиенте | RU18: 16 700 контактов, 751 ответ, 82 заявки, 15 сделок |
| 62 лида на франшизу аптек | https://coldy.ai/case-studies/b2b-franchise-cold-email | Coldy / «Евклид» | н/д | 2026-09-15 | вендор о клиенте | RU19: 3% на прямых ЛПР против 1% на общих почтах |
| Зарядные станции: 90 лидов за месяц | https://coldy.ai/case-studies/charging-stations-outreach-case | Coldy / «Поток B2B» | н/д (кампания март–апрель 2026) | 2026-09-15 | вендор о клиенте | RU20: 7000+ компаний, 7% ответов, 1,26% в лиды, регуляторный триггер |
| 9 лидов в неделю на построение отделов продаж | https://coldy.ai/case-studies/cold-email-sales-department-case | Coldy / AbsLead | н/д | 2026-09-15 | вендор о клиенте | RU21: 5000 контактов, 4 письма, обход РОПа |
| Встречи на выставке через аутрич | https://coldy.ai/case-studies/cold-outreach-exhibition-meetings | Coldy / Валентин | н/д | 2026-09-15 | вендор о клиенте | RU22: email 27%, Telegram 40%, 20 встреч; баны на 3-м письме |
| Евклид: 160 лидов на поддержку сайтов | https://coldy.ai/case-studies/email-outreach-bitrix-support-agency-case | Coldy / «Евклид» | 2026-01-15 | 2026-09-15 | вендор о клиенте | RU23: 20 322 письма, 160 лидов, 15 продаж, пауза из-за LTV |
| Полидэк: 86 клиентов из старой базы | https://coldy.ai/case-studies/email-outreach-customer-reactivation-industrial-tools-case | Coldy / «Евклид» | н/д | 2026-09-15 | вендор о клиенте | RU24: 8372 компании, 432 ответа, 86 клиентов, +482 тыс. ₽ |
| Веб-студия: две клиники за месяц | https://coldy.ai/case-studies/email-outreach-for-webstudio | Coldy / Utop!a | 2025-03-04 | 2026-09-15 | вендор о клиенте | RU25: 428 получателей, 13 ответов, 2 сделки, затраты 6647 ₽ |
| 73 лида на выставочные стенды | https://coldy.ai/case-studies/exhibition-stand-email-outreach-case | Coldy / «Евклид» | н/д | 2026-09-15 | вендор о клиенте | RU26: 9300 компаний, 389 ответов, 73 лида, сделки 1,5 и 3,5 млн ₽ |
| 52 отклика на гибкую керамику | https://coldy.ai/case-studies/flexible-ceramics-email-outreach-case | Coldy / «Евклид» | н/д | 2026-09-15 | вендор о клиенте | RU27: 5627 компаний, 101 ответ, 52 лида |
| FIBBEE: 17 партнёров, 12,8% ответов | https://coldy.ai/case-studies/how-fibbee-found-partners-through-cold-outreach-polza-case | Coldy / Polza | н/д | 2026-09-15 | вендор о клиенте | RU28: полная цепочка из 6 писем, 406 писем |
| Кадровое агентство: 64 лида | https://coldy.ai/case-studies/hr-outreach-open-vacancies-case | Coldy / «Поток B2B» | н/д | 2026-09-15 | вендор о клиенте | RU29: письма по открытым вакансиям, 4 продажи |
| IT-аутстаффинг: 25 лидов | https://coldy.ai/case-studies/it-outstaffing-cold-email-case | Coldy / Steps | н/д | 2026-09-15 | вендор о клиенте | RU30: 1284 получателя, 4% ответов, цена в первом письме |
| Стримеры: 3 контракта на $150–200 тыс. | https://coldy.ai/case-studies/streamer-outreach-igaming-case | Coldy / LeadBridge | н/д | 2026-09-15 | вендор о клиенте | RU31: 749 контактов, 167 ответов, 38 встреч |
| 87 партнёров через госзакупки | https://coldy.ai/case-studies/b2b-partner-acquisition-cold-email | Coldy / LeadBridge | н/д | 2026-09-15 | вендор о клиенте | RU32: ~2000 писем, 150 ответов (итог сомнителен) |
| Каталог кейсов Coldy | https://coldy.ai/case-studies | Coldy | н/д | 2026-09-15 | вендор (каталог) | A12: заголовки непрочитанных кейсов |
| Инфраструктура холодной рассылки для узкого B2B | https://habr.com/ru/articles/1069906/ | Сайткрафт | 2026-08-13 | 2026-09-15 | агентство о клиенте | RU33: 6021 письмо, 204 ответа, 19 квал. лидов, лимиты, домены |
| 120+ встреч за 8 месяцев | https://habr.com/ru/articles/909358/ | Антон Фортин | 2025-05-14 | 2026-09-15 | агентство о себе | RU34: email 0,95% против Telegram; провалы в нишах |
| Аутрич, а не спам | https://habr.com/ru/articles/910712/ | Антон Фортин | н/д (2025) | 2026-09-15 | агентство о себе | Повтор RU34 |
| Как я разослал 6583 письма и заключил две сделки | https://texterra.ru/blog/email-marketing-rabotayut-li-kholodnye-rassylki.html | TexTerra (автор) | н/д | 2026-09-15 | независимый практик | RU35: 27 лидов, 2 договора, баунс 17%, дословное письмо |
| Кейс: холодная рассылка принесла 45 лидов | https://handbox.by/blog/kejs-xolodnaya-rassyilka-v-b2b-segmente-kotoraya-prinesla-45-lidov | HANDBOX (BY) | 2023-12-05 | 2026-09-15 | агентство о клиенте | RU36: 647 писем, 45 ответов |
| Email аутрич: кейсы | https://calltalk.ru/keyses/ | Call-Talk | н/д | 2026-09-15 | агентство о себе (SEO-признаки) | RU37: 5 анонимных кампаний, цена лида и сделки по нишам |
| Кейсы SalesNotes | https://salesnotes.ru/cases | SalesNotes | н/д | 2026-09-15 | агентство о себе | RU38: сводки (16,2% и 16,6% ответов) |
| Open rate 80–90% в b2b | https://vc.ru/marketing/637516-kak-zapuskat-holodnye-email-rassylki-v-b2b-chtoby-poluchat-open-rate-80-90-i-desyatki-kvalificirovannyh-lidov | SalesNotes (Тарас Алтунин) | 2023-03-20 | 2026-09-15 | агентство о себе | RU38: методика, IT-аутсорс 86%/12% |
| Кейс IT-аутсорса (фрагмент) | https://salesnotes.ru/ak-poluchit-86-open-rate-i-12-reply-rate-v-nishe-prodazh-it | SalesNotes | н/д | 2026-09-15 | агентство о себе | RU38: блэклист нового домена |
| Холодная рассылка в B2B: конверсия 10–20% | https://vc.ru/marketing/882350-holodnaya-rassylka-v-b2b-kak-sdelat-ee-pravilno-chtoby-poluchit-konversiyu-v-10-20-otvetov-teplye-lidy-i-prodazhi | Respondo | 2023-10-18 | 2026-09-15 | вендор (гайд) | Методика Respondo: 3–5 писем для РФ, выбор адреса |
| ИИ-агент для холодных рассылок по вузам | https://vc.ru/marketing/3095638-ii-agent-dlya-holodnyh-rassylok-po-vuzam | Enbisys | 2026-08-25 | 2026-09-15 | практик о себе | A02 |
| IT-интегратор (Advalange) | https://coldy.ai/case-studies/email-outreach-for-software-integrator | Coldy | н/д | 2026-09-15 | вендор о клиенте | A01 |
| Сравнение холодных звонков и переписок | https://habr.com/ru/articles/506494/ | Юрфирма (Habr) | 2020-06-12 | 2026-09-15 | практик о себе | A03 (LinkedIn) |
| Belkins: Case studies (список) | https://belkins.io/case-studies | Belkins | н/д | 2026-09-15 | агентство о себе | Итоговые цифры W04, W06, W24, W25 |
| Lead Generation for Consumer Trends Research Company | https://belkins.io/case-studies/lead-generation-for-consumer-trends-research-company | Belkins | н/д | 2026-09-15 | агентство о клиенте | W01: 77 встреч, 2 сделки |
| Event-based cold outreach (GE HealthCare) | https://belkins.io/case-studies/lead-generation-for-a-medical-technology-company | Belkins | н/д | 2026-09-15 | агентство о клиенте | W02: 135 встреч, reply и positive по 4 конференциям |
| Fire safety and security service | https://belkins.io/case-studies/lead-generation-for-a-fire-safety-and-security-service | Belkins | н/д | 2026-09-15 | агентство о клиенте | W03: 341 встреча, >$300 тыс., CTA дословно |
| Signage manufacturer | https://belkins.io/case-studies/omnichannel-lead-generation-for-a-signage-manufacturer | Belkins | н/д | 2026-09-15 | агентство о клиенте | W04: ~6000 контактов, ~17 встреч, $575 тыс. |
| 10 appointments in 24 hours | https://belkins.io/case-studies/how-an-opportunity-brought-belkins-10-appointments-in-24-hours | Belkins | н/д | 2026-09-15 | агентство о себе | W05: 250 компаний, 6 встреч + 4 звонка |
| 150 meetings and 14 deals (solar) | https://belkins.io/case-studies/150-meetings-and-14-deals-for-a-solar-energy-company | Belkins | н/д | 2026-09-15 | агентство о клиенте | W06: персонализация расчётом крыши |
| Video production agency | https://belkins.io/case-studies/lead-generation-for-video-production-agency | Belkins | н/д | 2026-09-15 | агентство о клиенте | W24: что не сработало (referral, ABM) |
| Fired heater service provider | https://belkins.io/case-studies/lead-generation-for-fired-heater-service-provider | Belkins | н/д | 2026-09-15 | агентство о клиенте | W25: 77 кампаний, подходы |
| Meeting Email Case Study: 20% Booking Rate Framework | https://instantly.ai/blog/meeting-email-case-study-20-booking-rate-framework/ | Instantly | 2026-02-24 | 2026-09-15 | вендор (анонимный клиент) | W07: 4,2% → 9,7%, 8 → 42 встречи |
| Cold Email Case Study: 97% More Appointments After 1 A/B Test | https://mailshake.com/blog/cold-email-ab-test/ | Mailshake | 2026-02-01 | 2026-09-15 | вендор + агентство | W08: 206 проспектов, 30% ответов, дословные варианты |
| 4897 Cold Emails Sent – What Worked, What Didn’t | https://www.crazyeyemarketing.com/blog/case-study-4897-cold-emails-sent-what-worked-what-didnt/ | Crazy Eye Marketing | 2016-03-30 | 2026-09-15 | независимый практик | W09: тест 5 серий, победила просьба о 15 минутах |
| 6 Cold Email Case Studies with Great Reply Rates | https://www.levelingup.com/casestudies/6-cold-email-case-studies-great-reply-rates/ | LevelingUp / Single Grain | 2016-12-15 | 2026-09-15 | пересказ третьей стороны | W10–W12, A09, A10; текст письма W09 |
| How a B2B Podcasting Agency Booked 40 Sales Calls | https://borks.io/blog/podcasting-agency-40-calls-cold-email | Borks | 2026-04-15 | 2026-09-15 | агентство о клиенте | W13: сигнал LinkedIn, 14 200 писем, 40 встреч, 9 клиентов |
| B2B Case Study: Small IT Companies… (Foxit) | https://medium.com/@salesar/b2b-case-study-how-small-it-companies-gain-markets-through-precision-cold-outreach-5888fe1f10a7 | SalesAR | 2025-11-06 | 2026-09-15 | агентство о клиенте | W14: 3000 контактов, 4% ответов, 32 встречи |
| Cold Email B2B Lead Generation Hacks | https://salesar.io/blog/b2b-lead-generation-hacks | SalesAR | н/д | 2026-09-15 | агентство о себе | A08 |
| Last month I sent 4285 cold emails | https://www.linkedin.com/posts/joehead1_last-month-i-sent-4285-cold-emails-heres-activity-7384845992665174016-Az2P | Joe Head | н/д | 2026-09-15 | независимый практик | W15: 11% ответов, 3 звонка, 2 клиента |
| We send 30K cold emails a month for Vidico | https://www.linkedin.com/posts/taylorharen_we-send-30k-cold-emails-a-month-for-vidico-activity-7287890524034719744-Shv9 | Taylor Haren | н/д | 2026-09-15 | агентство о клиенте | W16: 6–10% положительных, 39 встреч за 30 дней |
| B2B SaaS case study (post) | https://www.linkedin.com/posts/rozana-petrovska_a-b2b-saas-founder-came-to-us-frustrated-activity-7367179257879420929-9HDL | Rozana Petrovska | н/д | 2026-09-15 | агентство о клиенте | W17: 23 встречи, €184 тыс. воронки |
| Tirvio case study | https://www.smartlead.ai/case-study/tirvio | Smartlead | н/д | 2026-09-15 | вендор о клиенте | W18: 35% положительных, 5 контрактов за 3 недели |
| Danish Lead Co. case study | https://www.smartlead.ai/case-study/danish-lead-co-martin-rasmussen | Smartlead | н/д | 2026-09-15 | вендор о клиенте | W19: 50–500 писем на положительный ответ |
| G7 Logistics Networks: Freight Forwarding Cold Email Results | https://leadgenjay.com/results/g7-logistics-networks | Lead Gen Jay | 2026-03-23 | 2026-09-15 | агентство о клиенте | W20: 61 тыс. писем, 1,85% ответов, 79 возможностей |
| Imaginaire Digital Agency’s Cold Email Strategy | https://woodpecker.co/blog/case-study-imaginaire/ | Woodpecker | 2018-05-17 | 2026-09-15 | вендор о клиенте | W21: 3 письма, 5–10% положительных, CAC ~$90 |
| The 7-Part Cold Email Structure That Got Us a 50% Reply Rate | https://www.lemlist.com/blog/email-structure | lemlist | обновлено 2026-09-04 | 2026-09-15 | вендор о себе | W22: 60 писем, 50% ответов |
| Cold email templates: 12 that book meetings (2026) | https://www.reachly.co/blogs/cold-email-templates | Reachly | 2026-05-28 | 2026-09-15 | агентство о себе | W23: 0,5–1% → 1,6% после смены оффера; Primal 85 SQL |
| Grow case study | https://www.cience.com/case-studies/grow/ | CIENCE | 2025-06-15 | 2026-09-15 | агентство о клиенте | A04 |
| August Ash case study | https://www.cience.com/case-studies/august-ash/ | CIENCE | н/д | 2026-09-15 | агентство о клиенте | A05 |
| Wyngman Agency case study | https://www.smartlead.ai/case-study/case-study-wyngman-agency | Smartlead | н/д | 2026-09-15 | вендор о клиенте | A06 |
| Profit Labs AI case study | https://www.smartlead.ai/case-study/case-study-robert-bradley | Smartlead | н/д | 2026-09-15 | вендор о клиенте | A07 |
| 6 Best B2B Cold Email Agencies for SaaS (2026) | https://snipeoutbound.com/blog/best-cold-email-agencies-b2b-saas/ | Snipe Outbound | н/д (проверено 2026-08-31) | 2026-09-15 | агентство о себе | A11; описание моделей Belkins, CIENCE, SalesBread |
| Top 10 Cold Email Agencies That Get Replies [2026] | https://salesbread.com/cold-email-agencies/ | SalesBread | н/д | 2026-09-15 | агентство о себе | Контекст: мнение, что массовый email требует рынка ≥5000 аккаунтов; 19,98% ответов в LinkedIn (данные агентства) |
