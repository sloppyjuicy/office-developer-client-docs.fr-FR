---
title: Télécharger l’état du message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 430734fe98799c386e71612355b194a6b8edf00a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575412"
---
# <a name="upload-message-state"></a><span data-ttu-id="4e5c4-103">Télécharger l’état du message</span><span class="sxs-lookup"><span data-stu-id="4e5c4-103">Upload Message State</span></span>

  
  
<span data-ttu-id="4e5c4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e5c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4e5c4-105">Cette rubrique décrit le déroulement de l’état du message de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4e5c4-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4e5c4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e5c4-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="4e5c4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4e5c4-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="4e5c4-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="4e5c4-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="4e5c4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4e5c4-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="4e5c4-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="4e5c4-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="4e5c4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4e5c4-112">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="4e5c4-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4e5c4-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="4e5c4-113">To this state:</span></span>  <br/> |<span data-ttu-id="4e5c4-114">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="4e5c4-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4e5c4-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4e5c4-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4e5c4-117">Description</span><span class="sxs-lookup"><span data-stu-id="4e5c4-117">Description</span></span>

<span data-ttu-id="4e5c4-118">Cet état lance le téléchargement d’un élément Outlook (courrier, calendrier, contact, tâche, une note ou journal) qui est nouveau ou a été déplacé vers le dossier actif, ou qui ont été modifiée.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="4e5c4-119">Outlook initialise la structure de données correpsonding **UPMSG** avec les informations appropriées pour l’élément comme étant ajouté, déplacé ou modifié.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="4e5c4-120">Si l’élément a été ajouté ou déplacé, le client puis correctement ajoute ou met à jour l’élément sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="4e5c4-121">Si l’élément a été modifié, Outlook plus spécifie dans la structure de données **UPMSG** si les modifications sont dans un en-tête de message (dans ce cas, l’élément est l’en-tête de message), dans les propriétés d’élément ou dans l’élément lui-même qui nécessite de conflit résolution.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="4e5c4-122">Le client met à jour l’élément sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="4e5c4-123">Lorsque le téléchargement de l’élément se termine, Outlook indique que le message a été téléchargé, afin qu’il ne sera pas traité dans un téléchargement suivant.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="4e5c4-124">Le magasin local renvoie l’état de la table de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e5c4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e5c4-125">See also</span></span>



[<span data-ttu-id="4e5c4-126">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="4e5c4-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4e5c4-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4e5c4-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4e5c4-128">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="4e5c4-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4e5c4-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4e5c4-129">SYNCSTATE</span></span>](syncstate.md)

