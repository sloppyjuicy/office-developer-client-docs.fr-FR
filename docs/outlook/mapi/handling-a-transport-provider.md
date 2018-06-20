---
title: Gestion d’un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 140fe97662f7a2ce68c18d8e0eb991d0819da6dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783409"
---
# <a name="handling-a-transport-provider"></a>Gestion d’un fournisseur de transport
  
**S’applique à**: Outlook 
  
Clients de communiquent avec des fournisseurs de transport par le biais de l’état les objets fournis par des fournisseurs de transport et le spouleur MAPI. Clients accéder aux objets de l’état en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d’état. Implémentent des objets de l’état du [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) de l’interface, qui a des méthodes pour la configuration des fournisseurs, purge entrant et sortant messages des files d’attente, les mots de passe paramètre et validation de l’état. Pour plus d’informations sur les objets d’état, voir [Table d’état et les objets d’état](status-table-and-status-objects.md).


- [Envoyer ou recevoir un Message à la demande](sending-or-receiving-a-message-on-demand.md): comment faire envoyer ou recevoir un message à la demande.
    
- [Ordre de Transport de paramètre](setting-transport-order.md): explique comment définir l’ordre de transport.
    
- [Reconfiguration d’un fournisseur de Transport](reconfiguring-a-transport-provider.md): décrit la procédure pour reconfigurer un fournisseur de transport et les propriétés que vous pouvez définir.
    

