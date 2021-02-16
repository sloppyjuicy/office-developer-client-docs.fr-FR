---
title: Gestion d’un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416537"
---
# <a name="handling-a-transport-provider"></a>Gestion d’un fournisseur de transport
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients communiquent avec les fournisseurs de transport via les objets d’état fournis par les fournisseurs de transport et lepooler MAPI. Les clients accèdent aux objets d’état en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d’état. Les objets d’état implémentent l’interface [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) qui dispose de méthodes pour configurer les fournisseurs, vider les files d’attente de messages entrants et sortants, définir des mots de passe et valider l’état. Pour plus d’informations sur les objets d’état, voir [Tableau d’état et Objets d’état.](status-table-and-status-objects.md)


- [Envoi ou réception d’un message à la demande](sending-or-receiving-a-message-on-demand.md): décrit comment envoyer ou recevoir un message à la demande.
    
- [Définition de l’ordre](setting-transport-order.md)de transport : décrit comment définir l’ordre de transport.
    
- [Reconfiguration d’un fournisseur de transport](reconfiguring-a-transport-provider.md): décrit comment reconfigurer un fournisseur de transport et quelles propriétés peuvent être définies.
    

