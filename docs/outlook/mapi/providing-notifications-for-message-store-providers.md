---
title: Fourniture de notifications pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419932"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="f3fc9-103">Fourniture de notifications pour les fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="f3fc9-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="f3fc9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3fc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3fc9-105">Bien que les notifications soient facultatives, elles sont une partie très importante d’un bon fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="f3fc9-106">Les applications clientes et lepooler MAPI s’appuient sur les notifications du fournisseur de la boutique de messages pour obtenir de bonnes performances lors de l’envoi de messages sortants ou de la réception de messages entrants.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="f3fc9-107">Les clients et lepooler MAPI peuvent fonctionner sans recevoir de notifications du fournisseur de la boutique de messages, mais ils ne pourront pas informer les utilisateurs des modifications apportées à la magasin de messages sans eux.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="f3fc9-108">En règle générale, cela signifie que les utilisateurs ne peuvent pas voir qu’un nouveau message est arrivé tant que leur client n’ouvre pas le dossier de réception de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="f3fc9-109">Les clients s’inscrivent pour recevoir des notifications en appelant la méthode [IMsgStore::Advise.](imsgstore-advise.md)</span><span class="sxs-lookup"><span data-stu-id="f3fc9-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="f3fc9-110">Le client transmet une interface [IMAPIAdviseSink : IUnknown,](imapiadvisesinkiunknown.md) un masque de bits qui indique le type de notifications que le client est intéressé par la réception et un **EntryID** qui indique l’objet dans la boutique de messages auquel la demande **de** conseil s’applique.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="f3fc9-111">Lorsque des événements pertinents se produisent dans l’objet (par exemple, lorsqu’un nouveau message arrive dans le dossier de réception de la boutique de messages), le fournisseur de la boutique de messages ou l’objet lui-même doit appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour tous les objets **IMAPIAdviseSink** qui ont été inscrits pour ce type d’événement.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="f3fc9-112">Même si votre fournisseur de magasin de messages n’avertit jamais les autres composants MAPI des modifications apportées à la boutique de messages, il doit toujours implémenter **IMsgStore::Advise** pour renvoyer MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="f3fc9-113">Cela informe les autres composants de ne pas s’attendre à recevoir de notifications du fournisseur de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3fc9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3fc9-114">See also</span></span>



[<span data-ttu-id="f3fc9-115">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="f3fc9-115">Message Store Features</span></span>](message-store-features.md)

