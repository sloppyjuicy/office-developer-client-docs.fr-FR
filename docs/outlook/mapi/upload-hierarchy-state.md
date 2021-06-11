---
title: Télécharger État de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415424"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="5b8ac-103">Télécharger État de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="5b8ac-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="5b8ac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b8ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5b8ac-105">Cette rubrique décrit ce qui se produit pendant l’état de la hiérarchie de chargement de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="5b8ac-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5b8ac-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="5b8ac-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b8ac-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="5b8ac-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="5b8ac-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="5b8ac-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="5b8ac-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="5b8ac-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="5b8ac-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="5b8ac-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="5b8ac-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="5b8ac-111">From this state:</span></span>  <br/> |[<span data-ttu-id="5b8ac-112">Synchronisation de l’état</span><span class="sxs-lookup"><span data-stu-id="5b8ac-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="5b8ac-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="5b8ac-113">To this state:</span></span>  <br/> |<span data-ttu-id="5b8ac-114">[Télécharger’état du dossier](upload-folder-state.md)ou synchroniser l’état</span><span class="sxs-lookup"><span data-stu-id="5b8ac-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="5b8ac-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="5b8ac-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="5b8ac-116">Un client qui quitte un état vers un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="5b8ac-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="5b8ac-117">Description</span><span class="sxs-lookup"><span data-stu-id="5b8ac-117">Description</span></span>

<span data-ttu-id="5b8ac-118">Cet état lance le téléchargement d’une hiérarchie d’arborescence de dossiers qui a été spécifiée dans un état de synchronisation précédent.</span><span class="sxs-lookup"><span data-stu-id="5b8ac-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="5b8ac-119">Outlook détermine le nombre de dossiers qui ont été créés ou modifiés dans cette hiérarchie et initialise *cEnt* dans **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="5b8ac-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="5b8ac-120">Outlook également le nombre de dossiers téléchargés avec un autre *iEnt membre.*</span><span class="sxs-lookup"><span data-stu-id="5b8ac-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="5b8ac-121">Pour télécharger chacun des dossiers  *cEnt,*  le client place la boutique locale dans l’état du dossier de chargement, en revenir à l’état de hiérarchie de chargement une fois le chargement du dossier terminé.</span><span class="sxs-lookup"><span data-stu-id="5b8ac-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="5b8ac-122">Lorsque l’état de la hiérarchie de chargement se termine, le magasin local revient à l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="5b8ac-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b8ac-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b8ac-123">See also</span></span>



[<span data-ttu-id="5b8ac-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="5b8ac-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5b8ac-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b8ac-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5b8ac-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="5b8ac-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5b8ac-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="5b8ac-127">SYNCSTATE</span></span>](syncstate.md)

