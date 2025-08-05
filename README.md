## Корреляция событий с использованием скрытых марковских моделей (HMM)
Этот проект посвящён разработке метода корреляции событий информационной безопасности с использованием **скрытых марковских моделей**. В рамках проекта исследуются алгоритмы и структура системы, способной анализировать последовательности событий и предсказывать как состояния системы, так и будущие события.

## Цель проекта

Разработка концепции и архитектуры инструмента для корреляции событий с помощью HMM, включая:

- выявление зависимостей между событиями ИБ;
- прогнозирование:
  - всех возможных состояний (**All States**),
  - текущего состояния (**Current State**),
  - следующего состояния (**Next State**),
  - следующего события (**Next Observation**).

## Алгоритмы

В модели используются комбинации следующих алгоритмов:

| Задача | Инициализация | Обучение |
|--------|----------------|----------|
| Прогнозирование состояний | EM (Expectation-Maximization) | SKM (Segmental K-Means) |
| Прогнозирование событий   | EM (Expectation-Maximization) | BW (Baum-Welch)         |

- **EM** – вычисление начальных параметров модели на основе наблюдений.
- **SKM** – ускоренное обучение состояний с использованием сегментного K-среднего.
- **BW** – алгоритм, использующий ожидания для обучения вероятностей наблюдений.

## Описание

В `math_foundations` расположено описание математической части метода.
В `diagrams` представлены блок-схемы работы метода.

## Источники

1. Chadza T., Kyriakopoulos K. G., Lambotharan S. Analysis of hidden Markov model learning algorithms for the detection and prediction of multi-stage network attacks //Future generation computer systems. – 2020. – Т. 108. – С. 636-649.
2. Kotenko I., Chechulin A. A cyber attack modeling and impact assessment framework //2013 5th International Conference on Cyber Conflict (CYCON 2013). – IEEE, 2013. – С. 1-24.
3. Shawly T. et al. Architectures for detecting interleaved multi-stage network attacks using hidden Markov models //IEEE Transactions on Dependable and Secure Computing. – 2019. – Т. 18. – №. 5. – С. 2316-2330.
4. Chadza T., Kyriakopoulos K. G., Lambotharan S. Analysis of hidden Markov model learning algorithms for the detection and prediction of multi-stage network attacks //Future generation computer systems. – 2020. – Т. 108. – С. 636-649.