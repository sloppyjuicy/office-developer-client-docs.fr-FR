---
title: État du dossier de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 82b00a33c5de11b3fc9ccd3bde4cf31c79b99c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787420"
---
# <a name="upload-folder-state"></a><span data-ttu-id="b4caa-103">État du dossier de téléchargement</span><span class="sxs-lookup"><span data-stu-id="b4caa-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="b4caa-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4caa-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="b4caa-105">Cette rubrique décrit le déroulement de l’état du dossier de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="b4caa-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b4caa-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="b4caa-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4caa-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="b4caa-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b4caa-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="b4caa-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="b4caa-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="b4caa-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b4caa-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="b4caa-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="b4caa-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="b4caa-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b4caa-112">Télécharger l’état de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="b4caa-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="b4caa-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="b4caa-113">To this state:</span></span>  <br/> |<span data-ttu-id="b4caa-114">Télécharger l’état de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="b4caa-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b4caa-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="b4caa-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b4caa-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="b4caa-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b4caa-117">Description</span><span class="sxs-lookup"><span data-stu-id="b4caa-117">Description</span></span>

<span data-ttu-id="b4caa-118">Cet état lance le téléchargement d’un dossier dans une hiérarchie a été spécifié dans un état de hiérarchie de téléchargement précédent.</span><span class="sxs-lookup"><span data-stu-id="b4caa-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="b4caa-119">Au cours de cet état, Outlook fournit l’objet folder (si elle n’a pas été supprimée) et les indicateurs indiquant l’état du dossier (nouveau, déplacé, modifié ou supprimé) dans le cadre de la structure de données **UPFLD** correspondante.</span><span class="sxs-lookup"><span data-stu-id="b4caa-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="b4caa-120">Le client télécharge ensuite ces informations vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="b4caa-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="b4caa-121">Si le transfert se déroule correctement, le client définit *ulFlags* dans **UPFLD** à **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="b4caa-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="b4caa-122">Ses informations internes sur la demande pour télécharger le dossier Outlook puis l’efface.</span><span class="sxs-lookup"><span data-stu-id="b4caa-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="b4caa-123">Lorsque le téléchargement du dossier se termine, la banque locale renvoie l’état de la hiérarchie de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="b4caa-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="b4caa-124">En fonction de la structure **[UPHIER](uphier.md)** correspondant à l’état de hiérarchie de téléchargement ci-dessus, Outlook détermine s’il afin de passer à télécharger le dossier suivant et en vue de l’état du dossier de téléchargement suivant.</span><span class="sxs-lookup"><span data-stu-id="b4caa-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b4caa-125">Si le client doit ne télécharger qu’un seul dossier, le client peut lancer la réplication par le biais de l' [état de synchronisation](synchronize-state.md) sans saisir l’état de la hiérarchie de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="b4caa-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="b4caa-126">Le client définit certains membres de **[synchronisation](sync.md)** : *ulFlags* **UPS_UPLOAD_ONLY** **UPS_ONE_FOLDER** et *feid* à l’ID du dossier — pour indiquer à ce qu’un seul dossier Outlook sera téléchargé.</span><span class="sxs-lookup"><span data-stu-id="b4caa-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4caa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4caa-127">See also</span></span>



[<span data-ttu-id="b4caa-128">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="b4caa-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b4caa-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b4caa-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b4caa-130">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="b4caa-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b4caa-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b4caa-131">SYNCSTATE</span></span>](syncstate.md)

