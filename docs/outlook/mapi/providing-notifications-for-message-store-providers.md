---
title: Fourniture de notifications pour les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3722893ae57a108b338725e46c975e92c0f8ff72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587508"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="cf622-103">Fourniture de notifications pour les fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="cf622-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="cf622-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf622-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf622-105">Alors que les notifications sont facultatives, ils sont un composant essentiel d’un fournisseur de magasin de message bonne.</span><span class="sxs-lookup"><span data-stu-id="cf622-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="cf622-106">Les applications clientes et le spouleur MAPI s’appuient sur les notifications à partir du fournisseur de banque de messages pour obtenir de bonnes performances lors de l’envoi de messages sortants ou la réception de messages entrants.</span><span class="sxs-lookup"><span data-stu-id="cf622-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="cf622-107">Clients et le spouleur MAPI peuvent fonctionner sans recevoir des notifications à partir du fournisseur de banque de messages, mais ils ne seront pas en mesure d’informer les utilisateurs des modifications dans la banque de messages sans les.</span><span class="sxs-lookup"><span data-stu-id="cf622-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="cf622-108">En règle générale, cela signifie que les utilisateurs ne pourront pas savoir qu’un nouveau message est arrivé jusqu'à ce que le client suivant pour ouvrir la banque de messages reçoivent dossier.</span><span class="sxs-lookup"><span data-stu-id="cf622-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="cf622-109">Clients s’inscrire pour les notifications en appelant la méthode [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="cf622-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="cf622-110">Le client transmet une [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) de l’interface, un masque de bits qui indique le type de notifications le client est intéressé par la réception, et un **ID d’entrée** qui indique quel objet dans le message stocker les **notifications** demande s’applique à.</span><span class="sxs-lookup"><span data-stu-id="cf622-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="cf622-111">Lorsque des événements pertinents se produisent dans l’objet (par exemple, lorsqu’un nouveau message arrive dans le dossier de réception dans la banque de messages), le fournisseur de banque de message ou de l’objet lui-même doit appeler la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour tous les ** IMAPIAdviseSink** les objets qui se sont inscrits pour ce type d’événement.</span><span class="sxs-lookup"><span data-stu-id="cf622-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="cf622-112">Même si la base de vos messages fournisseur avertit jamais autres composants MAPI des modifications dans la banque de messages, qu'il doit toujours implémenter **IMsgStore::Advise** pour retourner MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="cf622-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="cf622-113">Cela informe les autres composants ne pas pour attendre le fournisseur de magasins de notifications à partir du message.</span><span class="sxs-lookup"><span data-stu-id="cf622-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf622-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf622-114">See also</span></span>



[<span data-ttu-id="cf622-115">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="cf622-115">Message Store Features</span></span>](message-store-features.md)

