---
title: Suppression d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad891a9884e72aa352dc114232cd5951c590272f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585100"
---
# <a name="deleting-a-message"></a><span data-ttu-id="59f43-103">Suppression d’un message</span><span class="sxs-lookup"><span data-stu-id="59f43-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="59f43-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59f43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59f43-105">Un client peut supprimer un message lorsqu’il est ouvert et que l’utilisateur est le lire, ou lorsqu’elle est fermée et l’utilisateur visualise la table des matières.</span><span class="sxs-lookup"><span data-stu-id="59f43-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="59f43-106">Pour empêcher un utilisateur de suppression par inadvertance d’un message, MAPI définit la suppression des messages sous la forme d’un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="59f43-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="59f43-107">Marquer un message de suppression en les déplaçant vers le dossier qui a été désigné en tant que le dossier éléments supprimés, le dossier dont l’identificateur de l’entrée est stockée dans la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59f43-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="59f43-108">Supprimer le message en appelant la méthode [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) .</span><span class="sxs-lookup"><span data-stu-id="59f43-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="59f43-109">Lorsqu’un utilisateur choisit supprimer un message dans un dossier autre que le dossier éléments supprimés, marquer pour la suppression.</span><span class="sxs-lookup"><span data-stu-id="59f43-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="59f43-110">Uniquement lorsqu’un utilisateur sélectionne des messages à partir du dossier éléments supprimés doivent les messages d’être physiquement retirés de la station de travail.</span><span class="sxs-lookup"><span data-stu-id="59f43-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="59f43-111">Vous pouvez inviter l’utilisateur à vérifier que l’utilisateur prévu effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="59f43-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="59f43-112">**Pour supprimer un message**</span><span class="sxs-lookup"><span data-stu-id="59f43-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="59f43-113">Avec l’utilisateur, vérifiez que la suppression imminente est intentionnelle.</span><span class="sxs-lookup"><span data-stu-id="59f43-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="59f43-114">Déterminer le parent du dossier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="59f43-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="59f43-115">Si c’est le dossier éléments supprimés ou un sous-dossier dans le dossier éléments supprimés, appelez [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) pour supprimer le message.</span><span class="sxs-lookup"><span data-stu-id="59f43-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="59f43-116">Si le dossier n’est pas contenu dans le dossier éléments supprimés, appelez [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) avec l’indicateur MESSAGE_MOVE pour déplacer le message vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="59f43-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

