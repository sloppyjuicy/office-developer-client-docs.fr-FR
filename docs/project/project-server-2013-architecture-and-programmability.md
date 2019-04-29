---
title: Architecture et programmabilité de Project Server 2013
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
- Project 2013, architecture et programmabilité, programmabilité, Project Server, Project 2013, avantages pour EPM, architecture et Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Les Articles de cette section décrivent l'architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413786"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Architecture et programmabilité de Project Server 2013

Les Articles de cette section décrivent l'architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
  
Project Server 2013 est créé avec .NET Framework 4 et est la troisième version majeure de Project Server pour fournir une architecture à plusieurs couches. Pour l'accès Cloud, Project Server 2013 implémente un modèle objet côté client (CSOM) et un service OData pour la création de rapports qui peuvent être utilisés dans les applications Web, les applications mobiles et les applications Silverlight. Pour les applications locales, les clients peuvent utiliser les services CSOM ou interface PSI (Project Server Interface). 
  
## <a name="introduction-to-project-server-architecture"></a>Présentation de l'architecture de Project Server

Les rubriques de cette section décrivent l'architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
  
Pour un accès par programme à Project Server, vous devez utiliser les services CSOM ou PSI avec l'interface Windows Communication Foundation (WCF). L'interface de service Web ASMX de la PSI est déconseillée dans Project Server 2013, mais fonctionne toujours. La PSI permet un accès efficace à l'aide de jeux de données et vous pouvez créer des gestionnaires pour les événements côté serveur. Le CSOM utilise le PSI pour accéder à la couche d'objets métiers Project Server. Au lieu de quatre bases de données Project Server, Project Server 2013 utilise une seule base de données dans la couche d'accès aux données.
  
Project Server 2013 s'intègre de façon approfondie à SharePoint Server 2013. Le service d'application Project peut être associé à d'autres collections de sites SharePoint dans la batterie de serveurs. Project Server peut fonctionner avec les listes de tâches SharePoint et en faire des rapports dans la collection de sites, et peut également bénéficier d'un contrôle total où Project Server importe et gère les listes de tâches en tant que projets d'entreprise. Project Server utilise également la version 4 de Windows Workflow Foundation (WF4) et ajoute des activités de flux de travail pour les solutions de gestion de la demande.
  
Pour plus d'informations sur les nombreuses nouvelles fonctionnalités proposées par Project 2013 pour les développeurs, ainsi que sur les fonctionnalités déconseillées, consultez la rubrique [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Dans cette section

L' [architecture de Project Server 2013](project-server-2013-architecture.md) décrit les principales parties de la plateforme Project 2013, y compris les clients et les serveurs. 
  
La programmabilité de [Project Server](project-server-programmability.md) aborde les principales fonctionnalités d'extensibilité de project Server 2013, de la personnalisation de Project Web App et de la mise à niveau des applications qui sont conçues pour les versions antérieures de Project Server. 
  
[Ce que fait la PSI,](what-the-psi-does-and-does-not-do.md) il décrit les scénarios dans lesquels la PSI peut être utilisée et répertorie les éléments que le PSI ne peut pas faire. 
  
[Ce que fait et ne fait pas le CSOM](what-the-csom-does-and-does-not-do.md) décrit les scénarios dans lesquels le CSOM peut être utilisé et répertorie les éléments que l'CSOM ne peut pas faire. 
  
### <a name="topics-not-covered"></a>Rubriques non traitées

Les Articles de la section *architecture et programmabilité* ne documentent pas les fonctionnalités des clients de bureau Project (project standard 2013 et project professionnel 2013) ou Project Web App. 
  
L'aide de Visual Basic pour applications (VBA) est disponible dans Visual Basic Editor dans Project standard et Project professionnel.
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md)
    
- [Prise en main du développement de flux de travail Project Server](getting-started-developing-project-server-workflows.md)
    

