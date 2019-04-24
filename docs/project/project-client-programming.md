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
- VBA, modèle objet Project, projet, programmabilité, programmabilité, VBA de projet, Visual Basic pour applications, modèle objet Project, VBA, modèle objet, VBA, Visual Basic pour applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Les applications clientes de bureau 2013 de Project (Project standard 2013 et Project Professional 2013) peuvent être personnalisées et étendues à l'aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l'interface utilisateur du ruban et créer des compléments complexes. les compléments Office activent un nouveau modèle d'extensibilité pour les volets de tâches dans Project qui sont créés sur une plateforme Office 2013 commune. Project standard 2013 et Project Professional 2013 peuvent exécuter des compléments Office généraux et utiliser des compléments de volet de tâches développés spécifiquement pour l'intégration de Project à SharePoint, d'autres sites Web et d'autres applications Web, ainsi que des données externes.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301511"
---
# <a name="project-client-programming"></a>Programmation du client Project

Les applications clientes de bureau 2013 de Project (Project standard 2013 et Project Professional 2013) peuvent être personnalisées et étendues à l'aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l'interface utilisateur du ruban et créer des compléments complexes. les compléments Office activent un nouveau modèle d'extensibilité pour les volets de tâches dans Project qui sont créés sur une plateforme Office 2013 commune. Project standard 2013 et Project Professional 2013 peuvent exécuter des compléments Office généraux et utiliser des compléments de volet de tâches développés spécifiquement pour l'intégration de Project à SharePoint, d'autres sites Web et d'autres applications Web, ainsi que des données externes.
  
 **Migration vers Visual Studio** VBA est utile pour l'enregistrement de macros et le développement de solutions d'automatisation relativement simples. Pour développer des compléments de volet de tâches, des compléments et des solutions plus complexes, sécurisées, évolutives et faciles à déployer, nous vous recommandons d'utiliser Visual Studio 2012. Microsoft .NET Framework 4,0 et l'assembly PIA Project 2013 contiennent de nombreux avantages pour le développement et le déploiement de solutions qui automatisent et intègrent les clients de bureau Project 2013. 
  
> [!NOTE]
> Vous pouvez utiliser Visual Studio 2010 pour développer des compléments Project. Toutefois, Visual Studio 2012 inclut des modèles et des extensions conçus pour créer des clients de compléments Office. 
  
Le modèle objet **MSProject** pour VBA dans Project 2013 est essentiellement le même que le modèle objet **Microsoft. Office. Interop. MSProject** pour les solutions de code managé avec les outils de développement Office pour Visual Studio 2013 (également appelé VSTO). Visual Studio 2012 inclut des modèles pour développer des compléments d'application pour Project 2010 et pour Project 2013 (versions Project standard ou Project Professional). Les outils de développement VSTO et Office pour Visual Studio 2012 simplifient le développement, le test et le déploiement de solutions d'intégration avancées qui peuvent utiliser le client de bureau Project et d'autres applications Office 2013 et s'intégrer avec les sites SharePoint, les listes et travail. 
  
Les compléments de volet de tâches et d'autres compléments pour Office et SharePoint peuvent être vendus dans l'Office Store [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)(reportez-vous à la rubrique) pour une utilisation avec Project Online et les installations locales. Les macros VBA et les compléments VSTO ne peuvent pas être distribués dans l'Office Store; ils sont conçus pour une utilisation locale avec Project standard et Project professionnel. Vous pouvez distribuer des macros VBA dans un projet. Fichier MPP, installez-le dans le fichier global. MPT de votre ordinateur ou distribuez-le dans le modèle global d'entreprise dans Project Server 2013. Les compléments VSTO peuvent être distribués de façon plus sécurisée via le déploiement [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) , ce qui permet des mises à jour faciles. 
  
## <a name="reference"></a>Référence

[Référence du développeur VBA Project](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contient des articles d'aide d'introduction et VBA. 
  
## <a name="related-sections"></a>Sections connexes

[Architecture de Project Server 2013](project-server-2013-architecture.md) Indique comment les clients Project interagissent avec Project Server. 
  
## <a name="see-also"></a>Voir aussi

- [Projet pour les développeurs](https://msdn.microsoft.com/office/aa905469)
- [Centre pour développeurs Office](https://dev.office.com)
- [Centre de développement Visual Studio](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [Sécurité et déploiement ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Référence sur les champs disponibles](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

