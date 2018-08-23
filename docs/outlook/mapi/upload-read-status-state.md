---
title: Télécharger l’état de lecture de statut
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 41815a88fe1215d2a85a38592e04b0d0bbd43cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573046"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="7dffb-103">Télécharger l’état de lecture de statut</span><span class="sxs-lookup"><span data-stu-id="7dffb-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="7dffb-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dffb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7dffb-105">Cette rubrique décrit ce qui se produit lors du téléchargement de lire l’état de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="7dffb-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7dffb-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7dffb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dffb-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="7dffb-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="7dffb-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="7dffb-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="7dffb-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="7dffb-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="7dffb-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="7dffb-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="7dffb-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="7dffb-111">From this state:</span></span>  <br/> |[<span data-ttu-id="7dffb-112">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="7dffb-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="7dffb-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="7dffb-113">To this state:</span></span>  <br/> |<span data-ttu-id="7dffb-114">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="7dffb-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="7dffb-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="7dffb-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="7dffb-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="7dffb-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="7dffb-117">Description</span><span class="sxs-lookup"><span data-stu-id="7dffb-117">Description</span></span>

<span data-ttu-id="7dffb-118">Cet état lance le téléchargement de l’état de lecture d’éléments dans un dossier spécifié dans un état de table de téléchargement précédent.</span><span class="sxs-lookup"><span data-stu-id="7dffb-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="7dffb-119">Au cours de cet état, Outlook initialise la structure de données **UPREAD** associée avec des informations pour ces éléments dans le dossier dont l’état de lecture a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="7dffb-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="7dffb-120">Le client met à jour l’état de lecture de ces éléments sur le serveur comme étant lus ou non lus.</span><span class="sxs-lookup"><span data-stu-id="7dffb-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="7dffb-121">Lorsque cet état se termine, Outlook efface les informations internes sur l’état de la lecture, empêche le téléchargement à nouveau l’état de lecture.</span><span class="sxs-lookup"><span data-stu-id="7dffb-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="7dffb-122">Le magasin local renvoie l’état de la table de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="7dffb-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7dffb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dffb-123">See also</span></span>



[<span data-ttu-id="7dffb-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7dffb-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7dffb-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7dffb-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7dffb-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="7dffb-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7dffb-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="7dffb-127">SYNCSTATE</span></span>](syncstate.md)

