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
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567950"
---
# <a name="handling-a-transport-provider"></a>Gestion d’un fournisseur de transport
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Clients de communiquent avec des fournisseurs de transport par le biais de l’état les objets fournis par des fournisseurs de transport et le spouleur MAPI. Clients accéder aux objets de l’état en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d’état. Implémentent des objets de l’état du [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) de l’interface, qui a des méthodes pour la configuration des fournisseurs, purge entrant et sortant messages des files d’attente, les mots de passe paramètre et validation de l’état. Pour plus d’informations sur les objets d’état, voir [Table d’état et les objets d’état](status-table-and-status-objects.md).


- [Envoyer ou recevoir un Message à la demande](sending-or-receiving-a-message-on-demand.md): comment faire envoyer ou recevoir un message à la demande.
    
- [Ordre de Transport de paramètre](setting-transport-order.md): explique comment définir l’ordre de transport.
    
- [Reconfiguration d’un fournisseur de Transport](reconfiguring-a-transport-provider.md): décrit la procédure pour reconfigurer un fournisseur de transport et les propriétés que vous pouvez définir.
    

