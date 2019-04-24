---
title: Charger l'état du message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332633"
---
# <a name="upload-message-state"></a><span data-ttu-id="7fda8-103">Charger l'état du message</span><span class="sxs-lookup"><span data-stu-id="7fda8-103">Upload Message State</span></span>

  
  
<span data-ttu-id="7fda8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fda8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7fda8-105">Cette rubrique décrit ce qui se passe lors de l'état du message de téléchargement de la machine à États de réplication.</span><span class="sxs-lookup"><span data-stu-id="7fda8-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7fda8-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7fda8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fda8-107">Identificateur d'État:</span><span class="sxs-lookup"><span data-stu-id="7fda8-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="7fda8-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="7fda8-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="7fda8-109">Structure de données associée:</span><span class="sxs-lookup"><span data-stu-id="7fda8-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="7fda8-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="7fda8-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="7fda8-111">À partir de cet État:</span><span class="sxs-lookup"><span data-stu-id="7fda8-111">From this state:</span></span>  <br/> |[<span data-ttu-id="7fda8-112">Charger l'état de la table</span><span class="sxs-lookup"><span data-stu-id="7fda8-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="7fda8-113">À cet État:</span><span class="sxs-lookup"><span data-stu-id="7fda8-113">To this state:</span></span>  <br/> |<span data-ttu-id="7fda8-114">Charger l'état de la table</span><span class="sxs-lookup"><span data-stu-id="7fda8-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="7fda8-115">L'ordinateur d'état de réplication est un ordinateur d'État déterministe.</span><span class="sxs-lookup"><span data-stu-id="7fda8-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="7fda8-116">Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="7fda8-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="7fda8-117">Description</span><span class="sxs-lookup"><span data-stu-id="7fda8-117">Description</span></span>

<span data-ttu-id="7fda8-118">Cet État lance le téléchargement d'un élément Outlook (courrier, calendrier, contact, tâche, note ou journal) qui est nouveau ou qui a été déplacé vers le dossier actif ou qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="7fda8-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="7fda8-119">Outlook initialise la structure de données correpsonding **UPMSG** avec les informations appropriées pour l'élément comme étant ajoutée, déplacée ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="7fda8-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="7fda8-120">Si l'élément a été ajouté ou déplacé, le client ajoute ou met à jour de manière appropriée l'élément sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7fda8-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="7fda8-121">Si l'élément a été modifié, Outlook spécifie, dans la structure de données **UPMSG** , si les modifications figurent dans un en-tête de message (auquel cas l'élément est l'en-tête du message), dans les propriétés de l'élément ou dans l'élément lui-même qui nécessite un conflit. résolution.</span><span class="sxs-lookup"><span data-stu-id="7fda8-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="7fda8-122">Le client met ensuite à jour l'élément sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7fda8-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="7fda8-123">Une fois le téléchargement de l'élément terminé, Outlook note que le message a été téléchargé, afin qu'il ne soit pas traité lors d'un téléchargement ultérieur.</span><span class="sxs-lookup"><span data-stu-id="7fda8-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="7fda8-124">Le magasin local revient à l'état de la table de chargement.</span><span class="sxs-lookup"><span data-stu-id="7fda8-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7fda8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fda8-125">See also</span></span>



[<span data-ttu-id="7fda8-126">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7fda8-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7fda8-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7fda8-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7fda8-128">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="7fda8-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7fda8-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="7fda8-129">SYNCSTATE</span></span>](syncstate.md)

