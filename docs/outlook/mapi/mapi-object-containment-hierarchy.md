---
title: Hiérarchie d'imbrication d'objets MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 33747835-6eeb-4e07-8f92-3cfa81eecd0f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f5faf3a3d4971b01509d0ff0cfa59451015ba205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345817"
---
# <a name="mapi-object-containment-hierarchy"></a>Hiérarchie d'imbrication d'objets MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La relation contenant-contenu entre les objets spécifie les dépendances de certains objets pour les autres objets pour Access. Pour une application cliente, l'accès à des objets particuliers autorise l'accès à d'autres utilisateurs. Dans certains cas, la relation contenant-contenu entre les objets implémentés par un fournisseur de services suit une hiérarchie logique. Dans les autres cas, il est arbitraire. 
  
Un client doit obtenir l'accès à un objet session MAPI avant de pouvoir utiliser de nombreux autres objets (par exemple, les fournisseurs de services et le carnet d'adresses MAPI).
  
L'imbrication d'un magasin de messages repose sur la relation hiérarchique entre les objets de la Banque de messages: l'objet de banque de messages lui-même, les dossiers, les messages et les pièces jointes. Logiquement, les pièces jointes sont contenues dans les messages, les messages dans les dossiers et les dossiers de la Banque de messages. La relation contenant-contenu correspond à cette hiérarchie logique. Pour accéder à un message, par exemple, un client doit d'abord accéder au dossier dans lequel le message est contenu. Les profils et les objets d'État sont des exemples d'une relation de confinement plus arbitraire. Ces deux objets sont disponibles par le biais de la session. 
  
Avec certains objets, les conteneurs fournissent le seul accès. Les pièces jointes et les destinataires sont des exemples d'objets entièrement dépendants de leurs conteneurs. Le seul accès à une pièce jointe ou à un destinataire s'effectue par le biais du message auquel elle appartient. Les autres objets ont des chemins d'accès de substitution. Ces objets sont affectés à des identificateurs binaires, appelés identificateurs d'entrée, par les fournisseurs de services qui les créent. Les identificateurs d'entrée peuvent être utilisés pour accéder directement à leurs objets, ce qui permet aux clients de contourner l'arborescence de la relation contenant-contenu. 
  
L'illustration suivante montre la hiérarchie de relation contenant-contenu MAPI. La session se trouve en haut de l'arborescence car elle s'effectue par le biais de la session qu'un client accède à tous les autres objets. Le niveau suivant inclut la table de banque de messages, un objet table qui répertorie les propriétés de tous les fournisseurs de banques de messages de la session en cours et le carnet d'adresses pour fournir l'accès à tous les fournisseurs de carnets d'adresses. La table de banque de messages et le carnet d'adresses sont utilisés pour accéder aux objets implémentés par des fournisseurs de services particuliers, présentés ci-dessous, dans l'ordre de relation.
  
**Hiérarchie d’imbrication MAPI**
  
![Hiérarchie d'imbrication MAPI] (media/amapi_41.gif "Hiérarchie d'imbrication MAPI")
  
## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble de l'objet et de l'interface MAPI](mapi-object-and-interface-overview.md)

