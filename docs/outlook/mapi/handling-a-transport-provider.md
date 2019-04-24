---
title: Gestion d’un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299495"
---
# <a name="handling-a-transport-provider"></a>Gestion d’un fournisseur de transport
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients communiquent avec des fournisseurs de transport via les objets d'état fournis par les fournisseurs de transport et le spouleur MAPI. Les clients accèdent aux objets d'État en appelant [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d'État. Les objets d'État implémentent l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) , qui comporte des méthodes de configuration des fournisseurs, de vidage des files d'attente de messages entrants et sortants, de définition des mots de passe et de validation de l'État. Pour plus d'informations sur les objets d'État, voir [table d'État et objets d'État](status-table-and-status-objects.md).


- [Envoi ou réception d'un message à la demande](sending-or-receiving-a-message-on-demand.md): explique comment envoyer ou recevoir un message à la demande.
    
- [Définition](setting-transport-order.md)de l'ordre de transport: décrit la définition de l'ordre de transport.
    
- [Reconfiguration d'un fournisseur de transport](reconfiguring-a-transport-provider.md): décrit comment reconfigurer un fournisseur de transport et quelles propriétés peuvent être définies.
    

