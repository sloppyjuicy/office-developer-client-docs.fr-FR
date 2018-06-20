---
title: État de synchronisation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787321"
---
# <a name="synchronize-state"></a><span data-ttu-id="87587-103">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="87587-103">Synchronize State</span></span>

  
  
<span data-ttu-id="87587-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87587-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="87587-105">Cette rubrique décrit le déroulement de l’état de synchronisation de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="87587-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="87587-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="87587-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87587-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="87587-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="87587-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="87587-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="87587-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="87587-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="87587-110">**[SYNCHRONISATION](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="87587-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="87587-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="87587-111">From this state:</span></span>  <br/> |[<span data-ttu-id="87587-112">État inactif</span><span class="sxs-lookup"><span data-stu-id="87587-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="87587-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="87587-113">To this state:</span></span>  <br/> |<span data-ttu-id="87587-114">[État de la hiérarchie du téléchargement](download-hierarchy-state.md), [synchroniser le contenu d’un état](synchronize-contents-state.md), [Téléchargez l’état de la hiérarchie](upload-hierarchy-state.md)ou inactif</span><span class="sxs-lookup"><span data-stu-id="87587-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="87587-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="87587-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="87587-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="87587-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="87587-117">Description</span><span class="sxs-lookup"><span data-stu-id="87587-117">Description</span></span>

<span data-ttu-id="87587-118">Cet état lance la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="87587-118">This state initiates synchronization.</span></span> <span data-ttu-id="87587-119">Un magasin local peut passer à un téléchargement ou d’un état de téléchargement à partir d’ici.</span><span class="sxs-lookup"><span data-stu-id="87587-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="87587-120">Par exemple, un magasin local peut passer à l’état de hiérarchie de téléchargement pour télécharger une hiérarchie de dossiers sur le serveur, ou elle peut effectuer une synchronisation complète en premier téléchargement de la hiérarchie, puis la hiérarchie à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="87587-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="87587-121">Au cours de cet état, Outlook initialise la structure de données de **synchronisation** associée avec le chemin d’accès dans le magasin local, afin qu’Outlook voit les modifications au cours des autres États.</span><span class="sxs-lookup"><span data-stu-id="87587-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="87587-122">Le client définit le [in] les membres de la **synchronisation**, ce qui indique comment gérer les autres États à Outlook.</span><span class="sxs-lookup"><span data-stu-id="87587-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="87587-123">Par exemple, le client peut définir *ulFlags* **UPS_UPLOAD_ONLY** et **UPS_THESE_FOLDERS** et *pel* à une liste d’identificateurs d’entrée des dossiers pour indiquer à Outlook que seuls ces dossiers sera téléchargé.</span><span class="sxs-lookup"><span data-stu-id="87587-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="87587-124">Lorsque cet état se termine, la banque locale revient à l’état est inactif.</span><span class="sxs-lookup"><span data-stu-id="87587-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87587-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87587-125">See also</span></span>



[<span data-ttu-id="87587-126">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="87587-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="87587-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="87587-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="87587-128">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="87587-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="87587-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="87587-129">SYNCSTATE</span></span>](syncstate.md)

