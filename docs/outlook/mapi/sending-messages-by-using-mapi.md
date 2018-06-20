---
title: Envoyer des Messages à l’aide de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 36de3b70b0ab7b16f8abed85bbd0983224e00568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787112"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="a92f1-103">Envoyer des Messages à l’aide de MAPI</span><span class="sxs-lookup"><span data-stu-id="a92f1-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="a92f1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a92f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a92f1-105">Applications clientes appellent la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="a92f1-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="a92f1-106">**SubmitMessage** appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message avant de transférer le contrôle soit le spouleur MAPI ou directement à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="a92f1-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="a92f1-107">Le spouleur MAPI reçoit le message si une des actions suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="a92f1-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="a92f1-108">Le fournisseur de banque de message et le fournisseur de transport ne sont pas étroitement liées.</span><span class="sxs-lookup"><span data-stu-id="a92f1-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="a92f1-109">Le message nécessite un prétraitement.</span><span class="sxs-lookup"><span data-stu-id="a92f1-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="a92f1-110">La banque de messages étroitement couplés et de transport ne peut pas gérer tous les destinataires auxquels le message est adressé.</span><span class="sxs-lookup"><span data-stu-id="a92f1-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="a92f1-111">Une banque de messages étroitement couplés doit prendre en considération état d’un message avant qu’il présente le spouleur MAPI à transférer vers un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="a92f1-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="a92f1-112">Il existe des situations où un message s’affiche pour demander le spouleur MAPI, mais le spouleur MAPI doit vraiment pas impliqué.</span><span class="sxs-lookup"><span data-stu-id="a92f1-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="a92f1-113">Par exemple, considérez la situation où un utilisateur envoie un message à partir de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="a92f1-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="a92f1-114">Le client utilise un magasin étroitement couplé et transport.</span><span class="sxs-lookup"><span data-stu-id="a92f1-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="a92f1-115">Si la banque de messages étroitement couplés utilise l’emplacement du message comme critère unique permettant de décider s’il faut autoriser le spouleur MAPI sur les gérer le message, le spouleur MAPI toujours le message.</span><span class="sxs-lookup"><span data-stu-id="a92f1-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="a92f1-116">Pour éviter ce type de problème, une banque de messages étroitement couplés doit vérifier le statut du message en plus de l’emplacement du message.</span><span class="sxs-lookup"><span data-stu-id="a92f1-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="a92f1-117">Plus précisément, le fournisseur de transport ne doit pas demander que le spouleur MAPI télécharger tout message est envoyé en.</span><span class="sxs-lookup"><span data-stu-id="a92f1-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="a92f1-118">Le processus de transmission de message implique le fournisseur de banque de message, un ou plusieurs fournisseurs de transport et MAPI.</span><span class="sxs-lookup"><span data-stu-id="a92f1-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="a92f1-119">Les rubriques de cette section fournissent des informations détaillées sur des rôles spécifiques dans le processus de transmission de message.</span><span class="sxs-lookup"><span data-stu-id="a92f1-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a92f1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a92f1-120">See also</span></span>



[<span data-ttu-id="a92f1-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a92f1-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="a92f1-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a92f1-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

