---
title: Télécharger l’état de suppression de statut
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4a45cfafec5126c72f365858e41963bc95fa707a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574544"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="8e795-103">Télécharger l’état de suppression de statut</span><span class="sxs-lookup"><span data-stu-id="8e795-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="8e795-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e795-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8e795-105">Cette rubrique décrit le déroulement de l’état de l’état de téléchargement supprimer de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="8e795-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8e795-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="8e795-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e795-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="8e795-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8e795-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="8e795-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="8e795-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="8e795-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="8e795-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="8e795-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="8e795-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="8e795-111">From this state:</span></span>  <br/> |[<span data-ttu-id="8e795-112">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="8e795-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="8e795-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="8e795-113">To this state:</span></span>  <br/> |<span data-ttu-id="8e795-114">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="8e795-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8e795-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="8e795-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8e795-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="8e795-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8e795-117">Description</span><span class="sxs-lookup"><span data-stu-id="8e795-117">Description</span></span>

<span data-ttu-id="8e795-118">Cet état lance la mise à jour sur un serveur, les éléments Outlook (courrier, calendrier, contact, tâche, une note ou journal) qui ont été supprimées dans un dossier sur un magasin local spécifié dans un état de table de téléchargement précédent.</span><span class="sxs-lookup"><span data-stu-id="8e795-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="8e795-119">Au cours de cet état, Outlook initialise les membres de la structure de données **UPDEL** associée avec des informations pour les éléments qui ont été supprimé ou déplacé à partir du dossier.</span><span class="sxs-lookup"><span data-stu-id="8e795-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="8e795-120">Le client puis supprime les éléments spécifiés dans le dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="8e795-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="8e795-121">Pour distinguer les éléments qui ont été déplacés au lieu d’avoir été supprimé, le client doit vérifier les membres *pupmov* identifiés dans la structure **UPDEL** .</span><span class="sxs-lookup"><span data-stu-id="8e795-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="8e795-122">Lorsque cet état se termine, Outlook efface les informations internes indiquant que l’élément a été supprimé ; Par conséquent, Outlook n’aura plus un enregistrement de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8e795-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="8e795-123">Le magasin local renvoie l’état de la table de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="8e795-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e795-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e795-124">See also</span></span>



[<span data-ttu-id="8e795-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="8e795-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8e795-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e795-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8e795-127">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="8e795-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8e795-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="8e795-128">SYNCSTATE</span></span>](syncstate.md)

