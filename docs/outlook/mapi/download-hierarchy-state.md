---
title: Télécharger l'état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337008"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="d1593-103">Télécharger l'état de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="d1593-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="d1593-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1593-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="d1593-105">Cette rubrique décrit ce qui se passe lors de l'état de la hiérarchie de téléchargement de la machine à États de réplication.</span><span class="sxs-lookup"><span data-stu-id="d1593-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d1593-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d1593-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1593-107">Identificateur d'État:</span><span class="sxs-lookup"><span data-stu-id="d1593-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="d1593-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="d1593-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="d1593-109">Structure de données associée:</span><span class="sxs-lookup"><span data-stu-id="d1593-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="d1593-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="d1593-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="d1593-111">À partir de cet État:</span><span class="sxs-lookup"><span data-stu-id="d1593-111">From this state:</span></span>  <br/> |[<span data-ttu-id="d1593-112">Synchronisation de l’état</span><span class="sxs-lookup"><span data-stu-id="d1593-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="d1593-113">À cet État:</span><span class="sxs-lookup"><span data-stu-id="d1593-113">To this state:</span></span>  <br/> |<span data-ttu-id="d1593-114">Synchronisation de l’état</span><span class="sxs-lookup"><span data-stu-id="d1593-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="d1593-115">L'ordinateur d'état de réplication est un ordinateur d'État déterministe.</span><span class="sxs-lookup"><span data-stu-id="d1593-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="d1593-116">Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="d1593-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="d1593-117">Description</span><span class="sxs-lookup"><span data-stu-id="d1593-117">Description</span></span>

<span data-ttu-id="d1593-118">Cet État lance le téléchargement d'une hiérarchie d'arborescence de dossiers à partir d'un serveur vers le magasin local.</span><span class="sxs-lookup"><span data-stu-id="d1593-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="d1593-119">Outlook initialise la structure de données **DNHIER** associée à l'aide d'un pointeur vers la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="d1593-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="d1593-120">Le client télécharge la hiérarchie et insère de nouveaux dossiers ou des modifications apportées aux dossiers dans la banque locale.</span><span class="sxs-lookup"><span data-stu-id="d1593-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="d1593-121">Le processus de téléchargement adopte la synchronisation des modifications incrémentielles Microsoft Exchange (ICS).</span><span class="sxs-lookup"><span data-stu-id="d1593-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="d1593-122">Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1593-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="d1593-123">Lorsque cet État se termine, le magasin local revient à l'État Synchronize.</span><span class="sxs-lookup"><span data-stu-id="d1593-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1593-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1593-124">See also</span></span>



[<span data-ttu-id="d1593-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="d1593-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d1593-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="d1593-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d1593-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="d1593-127">SYNCSTATE</span></span>](syncstate.md)

