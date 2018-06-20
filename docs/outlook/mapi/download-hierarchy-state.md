---
title: État de hiérarchie de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e31a2a9c45a8896efbc43eb7f4b22f31f51e4013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783200"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="fd323-103">État de hiérarchie de téléchargement</span><span class="sxs-lookup"><span data-stu-id="fd323-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="fd323-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd323-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="fd323-105">Cette rubrique décrit le déroulement de l’état de hiérarchie de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="fd323-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fd323-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="fd323-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd323-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="fd323-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="fd323-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="fd323-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="fd323-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="fd323-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="fd323-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="fd323-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="fd323-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="fd323-111">From this state:</span></span>  <br/> |[<span data-ttu-id="fd323-112">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="fd323-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="fd323-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="fd323-113">To this state:</span></span>  <br/> |<span data-ttu-id="fd323-114">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="fd323-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="fd323-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="fd323-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="fd323-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="fd323-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="fd323-117">Description</span><span class="sxs-lookup"><span data-stu-id="fd323-117">Description</span></span>

<span data-ttu-id="fd323-118">Cet état lance le téléchargement d’une hiérarchie d’arborescence de dossiers à partir d’un serveur dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="fd323-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="fd323-119">Outlook initialise la structure de données **DNHIER** associée avec un pointeur vers la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="fd323-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="fd323-120">Le client télécharge la hiérarchie et insérer des dossiers ou des modifications de dossiers dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="fd323-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="fd323-121">Le processus de téléchargement adopte synchronisation modification incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="fd323-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="fd323-122">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd323-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="fd323-123">Lorsque cet état se termine, la banque locale renvoie l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="fd323-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd323-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd323-124">See also</span></span>



[<span data-ttu-id="fd323-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="fd323-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="fd323-126">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="fd323-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="fd323-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="fd323-127">SYNCSTATE</span></span>](syncstate.md)

