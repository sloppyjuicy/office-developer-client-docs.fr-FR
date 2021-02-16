---
title: Synchroniser l’état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414626"
---
# <a name="synchronize-state"></a><span data-ttu-id="a9889-103">Synchroniser l’état</span><span class="sxs-lookup"><span data-stu-id="a9889-103">Synchronize State</span></span>

  
  
<span data-ttu-id="a9889-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a9889-105">Cette rubrique décrit ce qui se produit pendant l’état de synchronisation de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="a9889-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a9889-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a9889-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9889-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="a9889-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a9889-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="a9889-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="a9889-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="a9889-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a9889-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="a9889-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="a9889-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="a9889-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a9889-112">État inactif</span><span class="sxs-lookup"><span data-stu-id="a9889-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="a9889-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="a9889-113">To this state:</span></span>  <br/> |<span data-ttu-id="a9889-114">[Télécharger l’état de la hiérarchie,](download-hierarchy-state.md) [synchroniser l’état du contenu,](synchronize-contents-state.md) [télécharger l’état de la](upload-hierarchy-state.md)hiérarchie ou l’état inactif</span><span class="sxs-lookup"><span data-stu-id="a9889-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a9889-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="a9889-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a9889-116">Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="a9889-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a9889-117">Description</span><span class="sxs-lookup"><span data-stu-id="a9889-117">Description</span></span>

<span data-ttu-id="a9889-118">Cet état lance la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a9889-118">This state initiates synchronization.</span></span> <span data-ttu-id="a9889-119">Un magasin local peut passer à un état de chargement ou de téléchargement à partir d’ici.</span><span class="sxs-lookup"><span data-stu-id="a9889-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="a9889-120">Par exemple, un magasin local peut passer à l’état de hiérarchie de téléchargement pour télécharger une hiérarchie de dossiers sur le serveur, ou il peut effectuer une synchronisation complète en téléchargeant d’abord la hiérarchie, puis en téléchargeant la hiérarchie à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="a9889-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="a9889-121">Pendant cet état, Outlook initialise la structure de données **SYNC** associée avec le chemin d’accès au magasin local, afin qu’Outlook voit les modifications pendant d’autres états.</span><span class="sxs-lookup"><span data-stu-id="a9889-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="a9889-122">Le client définit les membres [in] **de SYNC**, qui indique à Outlook comment gérer d’autres états.</span><span class="sxs-lookup"><span data-stu-id="a9889-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="a9889-123">Par exemple, le client peut définir  *ulFlags*  sur **UPS_UPLOAD_ONLY** et **UPS_THESE_FOLDERS** et  *pel*  à une liste d’identificateurs d’entrée des dossiers pour indiquer à Outlook que seuls ces dossiers seront téléchargés.</span><span class="sxs-lookup"><span data-stu-id="a9889-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="a9889-124">Lorsque cet état se termine, le magasin local revient à l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="a9889-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9889-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9889-125">See also</span></span>



[<span data-ttu-id="a9889-126">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="a9889-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a9889-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a9889-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a9889-128">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="a9889-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a9889-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a9889-129">SYNCSTATE</span></span>](syncstate.md)

