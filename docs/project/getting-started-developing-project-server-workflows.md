---
title: Prise en main développement flux de travail Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: La demande de processus de gestion dans Project Server 2013 incluent les flux de travail qui vous aident à gérer les propositions de projets et des analyses de portefeuille. Cette section contient des articles qui expliquent comment créer des flux de travail pour Project Server.
ms.openlocfilehash: 275f61b7992423a5e10a7ba90b8c76433290343e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787786"
---
# <a name="getting-started-developing-project-server-workflows"></a>Prise en main développement flux de travail Project Server

La demande de processus de gestion dans Project Server 2013 incluent les flux de travail qui vous aident à gérer les propositions de projets et des analyses de portefeuille. Cette section contient des articles qui expliquent comment créer des flux de travail pour Project Server.
  
Flux de travail Project Server 2013 utilise la plateforme de flux de travail SharePoint Server 2013, qui repose sur la version 4 de Windows Workflow Foundation (WF4). Flux de travail WF4 est déclaratives, ce qui signifie que l’outil de création de flux de travail enregistre les étapes de flux de travail, actions, conditions et autres éléments pour le code XAML, qui est interprété au moment de l’exécution. Vous pouvez utiliser SharePoint Designer 2013 ou Visual Studio 2012 pour créer des flux de travail déclaratifs. Un flux de travail requiert le moteur d’exécution du Workflow Manager Client 1.0, qui peut être sur un serveur local pour les solutions sur site ou sur un serveur distant pour les solutions Project Online.
  
Vous pouvez utiliser SharePoint Designer 2013 pour créer des flux de travail déclaratifs relativement simple. Pour les flux de travail complexes et les modèles de flux de travail qui peuvent être réutilisées, vous pouvez utiliser Visual Studio 2012 pour développer et déboguer des flux de travail pour Project Web App. Pour plus d’informations, voir [Création de flux de travail Project à l’aide de Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Une installation de test de Project Server, pas une installation de production, permet de développer et tester le flux de travail. Flux de travail qui est développées pour des versions précommerciales de Project Server 2013 doit être testé pour la version commerciale et peut avoir être recréées et redéployés. 
  
## <a name="in-this-section"></a>Dans cette section

[Créer un flux de travail Project Server pour la gestion de la demande](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Voir aussi



[Bloc de mise à jour des champs personnalisés et créer des sites de projet à partir d’un flux de travail Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Développement de flux de travail dans SharePoint Designer 2013 et Visio 2013](http://msdn.microsoft.com/en-us/library/jj163272%28office.15%29.aspx)
  
[Nouveautés des flux de travail pour SharePoint 2013](http://msdn.microsoft.com/en-us/library/jj163177.aspx)
  
[Développer des flux de travail SharePoint 2013 à l'aide de Visual Studio](http://msdn.microsoft.com/en-us/library/jj163199.aspx)
  
[Création de flux de travail de projet à l’aide de Visual Studio 2012](http://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](http://msdn.microsoft.com/en-us/library/dd489441.aspx)
  
[Introduction du développeur pour Windows Workflow Foundation (WF) dans .NET 4](http://msdn.microsoft.com/en-us/library/ee342461.aspx)
  
[Guide de gestion de la demande (livre blanc)](http://msdn.microsoft.com/en-us/library/ff973112.aspx)

