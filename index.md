---
title: Инструкции в Интернете
permalink: index.html
layout: home
---

# Упражнения по основам ИИ Azure

В этом репозитории содержатся практические лабораторные занятия для курса [AI-900 *Microsoft Azure Artificial Intelligence*](https://docs.microsoft.com/ru-ru/learn/certifications/courses/ai-900t00) и соответствующие модули для самостоятельного изучения на ресурсе Microsoft Learn: [Начало работы с искусственным интеллектом в Azure](https://docs.microsoft.com/learn/paths/get-started-with-artificial-intelligence-on-azure/), [Создание прогнозных моделей без кода в машинном обучении Azure](https://docs.microsoft.com/ru-ru/learn/paths/create-no-code-predictive-models-azure-machine-learning/),  [Изучение компьютерного зрения в Microsoft Azure](https://docs.microsoft.com/learn/paths/explore-computer-vision-microsoft-azure/), [Изучение обработки естественного языка](https://docs.microsoft.com/learn/paths/explore-natural-language-processing/) и [Изучение ИИ для общения](https://docs.microsoft.com/learn/paths/explore-conversational-ai/). Упражнения прилагаются к обучающим материалам и позволяют практиковаться с использованием описанных в них технологий. 

Для выполнения этих упражнений вам понадобится подписка Microsoft Azure. Если ваш инструктор не предоставил вам такую подписку, можете зарегистрироваться для получения бесплатной пробной версии на сайте [https://azure.microsoft.com](https://azure.microsoft.com).

{% assign labs = site.pages | where_exp:"page", "page.url contains '/instructions'" %}
| Упражнения |
| ------- | 
{% for activity in labs  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
