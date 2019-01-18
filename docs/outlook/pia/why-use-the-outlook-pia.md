---
title: Pourquoi utiliser Outlook PIA
TOCTitle: Why use the Outlook PIA
ms:assetid: 5cc9085e-7c97-4698-8cb9-e33e427c02e7
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb645534(v=office.15)
ms:contentKeyID: 55119773
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dc882eba5f4e6c7729b81626d7324f89b724a244
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709165"
---
# <a name="why-use-the-outlook-pia"></a>Pourquoi utiliser Outlook PIA

Depuis Outlook 98, Outlook propose un modèle objet permettant aux développeurs d'intégrer les fonctionnalités Outlook dans une application, d'étendre Outlook ou de l'automatiser. Ce modèle objet est conçu pour fonctionner avec la technologie COM (Component Object Model). Jusqu'ici, les développeurs d'applications Outlook ont développé des solutions COM à l'aide de Visual Basic pour Applications (VBA) et de Visual Basic. Toutefois, les solutions Outlook développées à l’aide de VBA présentent des restrictions de déploiement, notamment dans les environnements d’entreprise et sont difficiles à mettre à jour après leur déploiement.

Le .NET Framework fournit un ensemble complet de bibliothèques de classes et de technologies d’aide qui corrigent bon nombre des restrictions des compléments COM et VBA. Cependant, une application managée requiert un pont entre les environnements .NET et COM afin de rendre possible la programmation par rapport à un modèle objet COM. Un assembly d’interopérabilité est un wrapper COM qui agit comme un pont. Par conséquent, de plus en plus de solutions Outlook sont désormais développées en tant qu’applications managées qui dépendent d’un assembly d’interopérabilité. Pour découvrir comment les assemblys d’interopérabilité facilitent l’interopérabilité entre .NET et COM, voir [Introduction à l’interopérabilité entre COM et .NET](introduction-to-interoperability-between-com-and-net.md).

Un assembly d'interopérabilité décrit les types COM et permet au code managé d'interagir avec un modèle objet COM. Il peut exister un nombre quel qu'il soit d'assemblys d'interopérabilité pour décrire un type COM donné. En tant qu'éditeur de la bibliothèque de types, Outlook fournit un assembly PIA (Primary Interop Assembly) qui contient la description officielle du modèle objet Outlook reposant sur COM. D'une manière générale, il est préférable d'utiliser l'assembly PIA Outlook plutôt qu'un assembly d'interopérabilité provenant d'une autre source.

## <a name="using-visual-studio-and-office-developer-tools-for-visual-studio"></a>Utiliser Visual Studio et les outils de développement Office pour Visual Studio

Les développeurs peuvent créer des solutions Outlook managées en dehors de Visual Studio, mais Visual Studio facilite beaucoup l'intégration des fonctionnalités Outlook dans le code managé. La facilité et la commodité de développement facilite le passage du développement COM vers .NET pour les développeurs de compléments. Au moment de la conception, les développeurs peuvent utiliser les outils de développement Office pour Visual Studio pour créer des compléments ayant accès à la fois au modèle objet Outlook et au .NET Framework. Au moment de l'exécution, les outils de développement Office pour Visual Studio fournissent un chargeur pour ces compléments : lorsqu'un utilisateur démarre Outlook, ce chargeur démarre le CLR (Common Language Runtime), Visual Studio Tools pour Office Runtime, puis charge l'assembly du complément. L’assembly peut capturer des événements déclenchés dans Outlook.

Visual Studio 2012 installe les modèles complément pour Office 2010 par défaut. Pour utiliser les outils de développement Office pour Visual Studio dans le but de développer des compléments managés pour Outlook 2013, vous devez [télécharger](https://aka.ms/officedevtoolsforvs2012) les modèles pour Office 2013.

Pour plus d’informations sur les outils de développement Office pour Visual Studio, voir [Configurer un ordinateur pour développer des solutions Office](https://docs.microsoft.com/visualstudio/vsto/how-to-configure-a-computer-to-develop-office-solutions?view=vs-2017). Pour plus d’informations sur la programmation de compléments managés pour Outlook, voir [Débuter dans la programmation de compléments VSTO](https://docs.microsoft.com/visualstudio/vsto/getting-started-programming-vsto-add-ins?view=vs-2017).

## <a name="see-also"></a>Voir aussi

- [Installation et référencement de l'assembly PIA Outlook](installing-and-referencing-the-outlook-pia.md)

