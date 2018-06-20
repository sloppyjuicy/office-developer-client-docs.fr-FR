---
title: Recevoir des Messages à l’aide de fournisseurs de banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 94ea0fe7fba4e49c1f646d889f3727cf5ef4739d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786969"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="8dd2c-103">Recevoir des Messages à l’aide de fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="8dd2c-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="8dd2c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8dd2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8dd2c-105">Fournisseurs de banque de messages n’ont pas prendre en charge les envois de messages entrants (autrement dit, prennent en charge la possibilité pour les fournisseurs de transport et le spouleur MAPI à utiliser le message d’un fournisseur de magasins comme point de remise des messages).</span><span class="sxs-lookup"><span data-stu-id="8dd2c-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="8dd2c-106">Toutefois, si votre fournisseur de banque de messages n’accepte pas les envois de messages entrants, il ne peut être utilisé en tant que la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="8dd2c-107">Pour prendre en charge les envois de messages entrants, votre fournisseur de magasin de message procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8dd2c-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="8dd2c-108">Prend en charge les méthodes [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) et [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) afin que les applications clientes peuvent trouver les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="8dd2c-109">Prend en charge la méthode [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) afin que le spouleur MAPI peut indiquer le fournisseur de banque de messages un nouveau message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="8dd2c-110">Implémenter des notifications de sorte que les clients peuvent s’inscrire pour la notification de nouveau message.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="8dd2c-111">Les notifications sont facultatifs, mais votre fournisseur doit les implémenter.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="8dd2c-112">La séquence d’appels de méthode qui se produit lorsqu’un message entrant est remis à une banque de messages est la suivante :</span><span class="sxs-lookup"><span data-stu-id="8dd2c-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="8dd2c-113">Le spouleur MAPI appelle [IMsgStore::OpenEntry](imsgstore-openentry.md) avec boîte de réception [EntryID](entryid.md) pour obtenir une interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd2c-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="8dd2c-114">Le spouleur MAPI appelle [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour obtenir un nouvel objet de message.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="8dd2c-115">Le spouleur MAPI passe l’objet de message pour le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="8dd2c-116">Le fournisseur de transport remplit les propriétés de message avec des données à partir du système de messagerie sous-jacent et appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de l’objet message.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="8dd2c-117">Le fournisseur de banque de message utilise la méthode de notification pour informer les clients inscrits qu’un nouveau message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="8dd2c-118">Le spouleur MAPI appelle la méthode de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8dd2c-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8dd2c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dd2c-119">See also</span></span>



[<span data-ttu-id="8dd2c-120">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="8dd2c-120">Message Store Features</span></span>](message-store-features.md)

