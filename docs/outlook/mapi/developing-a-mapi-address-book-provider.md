---
title: Développement d'un fournisseur de carnets d'adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316701"
---
# <a name="developing-a-mapi-address-book-provider"></a>Développement d'un fournisseur de carnets d'adresses MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de carnet d'adresses fournit des informations de destinataire aux applications clientes, aux fournisseurs de banques de messages et de transport, ainsi qu'aux MAPI. Les informations sur les destinataires sont organisées de manière hiérarchique en compartiments de stockage connus sous le nom de conteneurs. Chaque carnet d'adresses du profil fournit un ou plusieurs conteneurs de niveau supérieur ou parent au carnet d'adresses MAPI, une vue intégrée des informations sur les destinataires de tous les fournisseurs de carnet d'adresses dans une session. Le carnet d'adresses MAPI permet aux clients et aux autres fournisseurs de services d'accéder aux données d'un fournisseur de carnets d'adresses.
  
MAPI crée le carnet d'adresses intégré en:
  
1. Récupération des conteneurs de niveau supérieur de chaque fournisseur de carnet d'adresses.
    
2. Extraction de la table de hiérarchie de chaque conteneur. 
    
3. Copie de chaque tableau de hiérarchie dans un tableau de hiérarchie intégré. Il s'agit de la table de hiérarchie intégrée qui est exposée au client. 
    
MAPI impose quelques exigences sur les auteurs de fournisseurs de carnets d'adresses. La gamme de fonctionnalités possibles que vous pouvez implémenter en tant qu'enregistreur de carnet d'adresses est variable et flexible. Par exemple, votre fournisseur peut être limité à fournir une vue en lecture seule d'un type particulier d'informations de destinataire ou à implémenter un ensemble complet de fonctionnalités, éventuellement permettant aux clients ou aux fournisseurs d'apporter des ajouts ou des modifications aux données du destinataire et d'imposer critères de recherche pour la définition des affichages personnalisés. 
  
Les données de votre fournisseur peuvent résider localement dans un fichier ou une base de données ou sur un serveur distant. Certains fournisseurs de carnets d'adresses sont conçus pour fonctionner avec un système de messagerie particulier, étroitement couplé à un fournisseur de transport, tandis que d'autres peuvent fonctionner avec n'importe quel système de messagerie.
  
MAPI définit un type spécial de fournisseur de carnet d'adresses appelé carnet d'adresses personnel, ou PAB, qui implémente un seul conteneur modifiable et peut contenir des informations de destinataire copiées à partir d'autres conteneurs, ainsi que des informations créées directement. Bien que tous les fournisseurs de carnets d'adresses puissent implémenter un PAB et que plusieurs carnets d'adresses PAB puissent être ajoutés à un profil, un seul de ces fournisseurs peut être désigné pour fonctionner comme PAB pendant une session. 
  

