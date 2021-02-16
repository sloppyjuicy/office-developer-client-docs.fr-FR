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
- vba, project object model,Project, programmability,Programmability, Project VBA,Visual Basic pour Applications, Project object model,VBA, object model,VBA,Visual Basic pour Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Les applications clientes de bureau Project 2013 (Project Standard 2013 et Project Professionnel 2013) peuvent être personnalisées et étendues à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et créer des add-ins complexes. Les add-ins Office permettent un nouveau modèle d’extensibilité pour les volets Office dans Project qui sont créés sur une plateforme Office 2013 commune. Project Standard 2013 et Project Professionnel 2013 peuvent exécuter des add-ins Office généraux et utiliser des applications du volet Office développées spécifiquement pour que Project s’intègre à SharePoint, à d’autres sites web et applications web, ainsi qu’à des données externes.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301511"
---
# <a name="project-client-programming"></a>Programmation du client Project

Les applications clientes de bureau Project 2013 (Project Standard 2013 et Project Professionnel 2013) peuvent être personnalisées et étendues à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et créer des add-ins complexes. Les add-ins Office permettent un nouveau modèle d’extensibilité pour les volets Office dans Project qui sont créés sur une plateforme Office 2013 commune. Project Standard 2013 et Project Professionnel 2013 peuvent exécuter des add-ins Office généraux et utiliser des applications du volet Office développées spécifiquement pour que Project s’intègre à SharePoint, à d’autres sites web et applications web, ainsi qu’à des données externes.
  
 **Déplacement vers Visual Studio** VBA est utile pour l’enregistrement des macros et le développement de solutions d’automatisation relativement simples. Pour développer des solutions plus complexes, sécurisées, évolutives et facilement déployées, nous vous recommandons d’utiliser Visual Studio 2012. Microsoft .NET Framework 4.0 et l’assembly d’opation principale Project 2013 offrent de nombreux avantages pour le développement et le déploiement de solutions qui automatisent et intègrent les clients de bureau Project 2013. 
  
> [!NOTE]
> Vous pouvez utiliser Visual Studio 2010 pour développer des add-ins Project. Toutefois, Visual Studio 2012 inclut des modèles et des extensions conçus pour créer des clients de add-ins Office. 
  
Le modèle objet **MSProject** pour VBA dans Project 2013 est essentiellement identique au modèle objet **Microsoft.Office.Interop.MSProject** pour les solutions avec code géré avec outils de développement Office pour Visual Studio 2013 (également appelé VSTO). Visual Studio 2012 inclut des modèles pour le développement de modules de niveau application pour Project 2010 et Project 2013 (versions De Project Standard ou Project Professionnel). VSTO et outils de développement Office pour Visual Studio 2012 simplifient le développement, le test et le déploiement de solutions d’intégration avancées qui peuvent utiliser le client de bureau Project et d’autres applications Office 2013, et s’intégrer à des sites, des listes et des flux de travail SharePoint. 
  
Les add-ins du volet Office et d’autres pour Office et SharePoint peuvent être vendus dans l’Office Store (voir) pour une utilisation avec Project Online et les installations sur [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) site. Les macros VBA et les macros VSTO ne peuvent pas être distribuées dans l’Office Store ; Ils sont conçus pour une utilisation locale avec Project Standard et Project Professionnel. Vous pouvez distribuer des macros VBA dans un projet. Fichier MPP, installez-les dans le fichier Global.MPT sur votre ordinateur ou distribuez-les dans le modèle global d’entreprise dans Project Server 2013. Les add-ins VSTO peuvent être distribués plus en toute sécurité via [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) déploiement, ce qui permet des mises à jour faciles. 
  
## <a name="reference"></a>Référence

[Référence du développeur VBA Project](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contient des articles d’introduction et d’aide VBA. 
  
## <a name="related-sections"></a>Sections connexes

[Architecture Project Server 2013](project-server-2013-architecture.md) Montre comment les clients Project interagissent avec Project Server. 
  
## <a name="see-also"></a>Voir aussi

- [Project pour les développeurs](https://msdn.microsoft.com/office/aa905469)
- [Centre de développement Office](https://dev.office.com)
- [Visual Studio développeur](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce sécurité et déploiement](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Référence sur les champs disponibles](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

