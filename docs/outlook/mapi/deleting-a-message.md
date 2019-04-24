---
title: Suppression d'un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316834"
---
# <a name="deleting-a-message"></a><span data-ttu-id="2c512-103">Suppression d'un message</span><span class="sxs-lookup"><span data-stu-id="2c512-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="2c512-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c512-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c512-105">Un client peut supprimer un message lorsqu'il est ouvert et que l'utilisateur le lit, ou lorsqu'il est fermé et que l'utilisateur affiche la table des matières.</span><span class="sxs-lookup"><span data-stu-id="2c512-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="2c512-106">Pour empêcher un utilisateur de supprimer un message par inadvertance, MAPI définit la suppression des messages comme un processus en deux étapes:</span><span class="sxs-lookup"><span data-stu-id="2c512-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="2c512-107">Marquer un message pour suppression en le dépositionnant vers le dossier désigné comme dossier éléments supprimés — le dossier dont l'identificateur d'entrée est stocké dans la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c512-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="2c512-108">Supprimez le message en appelant la méthode [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) .</span><span class="sxs-lookup"><span data-stu-id="2c512-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="2c512-109">Lorsqu'un utilisateur choisit de supprimer un message dans un dossier autre que le dossier éléments supprimés, marquez-le pour suppression.</span><span class="sxs-lookup"><span data-stu-id="2c512-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="2c512-110">Uniquement lorsqu'un utilisateur sélectionne des messages dans le dossier éléments supprimés si les messages doivent être supprimés physiquement de la station de travail.</span><span class="sxs-lookup"><span data-stu-id="2c512-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="2c512-111">Vous pouvez inviter l'utilisateur à vérifier que l'utilisateur a réellement prévu d'effectuer la suppression.</span><span class="sxs-lookup"><span data-stu-id="2c512-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="2c512-112">**Pour supprimer un message**</span><span class="sxs-lookup"><span data-stu-id="2c512-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="2c512-113">Vérifiez auprès de l'utilisateur que la suppression imminente est intentionnelle.</span><span class="sxs-lookup"><span data-stu-id="2c512-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="2c512-114">Déterminez le parent du dossier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="2c512-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="2c512-115">S'il s'agit du dossier éléments supprimés ou d'un sous-dossier dans le dossier éléments supprimés, appelez [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) pour supprimer le message.</span><span class="sxs-lookup"><span data-stu-id="2c512-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="2c512-116">Si le dossier n'est pas contenu dans le dossier éléments supprimés, appelez [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) avec l'indicateur MESSAGE_MOVE défini pour déplacer le message vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="2c512-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

