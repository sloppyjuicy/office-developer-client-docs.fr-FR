---
title: Modèle de réception de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cecdb2c30d6c9df2aafbeed43714269b863ebc48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19784880"
---
# <a name="message-reception-model"></a><span data-ttu-id="54ad7-103">Modèle de réception de message</span><span class="sxs-lookup"><span data-stu-id="54ad7-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="54ad7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54ad7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54ad7-105">Le fournisseur de transport détermine si le spouleur MAPI doit interrogent pour le courrier entrant ou s’il effectue un appel sur le spouleur MAPI lors de l’arrivée de nouveau courrier.</span><span class="sxs-lookup"><span data-stu-id="54ad7-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="54ad7-106">Le fournisseur de transport définit l’indicateur SP_LOGON_POLL lorsqu’il retourne [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) pour demander d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="54ad7-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="54ad7-107">Sinon, le fournisseur de transport utilise [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) lorsque le courrier entrant n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="54ad7-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="54ad7-108">Après la formation que le courrier entrant est disponible, le spouleur MAPI ouvre un nouveau message et demande le fournisseur de transport pour stocker les propriétés de message reçu dans le message.</span><span class="sxs-lookup"><span data-stu-id="54ad7-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="54ad7-109">Ce processus fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="54ad7-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="54ad7-110">Messages disponibles sont indiqués par le fournisseur de transport appelant **IMAPISupport::SpoolerNotify** ou par le spouleur MAPI [IXPLogon::Poll](ixplogon-poll.md)l’appel.</span><span class="sxs-lookup"><span data-stu-id="54ad7-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="54ad7-111">Le spouleur MAPI appelle [IXPLogon::StartMessage](ixplogon-startmessage.md) pour lancer le processus.</span><span class="sxs-lookup"><span data-stu-id="54ad7-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="54ad7-112">Le fournisseur de transport place une valeur de référence à l’emplacement référencé dans **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="54ad7-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="54ad7-113">Ces valeurs de référence autoriser le fournisseur de transport et le spouleur MAPI pour effectuer le suivi des messages est en cours de traitement quand il y a plusieurs messages à remettre.</span><span class="sxs-lookup"><span data-stu-id="54ad7-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="54ad7-114">Le fournisseur de transport stocke les données du message dans le passé [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span><span class="sxs-lookup"><span data-stu-id="54ad7-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="54ad7-115">Le fournisseur de transport appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur l’instance de **IMessage** et renvoie à partir de **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="54ad7-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="54ad7-116">Le spouleur MAPI appelle [IXPLogon::TransportNotify](ixplogon-transportnotify.md) si elle doit s’arrêter la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="54ad7-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="54ad7-117">Si un fournisseur de transport doit fournir un grand nombre de messages et le fournisseur de transport à l’aide **IMAPISupport::SpoolerNotify** au lieu de **IXPLogon::Poll**, il convient ne pas à appeler des **SpoolerNotify** trop souvent ne pas le faire dans l’ordre priver les autres fournisseurs de transport de temps processeur.</span><span class="sxs-lookup"><span data-stu-id="54ad7-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="54ad7-118">Le spouleur MAPI n’a pas logique pour éviter ce problème, mais en général l’intervalle entre les appels **SpoolerNotify** doit être plus longue que la durée de votre fournisseur de transport pour traiter un message.</span><span class="sxs-lookup"><span data-stu-id="54ad7-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="54ad7-119">> En outre, le spouleur MAPI peut traiter pas immédiatement un message entrant.</span><span class="sxs-lookup"><span data-stu-id="54ad7-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="54ad7-120">Le spouleur MAPI peut demander le fournisseur de transport pour effectuer d’autres tâches avant de recevoir le message entrant.</span><span class="sxs-lookup"><span data-stu-id="54ad7-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

