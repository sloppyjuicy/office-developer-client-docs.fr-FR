---
title: Télécharger État du dossier
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419568"
---
# <a name="upload-folder-state"></a><span data-ttu-id="f5ed0-103">Télécharger État du dossier</span><span class="sxs-lookup"><span data-stu-id="f5ed0-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="f5ed0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5ed0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f5ed0-105">Cette rubrique décrit ce qui se produit pendant l’état du dossier de chargement de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f5ed0-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f5ed0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5ed0-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="f5ed0-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="f5ed0-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="f5ed0-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="f5ed0-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="f5ed0-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="f5ed0-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="f5ed0-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="f5ed0-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="f5ed0-111">From this state:</span></span>  <br/> |[<span data-ttu-id="f5ed0-112">Télécharger hiérarchie</span><span class="sxs-lookup"><span data-stu-id="f5ed0-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="f5ed0-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="f5ed0-113">To this state:</span></span>  <br/> |<span data-ttu-id="f5ed0-114">Télécharger hiérarchie</span><span class="sxs-lookup"><span data-stu-id="f5ed0-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="f5ed0-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="f5ed0-116">Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="f5ed0-117">Description</span><span class="sxs-lookup"><span data-stu-id="f5ed0-117">Description</span></span>

<span data-ttu-id="f5ed0-118">Cet état lance le téléchargement d’un dossier dans une hiérarchie qui a été spécifiée dans un état de hiérarchie de téléchargement précédent.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="f5ed0-119">Pendant cet état, Outlook fournit l’objet dossier (s’il n’a pas été supprimé) et les indicateurs indiquant l’état du dossier (nouveau, déplacé, modifié ou supprimé) dans le cadre de la structure de données **UPFLD** correspondante.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="f5ed0-120">Le client charge ensuite ces informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="f5ed0-121">Si le chargement réussit, le client définit  *ulFlags*  dans **UPFLD** sur **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="f5ed0-122">Outlook effacer ensuite ses informations internes sur la demande de téléchargement du dossier.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="f5ed0-123">Lorsque le chargement du dossier se termine, la boutique locale revient à l’état de hiérarchie de chargement.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="f5ed0-124">En fonction de la structure **[UPHIER](uphier.md)** correspondant à l’état de hiérarchie de chargement précédent, Outlook détermine s’il faut poursuivre le chargement du dossier suivant et préparer l’état du dossier de chargement suivant.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f5ed0-125">Si le client n’a besoin de télécharger qu’un seul dossier, il peut lancer la réplication via l’état de synchronisation sans passer par l’état de hiérarchie de téléchargement. [](synchronize-state.md)</span><span class="sxs-lookup"><span data-stu-id="f5ed0-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="f5ed0-126">Le client définit certains  membres de **[SYNC](sync.md)** *(ulFlags* sur **UPS_UPLOAD_ONLY** et **UPS_ONE_FOLDER** et sur l’ID du dossier) pour indiquer à Outlook qu’un seul dossier sera téléchargé.</span><span class="sxs-lookup"><span data-stu-id="f5ed0-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5ed0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5ed0-127">See also</span></span>



[<span data-ttu-id="f5ed0-128">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="f5ed0-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f5ed0-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f5ed0-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f5ed0-130">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="f5ed0-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f5ed0-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="f5ed0-131">SYNCSTATE</span></span>](syncstate.md)

