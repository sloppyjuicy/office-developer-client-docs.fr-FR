---
title: Architecture de Project Server 2013 et programmabilité
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
- Project 2013, les avantages liés à la programmabilité, programmabilité, Project Server, Project 2013 et architecture pour Project Server, l’Architecture et EPM
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Les articles de cette section expliquent l’architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787931"
---
# <a name="project-server-2013-architecture-and-programmability"></a>Architecture de Project Server 2013 et programmabilité

Les articles de cette section expliquent l’architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
  
Project Server 2013 est générée avec le .NET Framework 4 et est la troisième version majeure de Project Server pour fournir une architecture à plusieurs couches de la valeur true. Pour l’accès nuage, Project Server 2013 implémente un modèle objet côté client (CSOM) et un service OData pour les rapports qui peut être utilisé dans les applications web, des applications mobiles et des applications Silverlight. Pour les applications sur site, les clients peuvent utiliser les services de l’Interface de Project Server (PSI) ou le modèle CSOM. 
  
## <a name="introduction-to-project-server-architecture"></a>Présentation de l’architecture de Project Server

Les rubriques de cette section décrivent l’architecture globale de la solution Enterprise Project Management (EPM), qui combine Project Professional 2013, Project Server 2013, Project Web App et SharePoint Server 2013.
  
Pour l’accès par programme à Project Server, vous devez utiliser le modèle CSOM ou services PSI avec l’interface de Windows Communication Foundation (WCF). L’interface ASMX du service web de la PSI est déconseillé dans Project Server 2013, mais il fonctionne toujours. La PSI permet un accès efficace à l’aide de jeux de données et vous pouvez créer des gestionnaires d’événements côté serveur. Le modèle CSOM lui-même utilise l’interface PSI pour accéder à la couche des objets métiers Project Server. Au lieu de quatre bases de données Project Server, Project Server 2013 utilise une base de données dans la couche d’accès aux données.
  
Project Server 2013 intègre profondément SharePoint Server 2013. Le Service d’Application Project peut être associé avec d’autres collections de sites SharePoint dans la batterie de serveurs. Project Server permettre exploiter et créer des rapports sur SharePoint, des listes de tâches dans la collection de sites et peuvent également prendre le contrôle où Project Server importe et gère les que listes de la tâche en tant que projets d’entreprise. Project Server utilise la version 4 de Windows Workflow Foundation (WF4) également et ajoute des activités de flux de travail pour les solutions de gestion de la demande.
  
Pour une description des nouvelles fonctionnalités de Project 2013 offre aux développeurs et des fonctionnalités qui sont déconseillées, consultez [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md).
  
## <a name="in-this-section"></a>Dans cette section

[Architecture de Project Server 2013](project-server-2013-architecture.md) décrit les principaux composants de la plateforme de Project 2013, y compris les clients et les serveurs. 
  
[Programmabilité de Project Server](project-server-programmability.md) présente les fonctionnalités d’extensibilité principale de Project Server 2013, la personnalisation de Project Web App et mise à niveau des applications qui sont créées pour les versions antérieures de Project Server. 
  
[Ce que la PSI fait et ne fait pas](what-the-psi-does-and-does-not-do.md) décrit des scénarios où la PSI peut être utilisée et répertorie les opérations PSI ne peut pas faire. 
  
[Ce que le modèle et ne](what-the-csom-does-and-does-not-do.md) décrit des scénarios où le modèle peut être utilisé et répertorie les opérations CSOM ne peut pas faire. 
  
### <a name="topics-not-covered"></a>Rubriques ne pas

Les articles de la section *Architecture et programmabilité* ne document pas les fonctionnalités des clients de bureau de projet (Project Standard 2013 et Project Professional 2013) Project Web App. 
  
Visual Basic pour l’aide d’Applications (VBA) est disponible dans Visual Basic editor dans Project Standard et Project Professional.
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md)
    
- [Prise en main développement flux de travail Project Server](getting-started-developing-project-server-workflows.md)
    

