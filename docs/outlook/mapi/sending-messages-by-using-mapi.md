---
title: Envoi de messages à l’aide de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438721"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="e7a9d-103">Envoi de messages à l’aide de MAPI</span><span class="sxs-lookup"><span data-stu-id="e7a9d-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="e7a9d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7a9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7a9d-105">Les applications clientes [appellent la méthode IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="e7a9d-106">**SubmitMessage** appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message avant de transférer le contrôle vers lepooler MAPI ou directement vers un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="e7a9d-107">Lepooler MAPI reçoit le message si l’une des erreurs suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="e7a9d-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="e7a9d-108">Le fournisseur de magasins de messages et le fournisseur de transport ne sont pas étroitement associés.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="e7a9d-109">Le message nécessite un prétraitment.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="e7a9d-110">La boutique de messages et le transport étroitement couplés ne peuvent pas gérer tous les destinataires auxquels le message est adressé.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="e7a9d-111">Une banque de messages étroitement couplée doit prendre en compte l’état d’un message avant de le présenter aupooler MAPI à télécharger vers un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="e7a9d-112">Il existe des situations dans lesquelles un message peut sembler nécessiter lepooler MAPI, mais lepooler MAPI ne doit vraiment pas être impliqué.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="e7a9d-113">Par exemple, prenons la situation dans laquelle un utilisateur envoie un message à partir de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="e7a9d-114">Le client utilise un magasin et un transport étroitement couplés.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="e7a9d-115">Si la magasin de messages étroitement couplé utilise l’emplacement du message comme seul critère pour décider si lepooler MAPI peut ou non gérer le message, lepooler MAPI reçoit toujours le message.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="e7a9d-116">Pour éviter ce type de problème, une magasin de messages étroitement couplé doit vérifier l’état du message en plus de l’emplacement du message.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="e7a9d-117">Plus précisément, le fournisseur de transport ne doit pas demander aupooler MAPI de télécharger les messages soumis activement.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="e7a9d-118">Le processus de transmission de message implique le fournisseur de magasins de messages, un ou plusieurs fournisseurs de transport et MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="e7a9d-119">Les rubriques de cette section fournissent des informations détaillées sur des rôles spécifiques dans le processus de transmission de message.</span><span class="sxs-lookup"><span data-stu-id="e7a9d-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e7a9d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7a9d-120">See also</span></span>



[<span data-ttu-id="e7a9d-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e7a9d-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="e7a9d-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e7a9d-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

