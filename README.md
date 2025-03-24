#  Текстовая классификация с использованием BERT и RoBERTa на датасете AG News

##  Цель проекта
Цель проекта — получить **практический опыт работы с LLM (Large Language Models)**, таких как **BERT** и **RoBERTa**, на реальной задаче классификации текста.  
Этот проект стал первым шагом в освоении трансформеров и библиотеки 🤗 Hugging Face.

---

##  Описание задачи
Классификация коротких новостных текстов на одну из четырёх категорий:

-  World
-  Sports
-  Business
-  Sci/Tech

Использован датасет [AG News](https://huggingface.co/datasets/ag_news), содержащий ~120,000 текстов.

---

##  Используемые технологии

-  Transformers (Hugging Face)
- `bert-base-uncased` и `roberta-base`
- PyTorch
- Hugging Face `Trainer` API
- `scikit-learn` для оценки метрик
- Google Colab + GPU (Tesla T4)

---

##  Этапы работы

1. Загрузка и объединение `train` и `test` частей AG News
2. Стратифицированное разбиение на train/validation
3. Токенизация текстов с использованием соответствующего токенайзера
4. Обучение модели через `Trainer`
5. Оценка качества: Accuracy, F1-score, Confusion Matrix

---

##  Результаты

###  Accuracy и F1-score

| Модель           | Accuracy | Macro F1 |
|------------------|----------|----------|
| `bert-base`      | 95.2%    | 0.95     |
| `roberta-base`   | 95.1%    | 0.95     |

###  Подробности (`roberta-base`):

| Класс     | Precision | Recall | F1-score |
|-----------|-----------|--------|----------|
| World     | 0.96      | 0.95   | 0.96     |
| Sports    | 0.99      | 0.99   | 0.99     |
| Business  | 0.93      | 0.92   | 0.93     |
| Sci/Tech  | 0.92      | 0.94   | 0.93     |

###  Confusion Matrix

(Добавь сюда изображение или ссылку на `confusion_matrix.png`)

---

##  Выводы

- ✅ Hugging Face `Trainer` позволяет легко применять LLM к реальным задачам
- ✅ `bert-base-uncased` показал отличное качество и высокую скорость
- ✅ `roberta-base` дал аналогичный результат, подтверждая стабильность подхода
- ✅ Модель готова для использования в проде, дообучения, или интеграции в ML-сервисы

---
