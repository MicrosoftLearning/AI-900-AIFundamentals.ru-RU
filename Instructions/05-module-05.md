---
lab:
  title: Изучение генеративного искусственного интеллекта с помощью Bing Copilot
---

В этом упражнении вы узнаете, как создать искусственный интеллект с помощью Bing Copilot. 

## Перед началом работы
Вам понадобится личная учетная запись Майкрософт. Если у вас ее нет, перейдите к [signup.live.com](https://signup.live.com/signup?azure-portal=true), чтобы зарегистрироваться.

# Изучение генеративного искусственного интеллекта с помощью Bing

1. Откройте [Bing.com](https://www.bing.com?azure-portal=true) и войдите с помощью личной учетной записи Майкрософт.

**Примечание**: Хотя вы можете войти с помощью рабочей или учебной учетной записи, вы увидите немного другой интерфейс пользователя по сравнению с входом с помощью личной учетной записи. Используя рабочую или учебную учетную запись вы увидите чат Bing Enterprise. 

1. Выберите **Чат** в меню в верхней части экрана. Чат переносит вас в Bing Copilot, который использует генеративный ИИ для улучшения результатов поиска. Это означает, что в отличие от самостоятельного поиска, который возвращает существующее содержимое, Bing Copilot может объединить новые ответы на основе моделирования естественного языка и информации в Интернете.  
    
1. В нижней части экрана появится окно **Задайте любой вопрос**. При вводе запросов в окно Bing Copilot использует всю цепочку беседы для возврата ответов. Например, давайте попробуем задать ряд вопросов о путешествиях. 

## Использование запросов для создания ответов

1. Введите запрос: `What are 3 pros and cons of traveling in the winter?`. Перед ответом появится *Поиск:...* и *Создание...*. Модель использует искомые ответы в качестве базовой информации для создания оригинальных ответов. Обратите внимание, что конец ответа содержит ссылки на источники. 

![Снимок экрана: ответ от Bing copilot на запрос о путешествиях с тремя маркерами преимуществ и тремя маркерами недостатков.](../media/generative-ai/bing-copilot-response-traveling.png) 

**Примечание**: Если вы еще не видите сообщение **Создание...* или ответ списка маркеров, значит, вы еще не видели Bing Copilot в действии. Вам необходимо вернуться в меню входа и связать текущую учетную запись, которую вы используете, с личной учетной записью. 
 
1. Введите запрос: `Find me 3 more pros`. Под этим запросом вы имеете в виду, что хотели бы увидеть еще 3 положительные причины для путешествий зимой, которые еще не были перечислены. Обратите внимание, что с помощью этого запроса вы просите Bing Copilot выполнить два действия, которые не делает сам поиск: использовать предыдущий ответ чата, чтобы исключить то, что было возвращено в новом ответе, и использовать тему предыдущего чата без явного указания. 

1. Введите запрос: `Where are 3 places I can go to find fewer crowds?`. 

**Примечание**: Обратите внимание, что в то время как Bing Copilot может дать связанный ответ, он может удалить более ранние "воспоминания" цепочки беседы по мере ее продолжения. В результате ответы, которые вы получаете, могут не быть напрямую связаны с путешествием в зимний период. Это в значительной степени связано с ограничениями ввода маркеров. Когда чат "запоминает" предыдущие части беседы, причиной этого является то, что он сохранил определенное количество маркеров из беседы. По мере того, как новые маркеры будут вводиться через ваши новые запросы и ответы, чат будет удалять старые маркеры. 

1. Кнопка **Новая тема** рядом с окном чата полезна для очистки предыдущей цепочки беседы, чтобы ответы на новые темы не основывались на предыдущей. Чтобы очистить журнал сообщений, используйте значок **Новая тема** рядом с окном чата. 

## Попробуйте создание изображения

1. Теперь давайте рассмотрим пример создания изображений. Введите запрос: `Create an image of an elephant eating a hamburger`. Обратите внимание, что перед тем, как Bing Copilot вернет ответ, появится сообщение *Я попробую создать это...*. 

![Снимок экрана: слоны едят гамбургеры.](../media/generative-ai/dall-e-elephant.png)

Важно отметить, что ответ может выглядеть похожим, но не таким же. Причиной этого является то, что ответы будут разными.  

1. В ответе внизу есть текст "Powered by DALL-E". Рассмотрим, как DALL-E основан на больших языковых моделях, поскольку вводимые вами тексты на естественном языке генерируют изображения. 

1. Вернитесь в чат Bing Copilot, щелкнув значок Microsoft Bing в правом верхнем углу экрана. 

## Попробуйте сгенерировать код

1. Теперь давайте посмотрим пример создания и перевода кода. Введите запрос: `Use Python to create a list`. 

1. Введите запрос: `Translate that into C#`. Обратите внимание, что вам не нужно было указывать, что такое "that" (это), поскольку Bing Copilot знает, что это, ссылаясь на историю беседы. 

## Bonus 

1. Введите запрос: `What are 3 examples of generative AI helping people?`. Вы можете использовать это в качестве способа мозгового штурма ваших собственных идей copilot!  

