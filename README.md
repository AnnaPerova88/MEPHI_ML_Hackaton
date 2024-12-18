# MEPHI_ML_Hackaton

# Виртуальный гид по Пушкинскому музею

Этот проект представляет собой веб-приложение, которое позволяет пользователям взаимодействовать с коллекцией картин Пушкинского музея с помощью чат-бота и распознавания изображений. Пользователи могут задать вопросы о картинах и получать ответы через текстовые или голосовые команды. Также приложение позволяет наводить телефон на картины в музее и получать информацию о них.

## Технологии

### 1. **ML Stack**

В проекте будут использоваться несколько моделей и технологий машинного обучения для обработки текста, распознавания речи и изображений. Рассмотрим каждый из компонентов:

#### 1.1. **GiGaChat** — для генерации ответов на вопросы (Natural Language Processing, NLP)

**GiGaChat** — это мощная модель для генерации текста и диалогов. Она используется для обработки текстовых запросов от пользователя и генерации ответов на вопросы о картинах.

- **Задача**: Обработка вопросов на естественном языке (например, "Кто автор картины 'Девочка на шаре'?") и генерация ответов.
- **Модель**: Для этого используется модель от Hugging Face, такая как **GPT-3** или **GiGaChat**, которая обучена на большом объеме данных для генерации релевантных и содержательных ответов.
- **Использование**: Модель будет отвечать на вопросы, используя API Hugging Face.

**Как использовать**:
- Для этого проекта используется **Hugging Face API** для доступа к модели.
- Регистрация на [Hugging Face](https://huggingface.co/) и получение API ключа необходимы для работы с моделью.

Пример кода для использования GiGaChat:

```javascript
// Пример запроса к Hugging Face API
const response = await axios.post('https://api-inference.huggingface.co/models/your_model', {
    inputs: question
}, {
    headers: { Authorization: `Bearer ${YOUR_HUGGING_FACE_API_KEY}` }
});
