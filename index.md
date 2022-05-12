---
title: Инструкции, размещенные в Интернете
permalink: index.html
layout: home
ms.openlocfilehash: b85af520a10e63a2f9a5696db03bfd946aff968f
ms.sourcegitcommit: 1ef64e3008a439d0d0bb3d93a27d3df68d3d64a9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/17/2022
ms.locfileid: "140688696"
---
# <a name="azure-ai-fundamentals-exercises"></a>Упражнения по основам ИИ Azure

Используйте приведенные ниже ссылки для выполнения практических занятий по курсу [AI-900 *Microsoft Azure AI Fundamentals*](https://docs.microsoft.com/learn/certifications/courses/ai-900t00).

Для выполнения этих упражнений вам понадобится подписка Microsoft Azure. Если ваш инструктор не предоставил вам такую подписку, можете зарегистрироваться для получения бесплатной пробной версии на сайте [https://azure.microsoft.com](https://azure.microsoft.com).

{% assign labs = site.pages | where_exp:"page", "page.url contains '/instructions'" %}
| Упражнения |
| ------- | 
{% за активность на лабораторных работах  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
