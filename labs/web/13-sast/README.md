# Bandit и Semgrep: SAST и импорт результатов

## Схема

```mermaid
flowchart LR
    n0["Код NetTool"]
    n1["Bandit и Semgrep"]
    n2["JSON-отчёты"]
    n3["DefectDojo и триаж"]
    n0 --> n1 --> n2 --> n3
```

## Что сделал

- Запустил Bandit и Semgrep на учебном Python-приложении и сохранил JSON-отчёты.
- Импортировал результаты в DefectDojo.
- Сопоставил находки анализаторов и разобрал дубли и различия покрытия.
