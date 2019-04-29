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
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421220"
---
# <a name="ipm-subtree"></a><span data-ttu-id="4c1fa-103">Sous-arborescence IPM</span><span class="sxs-lookup"><span data-stu-id="4c1fa-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="4c1fa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c1fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c1fa-105">MAPI crée une arborescence de dossiers sous le dossier racine d'une banque de messages pour tous les clients qui envoient et reçoivent des messages provenant de personnes, et non de destinataires.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="4c1fa-106">Les messages échangés entre les destinataires humains sont appelés messages interpersonnels et cet arbre est appelé message interpersonnel ou IPM, sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="4c1fa-107">Une sous-arborescence IPM pour un magasin de remise se compose au moins des dossiers suivants:</span><span class="sxs-lookup"><span data-stu-id="4c1fa-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="4c1fa-108">Boîte de réception</span><span class="sxs-lookup"><span data-stu-id="4c1fa-108">Inbox</span></span>
    
- <span data-ttu-id="4c1fa-109">Boîte d'envoi</span><span class="sxs-lookup"><span data-stu-id="4c1fa-109">Outbox</span></span>
    
- <span data-ttu-id="4c1fa-110">Éléments envoyés</span><span class="sxs-lookup"><span data-stu-id="4c1fa-110">Sent Items</span></span>
    
- <span data-ttu-id="4c1fa-111">Éléments supprimés</span><span class="sxs-lookup"><span data-stu-id="4c1fa-111">Deleted Items</span></span>
    
<span data-ttu-id="4c1fa-112">Il s'agit des noms et des rôles par défaut pour chacun de ces dossiers; un client peut spécifier ses propres noms si les noms par défaut ne sont pas appropriés.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="4c1fa-113">MAPI affecte des noms et des associations par défaut pour ces dossiers de sorte que les messages ne soient pas dévisibles par inadvertance si un client omet d'établir des dossiers de réception pour les messages.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="4c1fa-114">Dans un contexte Microsoft Office Outlook, une sous-arborescence IPM est constituée de dossiers par défaut supplémentaires pour le calendrier, les contacts, les tâches, les notes et le journal.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="4c1fa-115">La boîte de réception contient généralement des messages entrants et la boîte d'envoi conserve les messages sortants (c'est-à-dire, les messages en attente d'envoi).</span><span class="sxs-lookup"><span data-stu-id="4c1fa-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="4c1fa-116">Le dossier éléments envoyés contient une copie de chaque message envoyé si le client a défini la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) à l'identificateur d'entrée de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="4c1fa-117">Le dossier éléments supprimés contient les messages marqués pour suppression.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c1fa-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c1fa-118">See also</span></span>



[<span data-ttu-id="4c1fa-119">Dossiers MAPI</span><span class="sxs-lookup"><span data-stu-id="4c1fa-119">MAPI Folders</span></span>](mapi-folders.md)

