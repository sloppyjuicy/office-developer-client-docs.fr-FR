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
# <a name="handling-a-transport-provider"></a><span data-ttu-id="3512c-103">Gestion d’un fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="3512c-103">Handling a transport provider</span></span>
  
<span data-ttu-id="3512c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3512c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3512c-105">Les clients communiquent avec les fournisseurs de transport via les objets d’état fournis par les fournisseurs de transport et lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="3512c-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="3512c-106">Les clients accèdent aux objets d’état en appelant [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour récupérer la table d’état.</span><span class="sxs-lookup"><span data-stu-id="3512c-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="3512c-107">Les objets d’état implémentent l’interface [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) qui dispose de méthodes pour configurer les fournisseurs, vider les files d’attente de messages entrants et sortants, définir des mots de passe et valider l’état.</span><span class="sxs-lookup"><span data-stu-id="3512c-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="3512c-108">Pour plus d’informations sur les objets d’état, voir [Tableau d’état et Objets d’état.](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="3512c-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="3512c-109">[Envoi ou réception d’un message à la demande](sending-or-receiving-a-message-on-demand.md): décrit comment envoyer ou recevoir un message à la demande.</span><span class="sxs-lookup"><span data-stu-id="3512c-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="3512c-110">[Définition de l’ordre](setting-transport-order.md)de transport : décrit comment définir l’ordre de transport.</span><span class="sxs-lookup"><span data-stu-id="3512c-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="3512c-111">[Reconfiguration d’un fournisseur de transport](reconfiguring-a-transport-provider.md): décrit comment reconfigurer un fournisseur de transport et quelles propriétés peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="3512c-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

