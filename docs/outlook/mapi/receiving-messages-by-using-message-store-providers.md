---
title: Réception de messages à l'aide de fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418728"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="625e2-103">Réception de messages à l'aide de fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="625e2-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="625e2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="625e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="625e2-105">Les fournisseurs de banques de messages ne doivent pas prendre en charge les envois de messages entrants (autrement dit, prendre en charge la possibilité pour les fournisseurs de transport et le spouleur MAPI d'utiliser le fournisseur de banques de messages comme point de remise pour les messages).</span><span class="sxs-lookup"><span data-stu-id="625e2-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="625e2-106">Toutefois, si votre fournisseur de banque de messages ne prend pas en charge les envois de messages entrants, il ne peut pas être utilisé comme banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="625e2-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="625e2-107">Pour prendre en charge les envois de messages entrants, votre fournisseur de banque de messages doit effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="625e2-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="625e2-108">Prendre en charge les méthodes [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) et [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) afin que les applications clientes puissent trouver les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="625e2-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="625e2-109">Prendre en charge la méthode [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) afin que le spouleur MAPI puisse informer le fournisseur de banque de messages qu'un nouveau message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="625e2-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="625e2-110">Implémenter des notifications afin que les clients puissent s'inscrire pour recevoir des notifications de nouveau message.</span><span class="sxs-lookup"><span data-stu-id="625e2-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="625e2-111">Les notifications sont facultatives, mais votre fournisseur doit les implémenter.</span><span class="sxs-lookup"><span data-stu-id="625e2-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="625e2-112">La séquence des appels de méthode qui se produit lorsqu'un message entrant est remis à une banque de messages est la suivante:</span><span class="sxs-lookup"><span data-stu-id="625e2-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="625e2-113">Le spouleur MAPI appelle [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec l' [EntryID](entryid.md) de la boîte de réception pour obtenir une interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="625e2-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="625e2-114">Le spouleur MAPI appelle [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) pour obtenir un nouvel objet message.</span><span class="sxs-lookup"><span data-stu-id="625e2-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="625e2-115">Le spouleur MAPI transmet l'objet message au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="625e2-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="625e2-116">Le fournisseur de transport remplit les propriétés du message avec des données du système de messagerie sous-jacent et appelle la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de l'objet message.</span><span class="sxs-lookup"><span data-stu-id="625e2-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="625e2-117">Le fournisseur de banque de messages utilise sa méthode de notification pour informer les clients inscrits qu'un nouveau message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="625e2-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="625e2-118">Le spouleur MAPI appelle la méthode [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="625e2-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="625e2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="625e2-119">See also</span></span>



[<span data-ttu-id="625e2-120">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="625e2-120">Message Store Features</span></span>](message-store-features.md)

