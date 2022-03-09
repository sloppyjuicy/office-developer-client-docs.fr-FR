---
title: Hiérarchie de contenu d’objet MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
ms.openlocfilehash: df69fbad272a692b7b4108f3533637a732139b70
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377070"
---
# <a name="mapi-object-containment-hierarchy"></a>Hiérarchie de contenu d’objet MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La relation de contenu entre les objets spécifie les dépendances dont certains objets ont sur d’autres objets pour l’accès. Pour une application cliente, l’accès à des objets particuliers permet d’accéder à d’autres utilisateurs. Dans certains cas, la relation de contenu entre les objets implémentés par un fournisseur de services suit une hiérarchie logique. Dans d’autres cas, il s’agit d’une règle arbitraire. 
  
Un client doit obtenir l’accès à un objet de session MAPI avant de pouvoir utiliser de nombreux autres objets (par exemple, les fournisseurs de services et le carnet d’adresses MAPI).
  
Le contenu de la magasin de messages est basé sur la relation hiérarchique entre les objets de la magasin de messages : l’objet de la boutique de messages lui-même, les dossiers, les messages et les pièces jointes. Logiquement, les pièces jointes sont contenues dans les messages, les messages dans les dossiers et les dossiers de la magasin de messages. La relation de contenu correspond à cette hiérarchie logique. Pour accéder à un message, par exemple, un client doit d’abord accéder au dossier dans lequel le message est contenu. Les profils et les objets d’état sont des exemples de relation de contenu plus arbitraire. Ces deux objets sont disponibles via la session. 
  
Avec certains objets, les conteneurs fournissent le seul accès. Les pièces jointes et les destinataires sont des exemples d’objets qui dépendent totalement de leurs conteneurs. Le seul accès à une pièce jointe ou à un destinataire est via le message auquel il appartient. D’autres objets ont des chemins d’accès de remplacement. Ces objets sont affectés à des identificateurs binaires, appelés identificateurs d’entrée, par les fournisseurs de services qui les créent. Les identificateurs d’entrée peuvent être utilisés pour accéder directement à leurs objets, ce qui permet aux clients de contourner l’arborescence de contenu. 
  
L’illustration suivante illustre la hiérarchie de contenu MAPI. La session se trouve en haut de l’arborescence, car c’est par le biais de la session qu’un client accède à tous les autres objets. Le niveau suivant inclut la table de la boutique de messages, un objet table qui répertorie les propriétés de tous les fournisseurs de magasins de messages dans la session en cours et le carnet d’adresses pour fournir l’accès à tous les fournisseurs de carnet d’adresses. La table de la boutique de messages et le carnet d’adresses sont utilisés pour accéder aux objets implémentés par des fournisseurs de services particuliers, indiqués ensuite, par ordre de contenu.
  
**Hiérarchie d’imbrication MAPI**
  
![Hiérarchie d’imbrication MAPI](media/amapi_41.gif "Hiérarchie d’imbrication MAPI")
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’interface et de l’objet MAPI](mapi-object-and-interface-overview.md)

