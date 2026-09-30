# Анализ цен на бриллианты / Diamond Price Analysis

## 🇷🇺 Описание проекта

Данный проект посвящен исследовательскому анализу данных (EDA) и построению модели машинного обучения для прогнозирования цен на бриллианты.

**Цель проекта:**
Проанализировать датасет с характеристиками почти 54 000 бриллиантов, выявить ключевые факторы, влияющие на цену, и построить модель, способную точно предсказывать стоимость бриллианта на основе его характеристик.

**Основные признаки:**
- `carat`: вес бриллианта.
- `cut`: качество огранки.
- `color`: цвет бриллианта.
- `clarity`: чистота бриллианта.
- `x`, `y`, `z`: размеры в мм.
- `price` (целевая переменная): цена в долларах США.

**Используемые технологии:**
*   **Язык программирования:** Python
*   **Библиотеки для анализа данных:** Pandas, NumPy
*   **Библиотеки для визуализации:** Matplotlib, Seaborn
*   **Машинное обучение:** Scikit-learn (RandomForestRegressor, RobustScaler)
*   **Среда разработки:** Jupyter Notebook в VS Code
*   **Инструменты BI:** Power BI, DuckDB, DBeaver (использовались для дополнительного анализа и визуализации)

**Основные этапы работы:**
1.  **Загрузка и первичный осмотр данных.**
2.  **Исследовательский анализ данных (EDA):**
    *   Анализ распределения признаков.
    *   Выявление и обработка выбросов.
    *   Построение корреляционной матрицы и тепловых карт.
    *   Визуализация зависимостей цены от различных характеристик (вес, огранка, цвет, чистота).
3.  **Предобработка данных:**
    - Удаление неинформативных столбцов (`depth`, `table`).
    - Кодирование категориальных признаков (`cut`, `color`, `clarity`) с помощью `OrdinalEncoder` с сохранением иерархии.
4.  **Feature Engineering:** Создание новых признаков (`table_xy`, `depth_z`).
5.  **Построение модели машинного обучения:**
    *   Кодирование категориальных признаков с помощью `OrdinalEncoder`.
    *   Масштабирование данных с помощью `RobustScaler`.
    *   Обучение модели `RandomForestRegressor`.
    *   Оценка точности модели с помощью метрики R².

**Результаты:**
*   Выявлено, что наибольшее влияние на цену бриллианта оказывают его вес (carat) и геометрические размеры (x, y, z).
*   Построена модель `RandomForestRegressor`, которая показала высокую точность прогнозирования (R² ≈ 0.98).

---

## 🇬🇧 Project Description

This project is dedicated to Exploratory Data Analysis (EDA) and building a machine learning model to predict diamond prices.

**Project Goal:**
To analyze a dataset of nearly 54,000 diamonds, identify the key factors influencing price, and build a model that can accurately predict a diamond's value based on its characteristics.

**Technologies Used:**
*   **Programming Language:** Python
*   **Data Analysis Libraries:** Pandas, NumPy
*   **Visualization Libraries:** Matplotlib, Seaborn
*   **Machine Learning:** Scikit-learn (RandomForestRegressor, RobustScaler)
*   **Development Environment:** Jupyter Notebook in VS Code
*   **BI Tools:** Power BI, DuckDB, DBeaver (used for additional analysis and visualization)

**Key Steps:**
1.  **Data Loading and Initial Inspection.**
2.  **Exploratory Data Analysis (EDA):**
    *   Analysis of feature distributions.
    *   Outlier detection and handling.
    *   Building a correlation matrix and heatmaps.
    *   Visualization of price dependencies on various characteristics (carat, cut, color, clarity).
3.  **Feature Engineering:** Creating new features (`table_xy`, `depth_z`).
4.  **Machine Learning Model Building:**
    *   Encoding categorical features using `OrdinalEncoder`.
    *   Data scaling using `RobustScaler`.
    *   Training a `RandomForestRegressor` model.
    *   Evaluating model accuracy using the R² metric.

**Results:**
*   It was found that the most significant factors affecting diamond price are carat and geometric dimensions (x, y, z).
*   A `RandomForestRegressor` model was built, demonstrating high prediction accuracy (R² ≈ 0.98).

---
### **Как запустить проект / How to Run**
1.  Установите необходимые библиотеки: `pip install -r requirements.txt` (см. файл `requirements.txt`).
2.  Откройте файл `diamonds_analysis.ipynb` в Jupyter Notebook или VS Code.
3.  Запустите все ячейки ноутбука.