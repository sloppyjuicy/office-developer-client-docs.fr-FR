---
title: Développement d’un fournisseur de carnet d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
ms.openlocfilehash: 2939bca5d3512dd215e2370e4eabc531c1898535
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370021"
---
# <a name="developing-a-mapi-address-book-provider"></a>Développement d’un fournisseur de carnet d’adresses MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de carnet d’adresses fournit des informations sur les destinataires aux applications clientes, aux fournisseurs de magasins de messages et de transport, et à MAPI. Les informations sur les destinataires sont organisées hiérarchiquement en compartiments de stockage appelés conteneurs. Chaque carnet d’adresses du profil contribue à un ou plusieurs conteneurs de niveau supérieur, ou parent, au carnet d’adresses MAPI, une vue intégrée des informations sur les destinataires de tous les fournisseurs de carnets d’adresses dans une session. C’est par le biais du carnet d’adresses MAPI que les clients et autres fournisseurs de services ont accès aux données d’un fournisseur de carnet d’adresses.
  
MAPI crée le carnet d’adresses intégré en :
  
1. Récupération des conteneurs de niveau supérieur de chaque fournisseur de carnet d’adresses.
    
2. Récupération de la table de hiérarchie de chaque conteneur. 
    
3. Copie de chaque table de hiérarchie dans une table de hiérarchie intégrée. Il s’agit de la table de hiérarchie intégrée qui est exposée au client. 
    
MAPI impose peu d’exigences aux rédacteurs de fournisseurs de carnet d’adresses. Les fonctionnalités possibles que vous pouvez implémenter en tant que rédacteur de carnet d’adresses sont variées et flexibles. Par exemple, votre fournisseur peut être limité à fournir une vue en lecture seule d’un type particulier d’informations sur les destinataires ou implémenter un ensemble complet de fonctionnalités, ce qui peut permettre aux clients ou fournisseurs d’apporter des ajouts ou des modifications aux données des destinataires et d’imposer des critères de recherche pour définir des affichages personnalisés. 
  
Les données de votre fournisseur peuvent résider localement dans un fichier ou une base de données ou sur un serveur distant. Certains fournisseurs de carnets d’adresses sont destinés à fonctionner avec un système de messagerie particulier, étroitement associé à un fournisseur de transport, tandis que d’autres peuvent fonctionner avec n’importe quel système de messagerie.
  
MAPI définit un type spécial de fournisseur de carnet d’adresses appelé carnet d’adresses personnel( PAB), qui implémente un conteneur modifiable unique et peut contenir des informations sur les destinataires copiées à partir d’autres conteneurs, ainsi que des informations créées directement. Bien que n’importe quel fournisseur de carnet d’adresses puisse implémenter un carnet d’adresses en mode page et que plusieurs carnets d’adresses en mode sans fil peuvent être ajoutés à un profil, un seul de ces fournisseurs peut être désigné comme carnet d’adresses en mode sans fil au cours d’une session. 
  

