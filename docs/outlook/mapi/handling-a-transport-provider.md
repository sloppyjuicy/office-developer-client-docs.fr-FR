---
title: Gestion d’un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
ms.openlocfilehash: 29d787b31b509b31bc02bb66d69586f0d9322202
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379975"
---
# <a name="handling-a-transport-provider"></a>Gestion d’un fournisseur de transport
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients communiquent avec les fournisseurs de transport via les objets d’état fournis par les fournisseurs de transport et lepooler MAPI. Les clients accèdent aux objets d’état en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d’état. Les objets d’état implémentent l’interface [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) , qui dispose de méthodes pour configurer les fournisseurs, vider les files d’attente de messages entrants et sortants, définir des mots de passe et valider l’état. Pour plus d’informations sur les objets d’état, voir [Tableau d’état et Objets d’état](status-table-and-status-objects.md).


- [Envoi ou réception d’un message à la demande](sending-or-receiving-a-message-on-demand.md) : décrit comment envoyer ou recevoir un message à la demande.
    
- [Définition de l’ordre](setting-transport-order.md) de transport : décrit comment définir l’ordre de transport.
    
- [Reconfiguration d’un fournisseur de transport](reconfiguring-a-transport-provider.md) : décrit comment reconfigurer un fournisseur de transport et quelles propriétés peuvent être définies.
    

