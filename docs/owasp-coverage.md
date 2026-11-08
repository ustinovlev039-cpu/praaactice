[← На главную](../README.md) · [Веб-лабораторные](../labs/web/README.md)

# Карта OWASP Top 10:2025

В теоретическом файле `785_OWASP_Top_10.md` архива используется редакция **2025**. Ниже сохранена именно она, сверенная с [официальным перечнем OWASP](https://top10.owasp.org/2025/).

OWASP Top 10 — категории риска, а не десять отдельных техник эксплуатации. Привязка зависит от первопричины конкретной реализации. Наличие XSS, SQLi и SSTI не означает прохождение трёх разных категорий.

| Категория | Практика из архива | Граница покрытия |
| :-- | :-- | :-- |
| A01 · Broken Access Control | [IDOR](../labs/web/04-idor/README.md), [Directory Traversal](../labs/web/06-directory-traversal/README.md), [LFI](../labs/web/05-lfi/README.md) | Объектные права и границы файлового доступа |
| A02 · Security Misconfiguration | [XXE](../labs/web/09-xxe/README.md), [SAST](../labs/web/13-sast/README.md) | Настройки XML-парсера и учебного Flask-приложения |
| A03 · Software Supply Chain Failures | Теоретический блок | Отдельной практической лабораторной в веб-главе нет |
| A04 · Cryptographic Failures | Теоретический блок | Отдельной практической лабораторной в веб-главе нет |
| A05 · Injection | [XSS](../labs/web/02-xss/README.md), [SQLi](../labs/web/03-sql-injection/README.md), [Command Injection](../labs/web/07-command-injection/README.md), [Code Injection](../labs/web/08-code-injection/README.md), [SSTI](../labs/web/10-ssti/README.md) | Несколько контекстов внедрения; не исчерпывающее покрытие категории |
| A06 · Insecure Design | [Race Condition](../labs/web/11-race-condition/README.md) | Проверка бизнес-инварианта и атомарности операции |
| A07 · Authentication Failures | Теория; смежные сетевые кейсы подбора паролей | Не заявляется как отдельная веб-практика |
| A08 · Software or Data Integrity Failures | Теоретический блок | Отдельной практической лабораторной в веб-главе нет |
| A09 · Security Logging and Alerting Failures | [Журналы WAF](../labs/web/14-waf-safeline/README.md) | Работа с журналами; не полноценный тест всех отказов детектирования |
| A10 · Mishandling of Exceptional Conditions | Теоретический блок | Отдельной практической лабораторной в веб-главе нет |

## Сквозные инструменты

[Burp Suite](../labs/web/01-burp-http/README.md) помогает воспроизводить запросы, [Bandit и Semgrep](../labs/web/13-sast/README.md) — искать потенциальные проблемы в коде, [DefectDojo](../labs/web/12-defectdojo/README.md) — разбирать находки, [SafeLine](../labs/web/14-waf-safeline/README.md) — проверять дополнительный защитный слой. Инструмент не является самостоятельной категорией риска.

В архиве также есть четыре теста: классификация уязвимостей, OWASP Top 10, методология тестирования и OWASP WSTG. Они учтены в [карте источников](source-map.md), но не включены в число 14 практических лабораторных.
