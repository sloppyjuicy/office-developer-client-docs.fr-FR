---
title: Sous-arborescence IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6fe642d10a50d25874aee170441a07c184b46575
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591092"
---
# <a name="ipm-subtree"></a><span data-ttu-id="69bbb-103">Sous-arborescence IPM</span><span class="sxs-lookup"><span data-stu-id="69bbb-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="69bbb-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69bbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69bbb-105">MAPI crée une arborescence de dossiers sous le dossier racine d’une banque de messages pour envoyant des messages et de recevoir des messages à partir de humaine, plutôt qu’ordinateur, destinataires de tous les clients.</span><span class="sxs-lookup"><span data-stu-id="69bbb-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="69bbb-106">Les messages échangés entre les destinataires humaines sont appelés des messages interpersonnels et cette arborescence est connue en tant que message interpersonnel ou IPM, la sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="69bbb-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="69bbb-107">Une sous-arborescence IPM pour une banque de remise comprend au moins les dossiers suivants :</span><span class="sxs-lookup"><span data-stu-id="69bbb-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="69bbb-108">Inbox</span><span class="sxs-lookup"><span data-stu-id="69bbb-108">Inbox</span></span>
    
- <span data-ttu-id="69bbb-109">La boîte d’envoi</span><span class="sxs-lookup"><span data-stu-id="69bbb-109">Outbox</span></span>
    
- <span data-ttu-id="69bbb-110">Éléments envoyés</span><span class="sxs-lookup"><span data-stu-id="69bbb-110">Sent Items</span></span>
    
- <span data-ttu-id="69bbb-111">Éléments supprimés</span><span class="sxs-lookup"><span data-stu-id="69bbb-111">Deleted Items</span></span>
    
<span data-ttu-id="69bbb-112">Ce sont les noms par défaut et les rôles pour chacun de ces dossiers ; un client peut spécifier ses propres noms si les noms par défaut ne sont pas appropriés.</span><span class="sxs-lookup"><span data-stu-id="69bbb-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="69bbb-113">MAPI attribue des noms par défaut et associations pour ces dossiers pour conserver les messages de disparaître par inadvertance si un client oublie à établir les dossiers de réception des messages.</span><span class="sxs-lookup"><span data-stu-id="69bbb-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="69bbb-114">Dans un contexte de Microsoft Office Outlook, une sous-arborescence IPM se compose des dossiers par défaut supplémentaires pour le calendrier, Contacts, tâches, Notes et Journal.</span><span class="sxs-lookup"><span data-stu-id="69bbb-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="69bbb-115">La boîte de réception conserve généralement les messages entrants et la boîte d’envoi conserve les messages sortants (autrement dit, les messages en attente d’être envoyés).</span><span class="sxs-lookup"><span data-stu-id="69bbb-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="69bbb-116">Le dossier éléments envoyés conserve une copie de chaque message envoyé si le client a défini la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) à l’identificateur d’entrée de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="69bbb-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="69bbb-117">Le dossier éléments supprimés contient les messages marqués pour suppression.</span><span class="sxs-lookup"><span data-stu-id="69bbb-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69bbb-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69bbb-118">See also</span></span>



[<span data-ttu-id="69bbb-119">Dossiers MAPI</span><span class="sxs-lookup"><span data-stu-id="69bbb-119">MAPI Folders</span></span>](mapi-folders.md)

