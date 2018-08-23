---
title: Télécharger l’état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f9c334bc86bdff4abb2762642a37e3f0933a0b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589027"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="db6a4-103">Télécharger l’état de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="db6a4-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="db6a4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db6a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="db6a4-105">Cette rubrique décrit le déroulement de l’état de hiérarchie de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="db6a4-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="db6a4-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="db6a4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db6a4-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="db6a4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="db6a4-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="db6a4-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="db6a4-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="db6a4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="db6a4-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="db6a4-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="db6a4-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="db6a4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="db6a4-112">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="db6a4-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="db6a4-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="db6a4-113">To this state:</span></span>  <br/> |<span data-ttu-id="db6a4-114">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="db6a4-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="db6a4-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="db6a4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="db6a4-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="db6a4-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="db6a4-117">Description</span><span class="sxs-lookup"><span data-stu-id="db6a4-117">Description</span></span>

<span data-ttu-id="db6a4-118">Cet état lance le téléchargement d’une hiérarchie d’arborescence de dossiers à partir d’un serveur dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="db6a4-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="db6a4-119">Outlook initialise la structure de données **DNHIER** associée avec un pointeur vers la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="db6a4-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="db6a4-120">Le client télécharge la hiérarchie et insérer des dossiers ou des modifications de dossiers dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="db6a4-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="db6a4-121">Le processus de téléchargement adopte synchronisation modification incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="db6a4-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="db6a4-122">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="db6a4-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="db6a4-123">Lorsque cet état se termine, la banque locale renvoie l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="db6a4-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db6a4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db6a4-124">See also</span></span>



[<span data-ttu-id="db6a4-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="db6a4-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="db6a4-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="db6a4-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="db6a4-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="db6a4-127">SYNCSTATE</span></span>](syncstate.md)

