---
title: Télécharger l’état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384856"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="3f3b0-103">Télécharger l’état de la hiérarchie</span><span class="sxs-lookup"><span data-stu-id="3f3b0-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="3f3b0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f3b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3f3b0-105">Cette rubrique décrit le déroulement de l’état de hiérarchie de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3f3b0-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3f3b0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f3b0-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="3f3b0-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3f3b0-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="3f3b0-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="3f3b0-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="3f3b0-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3f3b0-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="3f3b0-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="3f3b0-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="3f3b0-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3f3b0-112">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="3f3b0-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="3f3b0-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="3f3b0-113">To this state:</span></span>  <br/> |<span data-ttu-id="3f3b0-114">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="3f3b0-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3f3b0-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3f3b0-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3f3b0-117">Description</span><span class="sxs-lookup"><span data-stu-id="3f3b0-117">Description</span></span>

<span data-ttu-id="3f3b0-118">Cet état lance le téléchargement d’une hiérarchie d’arborescence de dossiers à partir d’un serveur dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="3f3b0-119">Outlook initialise la structure de données **DNHIER** associée avec un pointeur vers la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="3f3b0-120">Le client télécharge la hiérarchie et insérer des dossiers ou des modifications de dossiers dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="3f3b0-121">Le processus de téléchargement adopte synchronisation modification incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="3f3b0-122">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f3b0-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="3f3b0-123">Lorsque cet état se termine, la banque locale renvoie l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="3f3b0-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f3b0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f3b0-124">See also</span></span>



[<span data-ttu-id="3f3b0-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="3f3b0-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3f3b0-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="3f3b0-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3f3b0-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="3f3b0-127">SYNCSTATE</span></span>](syncstate.md)

