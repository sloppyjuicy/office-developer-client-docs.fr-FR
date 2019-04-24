---
title: Prise en main du développement de flux de travail Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Les processus de gestion de la demande dans Project Server 2013 incluent des flux de travail qui vous aident à gérer les propositions de projet et les analyses de portefeuilles. Cette section contient des articles qui montrent comment créer des flux de travail pour Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344470"
---
# <a name="getting-started-developing-project-server-workflows"></a>Prise en main du développement de flux de travail Project Server

Les processus de gestion de la demande dans Project Server 2013 incluent des flux de travail qui vous aident à gérer les propositions de projet et les analyses de portefeuilles. Cette section contient des articles qui montrent comment créer des flux de travail pour Project Server.
  
Les flux de travail Project Server 2013 utilisent la plateforme de flux de travail SharePoint Server 2013, qui est basée sur la version 4 de Windows Workflow Foundation (WF4). Les flux de travail WF4 sont déclaratifs, ce qui signifie que l'outil de conception de flux de travail enregistre les étapes du flux de travail, les actions, les conditions et d'autres éléments dans le code XAML, qui est interprété au moment de l'exécution. Vous pouvez utiliser SharePoint Designer 2013 ou Visual Studio 2012 pour créer des flux de travail déclaratifs. Un flux de travail nécessite le moteur d'exécution du client Workflow Manager 1,0, qui peut se trouver sur un serveur local pour les solutions locales ou sur un serveur distant pour les solutions Project online.
  
Vous pouvez utiliser SharePoint Designer 2013 pour créer des flux de travail déclaratifs relativement simples. Pour les flux de travail complexes et les modèles de flux de travail qui peuvent être réutilisés, vous pouvez utiliser Visual Studio 2012 pour développer et déboguer des flux de travail pour Project Web App. Pour plus d'informations, consultez la rubrique [création de flux de travail de projet à l'aide de Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Utilisez une installation de test de Project Server, pas une installation de production, pour développer et tester des flux de travail. Les flux de travail qui sont développés pour les versions précommerciales de Project Server 2013 doivent être testés pour la version commerciale et devront peut-être être de nouveau créés et redéployés. 
  
## <a name="in-this-section"></a>Contenu de cette section

[Créer un flux de travail Project Server pour la gestion de la demande](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Voir aussi



[Mettre à jour en bloc des champs personnalisés et créer des sites de projet à partir d'un flux de travail Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Développement de flux de travail dans SharePoint Designer 2013 et Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Nouveautés des flux de travail pour SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Développer des flux de travail SharePoint 2013 à l'aide de Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Création de flux de travail de projet à l'aide de Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Présentation de Windows Workflow Foundation (WF) dans .NET 4 pour les développeurs](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Guide de l'Guide de la gestion de la demande (livre blanc)](https://msdn.microsoft.com/library/ff973112.aspx)

