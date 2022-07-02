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
- vba, modèle objet de projet, Projet, programmabilité, Programmabilité, Project VBA, Visual Basic pour Applications, Modèle objet Project, VBA, modèle objet, VBA, Visual Basic pour Applications
ms.localizationpriority: medium
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Les applications clientes de bureau Project 2013, Project Standard 2013 et Project Professionnel 2013, peuvent être personnalisées et étendues à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et créer des compléments complexes. Les compléments Office activent un nouveau modèle d’extensibilité pour les volets Office dans Project qui reposent sur une plateforme Office 2013 commune. Project Standard 2013 et Project Professionnel 2013 peuvent exécuter des compléments Office généraux et utiliser des compléments du volet Office développés spécifiquement pour Project afin de les intégrer à SharePoint, à d’autres sites web et applications web, ainsi qu’à des données externes.
ms.openlocfilehash: 35b85fd802354b82d8001c23cf169b0db910c10c
ms.sourcegitcommit: b9eed77e21325860cef74e4fb8b86adcc247bc09
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2022
ms.locfileid: "66608504"
---
# <a name="project-client-programming"></a>Programmation du client Project

Les applications clientes de bureau Project 2013, Project Standard 2013 et Project Professionnel 2013, peuvent être personnalisées et étendues à l’aide de VBA pour écrire des macros. Vous pouvez utiliser Visual Studio 2012 pour personnaliser l’interface utilisateur du ruban et créer des compléments complexes. Les compléments Office activent un nouveau modèle d’extensibilité pour les volets Office dans Project qui reposent sur une plateforme Office 2013 commune. Project Standard 2013 et Project Professionnel 2013 peuvent exécuter des compléments Office généraux et utiliser des compléments du volet Office développés spécifiquement pour Project afin de les intégrer à SharePoint, à d’autres sites web et applications web, ainsi qu’à des données externes.
  
 **Passage à Visual Studio** VBA est utile pour l’enregistrement des macros et le développement de solutions d’automatisation relativement simples. Pour développer des compléments du volet Office, des compléments et des solutions plus complexes, sécurisées, évolutives et faciles à déployer, nous vous recommandons d’utiliser Visual Studio 2012. Microsoft .NET Framework 4.0 et l’assembly d’interopérabilité principal Project 2013 offrent de nombreux avantages pour le développement et le déploiement de solutions qui automatisent et intègrent les clients de bureau Project 2013. 
  
> [!NOTE]
> Vous pouvez utiliser Visual Studio 2010 pour développer des compléments Project. Toutefois, Visual Studio 2012 inclut des modèles et des extensions conçus pour créer des clients de compléments Office. 
  
Le modèle objet **MSProject** pour VBA dans Project 2013 est essentiellement le même que le modèle objet **Microsoft.Office.Interop.MSProject** pour les solutions de code managé avec les outils de développement Office pour Visual Studio 2013 (également appelé VSTO). Visual Studio 2012 inclut des modèles pour le développement de compléments au niveau de l’application pour Project 2010 et Project 2013 (les versions Project Standard ou Project Professionnel). VSTO et Outils de développement Office pour Visual Studio 2012 simplifient le développement, le test et le déploiement de solutions d’intégration avancées qui peuvent utiliser le client de bureau Project et d’autres applications Office 2013, et s’intégrer aux sites, listes et workflows SharePoint. 
  
Les compléments du volet Office et d’autres compléments pour Office et SharePoint peuvent être vendus dans l’Office Store (voir [https://office.microsoft.com/store/](https://office.microsoft.com/store/)) pour une utilisation avec des installations Project Online et locales. Les macros VBA et les compléments VSTO ne peuvent pas être distribués dans l’Office Store ; ils sont conçus pour une utilisation locale avec Project Standard et Project Professionnel. Vous pouvez distribuer des macros VBA dans un projet. Fichier MPP, installez-les dans le fichier Global.MPT sur votre ordinateur ou distribuez-les dans le modèle global d’entreprise dans Project Server 2013. Les compléments VSTO peuvent être distribués de manière plus sécurisée via le déploiement [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) , ce qui permet des mises à jour faciles. 
  
## <a name="reference"></a>Référence

[Informations de référence sur les développeurs VBA project](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contient des articles d’introduction et d’aide VBA. 
  
## <a name="related-sections"></a>Sections connexes

[Architecture de Project Server 2013](project-server-2013-architecture.md) Montre comment les clients Project interagissent avec Project Server. 
  
## <a name="see-also"></a>Voir aussi

- [Project pour les développeurs](https://msdn.microsoft.com/office/aa905469)
- [Centre de développement Office](https://developer.microsoft.com/en-us/office)
- [Centre de développement Visual Studio](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [Sécurité et déploiement ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Référence sur les champs disponibles](https://support.office.com/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

