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
ms.localizationpriority: medium
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Les applications clientes de bureau Project 2013 (Project Standard 2013 et Project Professionnel 2013) peuvent être personnalisées et étendues à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et créer des add-ins complexes. Office de recherche active un nouveau modèle d’extensibilité pour les volets Des tâches dans Project qui sont créés sur une plateforme Office 2013 commune. Project Standard 2013 et Project Professionnel 2013 peuvent exécuter des applications Office générales et utiliser des applications de volet de tâches développées spécifiquement pour Project afin de s’intégrer à SharePoint, à d’autres sites web et applications web, ainsi qu’à des données externes.
ms.openlocfilehash: 7e3f18bfd0a593ebfa4feec9cd3b3f483d368d30
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180193"
---
# <a name="project-client-programming"></a>Programmation du client Project

Les applications clientes de bureau Project 2013 (Project Standard 2013 et Project Professionnel 2013) peuvent être personnalisées et étendues à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et créer des add-ins complexes. Office de recherche active un nouveau modèle d’extensibilité pour les volets Des tâches dans Project qui sont créés sur une plateforme Office 2013 commune. Project Standard 2013 et Project Professionnel 2013 peuvent exécuter des applications Office générales et utiliser des applications de volet de tâches développées spécifiquement pour Project afin de s’intégrer à SharePoint, à d’autres sites web et applications web, ainsi qu’à des données externes.
  
 **Le passage à Visual Studio** VBA est utile pour enregistrer des macros et développer des solutions d’automatisation relativement simples. Pour développer des solutions plus complexes, sécurisées, évolutives et facilement déployées, nous vous recommandons d’utiliser Visual Studio 2012. Microsoft .NET Framework 4.0 et l’assembly d’interconnexion principale Project 2013 offrent de nombreux avantages pour le développement et le déploiement de solutions qui automatisent et intègrent les clients de bureau Project 2013. 
  
> [!NOTE]
> Vous pouvez utiliser Visual Studio 2010 pour développer des Project de développement. Toutefois, Visual Studio 2012 inclut des modèles et des extensions conçus pour créer Office clients de modules. 
  
Le modèle objet **MSProject** pour VBA Project 2013 est essentiellement identique à **Microsoft.Office. Modèle objet Interop.MSProject** pour les solutions avec code Office outils de développement Visual Studio 2013 (également appelés VSTO). Visual Studio 2012 inclut des modèles de développement de Project 2010 et Project 2013 (versions Project Standard ou Project Professionnel). Les outils de développement VSTO et Office pour Visual Studio 2012 simplifient le développement, le test et le déploiement de solutions d’intégration avancées qui peuvent utiliser le client de bureau Project et d’autres applications Office 2013 et s’intégrer à des sites, des listes et des flux de travail SharePoint. 
  
Les add-ins du volet De tâches et d’autres pour Office et SharePoint peuvent être vendus dans le Office Store (voir) pour une utilisation avec les installations Project Online et sur [https://office.microsoft.com/store/](https://office.microsoft.com/store/) site. Les macros VBA et les VSTO ne peuvent pas être distribués dans le Office Store ; ils sont conçus pour une utilisation locale avec Project Standard et Project Professionnel. Vous pouvez distribuer des macros VBA dans un projet. Le fichier MPP, installez-les dans le fichier Global.MPT sur votre ordinateur ou distribuez-les dans le modèle global d’entreprise dans Project Server 2013. VSTO peuvent être distribués plus en toute sécurité via un déploiement [ClickOnce,](https://msdn.microsoft.com/library/t71a733d.aspx) ce qui permet des mises à jour faciles. 
  
## <a name="reference"></a>Référence

[Project référence du développeur VBA](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) contient des articles d’introduction et d’aide VBA. 
  
## <a name="related-sections"></a>Sections connexes

[Project Server 2013](project-server-2013-architecture.md) illustre la façon dont les clients Project interagissent avec Project Server. 
  
## <a name="see-also"></a>Voir aussi

- [Project pour les développeurs](https://msdn.microsoft.com/office/aa905469)
- [Office développeur](https://dev.office.com)
- [Visual Studio développeur](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce sécurité et déploiement de l’ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Référence sur les champs disponibles](https://support.office.com/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

