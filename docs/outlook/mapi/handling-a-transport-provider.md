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
# <a name="handling-a-transport-provider"></a><span data-ttu-id="83b0f-103">Gestion d’un fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="83b0f-103">Handling a transport provider</span></span>
  
<span data-ttu-id="83b0f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83b0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83b0f-105">Les clients communiquent avec des fournisseurs de transport via les objets d'état fournis par les fournisseurs de transport et le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="83b0f-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="83b0f-106">Les clients accèdent aux objets d'État en appelant [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d'État.</span><span class="sxs-lookup"><span data-stu-id="83b0f-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="83b0f-107">Les objets d'État implémentent l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) , qui comporte des méthodes de configuration des fournisseurs, de vidage des files d'attente de messages entrants et sortants, de définition des mots de passe et de validation de l'État.</span><span class="sxs-lookup"><span data-stu-id="83b0f-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="83b0f-108">Pour plus d'informations sur les objets d'État, voir [table d'État et objets d'État](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="83b0f-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="83b0f-109">[Envoi ou réception d'un message à la demande](sending-or-receiving-a-message-on-demand.md): explique comment envoyer ou recevoir un message à la demande.</span><span class="sxs-lookup"><span data-stu-id="83b0f-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="83b0f-110">[Définition](setting-transport-order.md)de l'ordre de transport: décrit la définition de l'ordre de transport.</span><span class="sxs-lookup"><span data-stu-id="83b0f-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="83b0f-111">[Reconfiguration d'un fournisseur de transport](reconfiguring-a-transport-provider.md): décrit comment reconfigurer un fournisseur de transport et quelles propriétés peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="83b0f-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

