---
title: Modèle de réception des messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356944"
---
# <a name="message-reception-model"></a><span data-ttu-id="e4a8a-103">Modèle de réception des messages</span><span class="sxs-lookup"><span data-stu-id="e4a8a-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="e4a8a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4a8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4a8a-105">Le fournisseur de transport contrôle si le spouleur MAPI doit l'interroger pour le courrier entrant ou s'il effectue un appel vers le spouleur MAPI lors de l'arrivée de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="e4a8a-106">Le fournisseur de transport définit l'indicateur SP_LOGON_POLL lorsqu'il revient de [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) pour demander l'interrogation.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="e4a8a-107">Dans le cas contraire, le fournisseur de transport utilise [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) lorsque le courrier entrant est disponible.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="e4a8a-108">Une fois que le courrier entrant est disponible, le spouleur MAPI ouvre un nouveau message et demande au fournisseur de transport de stocker les propriétés de message reçues dans le message.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="e4a8a-109">Ce processus fonctionne comme suit:</span><span class="sxs-lookup"><span data-stu-id="e4a8a-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="e4a8a-110">Les messages disponibles sont indiqués par le fournisseur de transport appelant **IMAPISupport:: SpoolerNotify** ou par le SPOULEur MAPI qui appelle [IXPLogon::P oll](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="e4a8a-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="e4a8a-111">Le spouleur MAPI appelle [IXPLogon:: StartMessage](ixplogon-startmessage.md) pour lancer le processus.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="e4a8a-112">Le fournisseur de transport place une valeur de référence à l'emplacement référencé dans **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="e4a8a-113">Ces valeurs de référence autorisent le fournisseur de transport et le spouleur MAPI à effectuer le suivi du message en cours de traitement lorsqu'il y a plusieurs messages à livrer.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="e4a8a-114">Le fournisseur de transport stocke les données de message dans l'instance [IMessage: IMAPIProp](imessageimapiprop.md) passée.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="e4a8a-115">Le fournisseur de transport appelle la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) sur l'instance **IMessage** et renvoie à partir de **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="e4a8a-116">Le spouleur MAPI appelle [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) s'il doit arrêter la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e4a8a-117">Si un fournisseur de transport doit livrer un grand nombre de messages et que le fournisseur de transport utilise **IMAPISupport:: SpoolerNotify** au lieu de **IXPLogon::P oll**, vous devez veiller à ne pas appeler **SpoolerNotify** trop fréquemment pour ne pas priver les autres fournisseurs de transport du temps processeur.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="e4a8a-118">Le spouleur MAPI est doté d'une logique pour éviter ce problème, mais en général l'intervalle entre les appels **SpoolerNotify** doit être plus long que le temps nécessaire à votre fournisseur de transport pour traiter un message.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="e4a8a-119">> en outre, le spouleur MAPI ne peut pas traiter immédiatement un message entrant.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="e4a8a-120">Le spouleur MAPI peut demander au fournisseur de transport d'effectuer d'autres tâches avant de recevoir le message entrant.</span><span class="sxs-lookup"><span data-stu-id="e4a8a-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

