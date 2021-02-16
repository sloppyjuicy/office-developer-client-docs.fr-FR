---
title: Télécharger l’état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337008"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="3e85b-103">Télécharger l’état de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="3e85b-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="3e85b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e85b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3e85b-105">Cette rubrique décrit ce qui se produit pendant l’état de la hiérarchie de téléchargement de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="3e85b-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3e85b-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3e85b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e85b-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="3e85b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3e85b-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="3e85b-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="3e85b-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="3e85b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3e85b-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="3e85b-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="3e85b-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="3e85b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3e85b-112">Synchronisation de l’état</span><span class="sxs-lookup"><span data-stu-id="3e85b-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="3e85b-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="3e85b-113">To this state:</span></span>  <br/> |<span data-ttu-id="3e85b-114">Synchronisation de l’état</span><span class="sxs-lookup"><span data-stu-id="3e85b-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3e85b-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="3e85b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3e85b-116">Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="3e85b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3e85b-117">Description</span><span class="sxs-lookup"><span data-stu-id="3e85b-117">Description</span></span>

<span data-ttu-id="3e85b-118">Cet état lance le téléchargement d’une hiérarchie d’arborescences de dossiers à partir d’un serveur vers le magasin local.</span><span class="sxs-lookup"><span data-stu-id="3e85b-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="3e85b-119">Outlook initialise la structure de données **DNHIER** associée avec un pointeur vers la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="3e85b-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="3e85b-120">Le client télécharge la hiérarchie et insère de nouveaux dossiers ou modifications dans les dossiers de la boutique locale.</span><span class="sxs-lookup"><span data-stu-id="3e85b-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="3e85b-121">Le processus de téléchargement adopte microsoft Exchange Incremental Change Synchronization (ICS).</span><span class="sxs-lookup"><span data-stu-id="3e85b-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="3e85b-122">Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3e85b-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="3e85b-123">Lorsque cet état se termine, le magasin local revient à l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="3e85b-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e85b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e85b-124">See also</span></span>



[<span data-ttu-id="3e85b-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="3e85b-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3e85b-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="3e85b-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3e85b-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="3e85b-127">SYNCSTATE</span></span>](syncstate.md)

