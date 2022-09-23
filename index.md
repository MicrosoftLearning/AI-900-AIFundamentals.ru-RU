---
title: Инструкции, размещенные в Интернете
permalink: index.html
layout: home
ms.openlocfilehash: 86fa2da9bfa9e4d7edb0c853f77e95fe69e97411
ms.sourcegitcommit: 3fc8440b350b498c2f50ab4ce531a0f906792584
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2022
ms.locfileid: "147866010"
---
# <a name="azure-ai-fundamentals-exercises"></a>Упражнения по основам ИИ Azure

Эти практические упражнения предназначены для поддержки обучающих материалов в [Microsoft Learn](https://docs.microsoft.com/training/).

Для выполнения этих упражнений вам понадобится подписка Microsoft Azure. Зарегистрироваться для получения бесплатной пробной версии можно по адресу [https://azure.microsoft.com](https://azure.microsoft.com).

{% assign labs = site.pages | where_exp:"page", "page.url contains '/instructions'" %}
| Упражнения |
| ------- | 
{% за активность на лабораторных работах  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
