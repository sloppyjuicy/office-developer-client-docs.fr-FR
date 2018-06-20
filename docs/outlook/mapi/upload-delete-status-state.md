---
title: État de la suppression de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ff957e649d5de64c65ac169b3bc413ac7b6c9491
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787426"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="e8fd1-103">État de la suppression de téléchargement</span><span class="sxs-lookup"><span data-stu-id="e8fd1-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="e8fd1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e8fd1-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="e8fd1-105">Cette rubrique décrit le déroulement de l’état de l’état de téléchargement supprimer de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e8fd1-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="e8fd1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8fd1-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="e8fd1-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e8fd1-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="e8fd1-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="e8fd1-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="e8fd1-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e8fd1-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="e8fd1-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="e8fd1-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="e8fd1-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e8fd1-112">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="e8fd1-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="e8fd1-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="e8fd1-113">To this state:</span></span>  <br/> |<span data-ttu-id="e8fd1-114">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="e8fd1-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e8fd1-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e8fd1-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e8fd1-117">Description</span><span class="sxs-lookup"><span data-stu-id="e8fd1-117">Description</span></span>

<span data-ttu-id="e8fd1-118">Cet état lance la mise à jour sur un serveur, les éléments Outlook (courrier, calendrier, contact, tâche, une note ou journal) qui ont été supprimées dans un dossier sur un magasin local spécifié dans un état de table de téléchargement précédent.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="e8fd1-119">Au cours de cet état, Outlook initialise les membres de la structure de données **UPDEL** associée avec des informations pour les éléments qui ont été supprimé ou déplacé à partir du dossier.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="e8fd1-120">Le client puis supprime les éléments spécifiés dans le dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="e8fd1-121">Pour distinguer les éléments qui ont été déplacés au lieu d’avoir été supprimé, le client doit vérifier les membres *pupmov* identifiés dans la structure **UPDEL** .</span><span class="sxs-lookup"><span data-stu-id="e8fd1-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="e8fd1-122">Lorsque cet état se termine, Outlook efface les informations internes indiquant que l’élément a été supprimé ; Par conséquent, Outlook n’aura plus un enregistrement de l’élément.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="e8fd1-123">Le magasin local renvoie l’état de la table de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="e8fd1-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8fd1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8fd1-124">See also</span></span>



[<span data-ttu-id="e8fd1-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="e8fd1-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e8fd1-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e8fd1-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e8fd1-127">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="e8fd1-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e8fd1-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e8fd1-128">SYNCSTATE</span></span>](syncstate.md)

