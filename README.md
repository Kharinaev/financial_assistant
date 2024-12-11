# financial_assistant

## Abstract

В данном проекте исследовано применение Retrieval-Augmented Generation (RAG) для повышения качества ответов больших языковых моделей (LLM) в финансовой сфере, с акцентом на российский фондовый рынок. Используются вопросы теста для неквалифицированных инвесторов от Центрального Банка России и материалы из релеватных курсов для демонстрации того факта, что добавление релевантного контекста повышает точность ответов, особенно для малых моделей

## Структура репозитория

- **notebooks**: Jupyter Notebook для различных этапов работы с данными и моделями
  - [`01-parse-md.ipynb`](notebooks/01-parse-md.ipynb): Предобработка данных (документов)
  - [`02-parse-questions.ipynb`](notebooks/02-parse-questions.ipynb): Предобработка данных (вопросов)
  - [`03-plain-llm.ipynb`](notebooks/03-plain-llm.ipynb): Генерация ответов LLM без контекста
  - [`04-rag.ipynb`](notebooks/04-rag.ipynb): Реализация RAG
  - [`05-res-analysis.ipynb`](notebooks/05-res-analysis.ipynb): Анализ результатов

- **artifacts/prompts**: Шаблоны используемых промптов
  - [`system_v1.md`](artifacts/prompts/system_v1.md): Системный промпт
  - [`v1.md`](artifacts/prompts/v1.md): Базовый шаблон
  - [`rag_v1.md`](artifacts/prompts/rag_v1.md): Шаблон для RAG

- **data**: Данные, используемые в проекте
  - [`alfa_invest_advanced_paragraphs.csv`](data/alfa_invest_advanced_paragraphs.csv): Статьи курса для продвинутых
  - [`alfa_invest_begginer_paragraphs.csv`](data/alfa_invest_begginer_paragraphs.csv): Статьи курса для начинающих
  - **test_qual_investor**
    - [`chapters.json`](data/test_qual_investor/chapters.json): Главы теста
    - [`questions.json`](data/test_qual_investor/questions.json): Вопросы теста
