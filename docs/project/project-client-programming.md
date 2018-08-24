---
title: Programmation du client Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- VBA, project la programmabilité de Project, modèle objet, la programmabilité de projet VBA, Visual Basic pour Applications, VBA, modèle objet modèle d’objet projet, VBA, Visual Basic pour Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Les applications de client de bureau Project 2013, Project Standard 2013 et Project Professional 2013 — peuvent être personnalisés et étendus à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et de créer des compléments complexes permet de compléments Office de modèle une nouvelle extensibilité pour les volets de tâches de projet qui sont basés sur une plate-forme commune de Office 2013. Project Standard 2013 et Project Professional 2013 peuvent exécuter des compléments Office générales et utiliser tâche volet compléments qui sont développés spécifiquement pour le projet d’intégrer SharePoint, autres sites Web et les applications web et les données externes.
ms.openlocfilehash: 9e89c5a1f6486ce49ad8b95bcd7a92497b7a2436
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594739"
---
# <a name="project-client-programming"></a>Programmation du client Project

Les applications de client de bureau Project 2013, Project Standard 2013 et Project Professional 2013 — peuvent être personnalisés et étendus à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et de créer des compléments complexes permet de compléments Office de modèle une nouvelle extensibilité pour les volets de tâches de projet qui sont basés sur une plate-forme commune de Office 2013. Project Standard 2013 et Project Professional 2013 peuvent exécuter des compléments Office générales et utiliser tâche volet compléments qui sont développés spécifiquement pour le projet d’intégrer SharePoint, autres sites Web et les applications web et les données externes.
  
 **Passage à Visual Studio** VBA est utile pour l’enregistrement de macros et du développement de solutions d’automatisation relativement simple. Pour développer des compléments de volet de tâches, des compléments et plus complexe, sécurisée, évolutive et facile à déployer des solutions, nous recommandons d’utiliser Visual Studio 2012. Microsoft .NET Framework 4.0 et l’assembly PIA Project 2013 offrent de nombreux avantages pour développer et déployer des solutions qui automatisent et intègrent les clients de bureau de Project 2013. 
  
> [!NOTE]
> Vous pouvez utiliser Visual Studio 2010 pour développer des compléments Project. Toutefois, Visual Studio 2012 inclut les modèles et les extensions qui sont conçues pour créer des clients Office Add-ins. 
  
Le modèle objet **MSProject** pour VBA dans Project 2013 est essentiellement le même que le modèle d’objet **Microsoft.Office.Interop.MSProject** pour les solutions de code managé avec les outils de développement Office pour Visual Studio 2013 (également appelé VSTO). Visual Studio 2012 inclut des modèles pour le développement d’application au niveau des compléments pour Project 2010 et Project 2013 (versions de Project Standard ou Project Professionnel). VSTO et outils de développement Office pour Visual Studio 2012 simplifient le développement, le test et déploiement de solutions d’intégration avancée qui peuvent utiliser le client de bureau Project et d’autres applications Office 2013 et les intégrer à des sites SharePoint, listes, et flux de travail. 
  
Compléments de volet de tâches et d’autres compléments pour Office et SharePoint peuvent être vendus dans l’Office Store (voir [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) pour une utilisation avec des installations de Project Online et sur site. Compléments VSTO et les macros VBA ne peut pas être répercutées dans le magasin Office ; ils sont conçus pour une utilisation locale avec Project Standard et Project Professional. Vous pouvez distribuer des macros VBA dans un projet. Fichier MPP, les installer dans le fichier Global.MPT sur votre ordinateur, ou les distribuer dans le modèle global d’entreprise dans Project Server 2013. Compléments VSTO peuvent être distribués de façon plus sécurisée via le déploiement [ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx) , qui permet de faciles mises à jour. 
  
## <a name="reference"></a>Référence

[Référence du développeur VBA Project](http://msdn.microsoft.com/en-us/library/ee861523%28office.15%29.aspx) Contient la présentation et articles d’aide VBA. 
  
## <a name="related-sections"></a>Sections associées

[Architecture de Project Server 2013](project-server-2013-architecture.md) Montre comment les clients Project interagissent avec Project Server. 
  
## <a name="see-also"></a>Voir aussi

- [Projet pour les développeurs](http://msdn.microsoft.com/en-us/office/aa905469)
- [Centre pour développeurs Office](https://dev.office.com)
- [Centre de développement Visual Studio](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx)
- [Sécurité et déploiement ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx)
- [Référence sur les champs disponibles](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

