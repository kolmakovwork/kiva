# EDA краудфандинговой платформы kiva.org
**Статус проекта:** Завершен.

**Навыки и инструменты:** Python: pandas, datetime, numpy, matplotlib, seaborn, plotly, scipy, squarify, WordCloud, Counter.

### В репозитории:
1. 15_masterskaya_kiva_portfolio.ipynb - jupyter notebook c EDA
2. kiva.zip (35 Мб) - внутри датасет kiva.csv (190мб). Сразу читаем .zip - экономит место в 5 раз. Взят с Kaggle, обогащается индексом бедности страны.
3. population.xlsx - население стран с википедии для обогащения датасета https://en.wikipedia.org/wiki/List_of_countries_and_dependencies_by_population

## Контекст проекта


Kiva основана в 2005 году в Сан-Франциско. Краудфандинговая платформа kiva.org ставит своей целью предоставление финансовых услуг (займы) наиболее нуждающимся и необеспеченным людям в основном из бедных стран. Заёмщики оставляют заявку на сайте, доноры поддерживают её  финансово, на месте партнёр организации выдаёт кредит, который погашается из этих средств, которые донорам возвращаются уже заёмщиками через платформу.

Представленный компанией датасет за 2014-2017гг. содержит информацию об успешных займах на различные проекты в 85 разных странах.

## Цели исследования:

1. Выявить от каких  характеристик зависит скорость набора средств на заявку (разница между временем, когда заявка опублирована на сайте и средства на неё собраны)
2. Анализ заявок и индекса бедности, дать рекомендации о тех странах, на которые Kiva стоит обратить внимание.
3. Общее EDA: Проанализировать пол заемщиков, доля заёмщиков-женщин в разрезе основной религии, активность Kiva и заявителей в разрезе стран, частота полного финансирования.
4. Сформировать и проверить гипотезы и равенстве средних по заёмщикам-женщинам

## Описание данных:
Датасет kiva.csv с исполненными заявками за 2014-2017гг.

- id —  идентификатор заявки-кредита;
- funded_amount - сумма сбора (выдается агенту, USD);
- loan_amount - сумма запрашиваемого займа (от агента заемщику, USD) (loan_amount=funded_amount)
- activity - подсектор применения
- sector - сектор применения
- use - назначение-описание использования
- country_code - ISO-код страны страны, в которой выдан кредит
- country - название страны, в которой выдан кредит
- region - регион в стране
- currency - местная валюта (не интересует)
- partner_id - номер партнера, выдающий кредит
- posted_time - время публикации заявки на сайте
- disbursed_time - время предоставления кредита
- funded_time - время когда собрали денежные средства (может быть раньше даты заявки)
- term_in_months - срок в месяцах, на который был выдан кредит
- lender_count -кол-во кредиторов
- tags - тэги по сайту
- borrower_genders - пол заемщика(ов)
- repayment_interval - регулярность выплат:
    * bullet - единовременное погашение
    * weekly - еженедельно
    * monthly -ежемесячно
    * irregular - нерегулярно
- date - дата (в формате гггг-мм-дд) (предположительно = posted_time)
- main_country_religion - главная религия страны:
    * Christians - христиане
    * Muslims - мусульмане
    * Buddhists - буддисты
    * Hindus - индусы
    * Folk Religions - народные религии
    * Jews - евреи
    * Unaffiliated -неаффилированные

## Общий вывод: 
Было выявлено от каких  характеристик зависит скорость набора средств на заявку, даны рекомендации о тех странах на которые Kiva стоит обратить внимание, проведено общее EDA, проверены гипотезы по заёмщикам-женщинам.
Более подробно можно посмотреть в проекте.
