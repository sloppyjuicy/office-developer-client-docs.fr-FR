---
title: Télécharger l’état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3ed24682086556addf76b8451674a73bd82ce050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572185"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="c7bc0-103">Télécharger l’état de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="c7bc0-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="c7bc0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7bc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c7bc0-105">Cette rubrique décrit le déroulement de l’état de la hiérarchie de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="c7bc0-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c7bc0-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c7bc0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7bc0-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="c7bc0-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="c7bc0-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="c7bc0-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="c7bc0-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="c7bc0-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="c7bc0-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="c7bc0-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="c7bc0-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="c7bc0-111">From this state:</span></span>  <br/> |[<span data-ttu-id="c7bc0-112">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="c7bc0-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="c7bc0-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="c7bc0-113">To this state:</span></span>  <br/> |<span data-ttu-id="c7bc0-114">[Télécharger l’état du dossier](upload-folder-state.md), ou l’état de synchronisation</span><span class="sxs-lookup"><span data-stu-id="c7bc0-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c7bc0-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="c7bc0-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="c7bc0-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="c7bc0-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="c7bc0-117">Description</span><span class="sxs-lookup"><span data-stu-id="c7bc0-117">Description</span></span>

<span data-ttu-id="c7bc0-118">Cet état lance téléchargement d’une hiérarchie de dossiers qui a été spécifiée dans une synchroniser l’état.</span><span class="sxs-lookup"><span data-stu-id="c7bc0-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="c7bc0-119">Outlook détermine le nombre de dossiers qui ont été créés ou modifiés dans cette hiérarchie et initialise *cEnt* dans **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="c7bc0-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="c7bc0-120">Outlook conserve également le nombre de dossiers téléchargés avec un autre membre *iEnt* .</span><span class="sxs-lookup"><span data-stu-id="c7bc0-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="c7bc0-121">Pour chacun des dossiers *cEnt* télécharger, le client déplace le magasin local dans l’état du dossier téléchargement, renvoi à l’état de la hiérarchie de téléchargement lorsque le téléchargement du dossier se termine.</span><span class="sxs-lookup"><span data-stu-id="c7bc0-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="c7bc0-122">Lorsque l’état de la hiérarchie de téléchargement se termine, la banque locale renvoie l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c7bc0-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7bc0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7bc0-123">See also</span></span>



[<span data-ttu-id="c7bc0-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="c7bc0-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c7bc0-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c7bc0-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c7bc0-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="c7bc0-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c7bc0-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="c7bc0-127">SYNCSTATE</span></span>](syncstate.md)

