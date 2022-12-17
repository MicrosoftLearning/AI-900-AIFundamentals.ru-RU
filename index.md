---
title: 'Инструкции, размещенные в Интернете'
permalink: index.html
layout: home
---

# <a name="azure-ai-fundamentals-exercises"></a>Упражнения по основам ИИ Azure

Эти практические упражнения предназначены для поддержки обучающих материалов в [Microsoft Learn](https://docs.microsoft.com/training/).

Для выполнения этих упражнений вам понадобится подписка Microsoft Azure. Зарегистрироваться для получения бесплатной пробной версии можно по адресу [https://azure.microsoft.com](https://azure.microsoft.com).

{% assign labs = site.pages | where_exp:"page", "page.url contains '/instructions'" %}
| Упражнения |
| ------- | 
{% за активность на лабораторных работах  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
