---
title: Project Architecture et programmabilité de Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, architecture et programmabilité, programmabilité, Project Server,Project 2013, avantages pour EPM, Architecture et Project Server
ms.localizationpriority: medium
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Les articles de cette section décrivent l’architecture globale de la solution de gestion Enterprise Project (EPM), qui combine Project Professionnel 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
ms.openlocfilehash: 975eaefe65599954e13a402083f43da7dc5018c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628989"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Project Architecture et programmabilité de Server 2013

Les articles de cette section décrivent l’architecture globale de la solution de gestion Enterprise Project (EPM), qui combine Project Professionnel 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
  
Project Server 2013 est conçu avec le .NET Framework 4 et est la troisième version majeure de Project Server pour fournir une véritable architecture multitente. Pour l’accès au cloud, Project Server 2013 implémente un modèle objet côté client (CSOM) et un service OData pour les rapports qui peuvent être utilisés dans les applications web, les applications mobiles et les applications Silverlight. Pour les applications sur site, les clients peuvent utiliser le CSOM ou les services PSI (Project Server Interface). 
  
## <a name="introduction-to-project-server-architecture"></a>Présentation de l’architecture Project Server

Les rubriques de cette section décrivent l’architecture globale de la solution de gestion Enterprise Project (EPM), qui combine Project Professionnel 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
  
Pour l’accès par programme à Project Server, vous devez utiliser le CSOM ou les services PSI avec l’interface WCF (Windows Communication Foundation). L’interface de service web ASMX de l’interface PSI est Project Server 2013, mais fonctionne toujours. L’interface PSI permet un accès efficace à l’aide de jeux de données et vous pouvez créer des handlers pour les événements côté serveur. Le modèle CSOM lui-même utilise l’interface PSI pour accéder à la couche Project’objet métier serveur. Au lieu de quatre bases de données Project server, Project Server 2013 utilise une seule base de données dans la couche d’accès aux données.
  
Project Server 2013 s’intègre de SharePoint Server 2013. Le Project d’application peut être associé à d’SharePoint collections de sites dans la batterie de serveurs. Project Le serveur peut fonctionner avec des listes de tâches SharePoint dans la collection de sites et peut également obtenir un contrôle total sur l’emplacement où Project Server importe et gère les listes de tâches en tant que projets d’entreprise. Project Le serveur utilise également la version 4 de Windows Workflow Foundation (WF4) et ajoute des activités de flux de travail pour les solutions de gestion de la demande.
  
Pour plus d’informations sur les nombreuses nouvelles fonctionnalités que Project 2013 fournit aux développeurs et sur les fonctionnalités qui sont dépréciées, voir Mises à jour pour les développeurs dans [Project 2013.](updates-for-developers-in-project-2013.md)
  
## <a name="in-this-section"></a>Dans cette section

[Project Server 2013 décrit](project-server-2013-architecture.md) les principales parties de la plateforme Project 2013, y compris les clients et les serveurs. 
  
[Project Server programmabilité](project-server-programmability.md) décrit les principales fonctionnalités d’extensibilité de Project Server 2013, la personnalisation de Project Web App et la mise à niveau des applications conçues pour les versions précédentes de Project Server. 
  
[Ce que l’interface PSI](what-the-psi-does-and-does-not-do.md) fait et ne fait pas décrit les scénarios dans lequel l’interface PSI peut être utilisée et répertorie les choses que l’interface PSI ne peut pas faire. 
  
[Ce que le CSOM](what-the-csom-does-and-does-not-do.md) fait et ne fait pas décrit les scénarios dans lequel le CSOM peut être utilisé et répertorie les choses que le CSOM ne peut pas faire. 
  
### <a name="topics-not-covered"></a>Rubriques non couvertes

Les articles de la section Architecture et *programmabilité* ne documentent pas les fonctionnalités des clients de bureau Project (Project Standard 2013 et Project Professionnel 2013) ou Project Web App. 
  
Visual Basic pour Applications (VBA) est disponible dans l’éditeur Visual Basic dans Project Standard et Project Professionnel.
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md)
    
- [Prise en main du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md)
    

