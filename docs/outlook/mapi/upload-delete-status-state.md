---
title: Télécharger l’état de suppression d’état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425840"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="59a79-103">Télécharger l’état de suppression d’état</span><span class="sxs-lookup"><span data-stu-id="59a79-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="59a79-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59a79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="59a79-105">Cette rubrique décrit ce qui se produit lors de l’état de suppression de téléchargement de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="59a79-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="59a79-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="59a79-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59a79-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="59a79-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="59a79-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="59a79-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="59a79-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="59a79-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="59a79-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="59a79-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="59a79-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="59a79-111">From this state:</span></span>  <br/> |[<span data-ttu-id="59a79-112">Charger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="59a79-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="59a79-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="59a79-113">To this state:</span></span>  <br/> |<span data-ttu-id="59a79-114">Charger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="59a79-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="59a79-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="59a79-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="59a79-116">Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="59a79-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="59a79-117">Description</span><span class="sxs-lookup"><span data-stu-id="59a79-117">Description</span></span>

<span data-ttu-id="59a79-118">Cet état lance la mise à jour sur un serveur des éléments Outlook (courrier, calendrier, contact, tâche, note ou journal) qui ont été supprimés dans un dossier d’un magasin local spécifié dans un état de table de chargement précédent.</span><span class="sxs-lookup"><span data-stu-id="59a79-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="59a79-119">Pendant cet état, Outlook initialise les membres de la structure de données **UPDEL** associée avec les informations des éléments qui ont été supprimés ou déplacés du dossier.</span><span class="sxs-lookup"><span data-stu-id="59a79-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="59a79-120">Le client supprime ensuite les éléments spécifiés dans le dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="59a79-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="59a79-121">Pour distinguer les éléments qui ont été déplacés au lieu d’avoir été supprimés, le client doit vérifier les *membresmov* identifiés dans la structure **UPDEL.**</span><span class="sxs-lookup"><span data-stu-id="59a79-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="59a79-122">Lorsque cet état se termine, Outlook efface les informations internes indiquant que l’élément a été supprimé ; Par conséquent, Outlook n’aura plus d’enregistrement de l’élément.</span><span class="sxs-lookup"><span data-stu-id="59a79-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="59a79-123">La boutique locale revient à l’état de la table de chargement.</span><span class="sxs-lookup"><span data-stu-id="59a79-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59a79-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59a79-124">See also</span></span>



[<span data-ttu-id="59a79-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="59a79-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="59a79-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="59a79-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="59a79-127">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="59a79-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="59a79-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="59a79-128">SYNCSTATE</span></span>](syncstate.md)

