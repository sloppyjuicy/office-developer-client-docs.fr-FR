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
# <a name="handling-a-transport-provider"></a><span data-ttu-id="bfe3b-103">Gestion d’un fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="bfe3b-103">Handling a transport provider</span></span>
  
<span data-ttu-id="bfe3b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bfe3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bfe3b-105">Clients de communiquent avec des fournisseurs de transport par le biais de l’état les objets fournis par des fournisseurs de transport et le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="bfe3b-106">Clients accéder aux objets de l’état en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d’état.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="bfe3b-107">Implémentent des objets de l’état du [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) de l’interface, qui a des méthodes pour la configuration des fournisseurs, purge entrant et sortant messages des files d’attente, les mots de passe paramètre et validation de l’état.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="bfe3b-108">Pour plus d’informations sur les objets d’état, voir [Table d’état et les objets d’état](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bfe3b-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="bfe3b-109">[Envoyer ou recevoir un Message à la demande](sending-or-receiving-a-message-on-demand.md): comment faire envoyer ou recevoir un message à la demande.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="bfe3b-110">[Ordre de Transport de paramètre](setting-transport-order.md): explique comment définir l’ordre de transport.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="bfe3b-111">[Reconfiguration d’un fournisseur de Transport](reconfiguring-a-transport-provider.md): décrit la procédure pour reconfigurer un fournisseur de transport et les propriétés que vous pouvez définir.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

