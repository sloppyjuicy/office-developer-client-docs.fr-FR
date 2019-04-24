---
title: Écriture d'un client automatisé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325591"
---
# <a name="writing-an-automated-client"></a>Écriture d'un client automatisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une application cliente automatisée est une application qui s'exécute sans assistance, sans afficher d'interface utilisateur.
  
 Par défaut, de nombreuses méthodes d'interface MAPI affichent une interface utilisateur. Toutes ces méthodes comportent des indicateurs qui permettent à un client d'autoriser ou de supprimer cet affichage. Bien que MAPI s'attend à ce que les fournisseurs de services respectent ces indicateurs, certains fournisseurs ne satisfont pas toujours à ces attentes. Un motif légitime de non-respect des indicateurs est la dépendance du fournisseur de services sur un autre service qui n'autorise pas la suppression de l'interface utilisateur. Si vous développez un client automatisé, soyez attentif aux fournisseurs de services que vous utilisez et à la façon dont ils sont configurés. Ne partez pas du principe que tous les appels permettant de supprimer une interface utilisateur aboutiront. 
  
Les clients automatisés doivent disposer des informations nécessaires pour une configuration correcte de chacun des services de messagerie dans le profil. Il existe deux façons de fournir des informations de configuration à l'ouverture de session:
  
- Le fournisseur de services peut récupérer des informations à partir du profil.
    
- Le fournisseur de services peut inviter l'utilisateur à fournir des informations. 
    
Étant donné que la deuxième option n'est pas disponible pour les clients automatisés, ces clients doivent utiliser la première option. Les clients doivent configurer leurs profils avec soin pour s'assurer que cette option fonctionne toujours.
  
Les clients automatisés définissent toujours l'indicateur MAPI_NO_MAIL dans l'appel de la fonction [MAPILogonEx](mapilogonex.md) pour commencer une session MAPI. 
  

