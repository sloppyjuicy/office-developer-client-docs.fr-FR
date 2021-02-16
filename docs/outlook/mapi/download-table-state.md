---
title: Télécharger l’état du tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338338"
---
# <a name="download-table-state"></a><span data-ttu-id="25ec2-103">Télécharger l’état du tableau</span><span class="sxs-lookup"><span data-stu-id="25ec2-103">Download Table State</span></span>

  
  
<span data-ttu-id="25ec2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25ec2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="25ec2-105">Cette rubrique décrit ce qui se produit pendant l’état de la table de téléchargement de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="25ec2-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="25ec2-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="25ec2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25ec2-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="25ec2-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="25ec2-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="25ec2-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="25ec2-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="25ec2-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="25ec2-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="25ec2-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="25ec2-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="25ec2-111">From this state:</span></span>  <br/> |[<span data-ttu-id="25ec2-112">Synchroniser l’état du contenu</span><span class="sxs-lookup"><span data-stu-id="25ec2-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="25ec2-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="25ec2-113">To this state:</span></span>  <br/> |<span data-ttu-id="25ec2-114">Synchroniser l’état du contenu</span><span class="sxs-lookup"><span data-stu-id="25ec2-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="25ec2-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="25ec2-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="25ec2-116">Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="25ec2-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="25ec2-117">Description</span><span class="sxs-lookup"><span data-stu-id="25ec2-117">Description</span></span>

<span data-ttu-id="25ec2-118">Cet état lance le téléchargement d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="25ec2-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="25ec2-119">Pendant cet état, Outlook initialise la structure de données **DNTBL** associée avec des informations sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="25ec2-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="25ec2-120">Le client télécharge le contenu du dossier et met à jour le dossier sur la boutique locale avec de nouveaux contenus, modifications ou suppressions à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="25ec2-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="25ec2-121">Le processus de téléchargement adopte microsoft Exchange Incremental Change Synchronization (ICS).</span><span class="sxs-lookup"><span data-stu-id="25ec2-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="25ec2-122">Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="25ec2-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="25ec2-123">Lorsque cet état se termine, la boutique locale revient à l’état de synchronisation du contenu.</span><span class="sxs-lookup"><span data-stu-id="25ec2-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25ec2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ec2-124">See also</span></span>



[<span data-ttu-id="25ec2-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="25ec2-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="25ec2-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="25ec2-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="25ec2-127">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="25ec2-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="25ec2-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="25ec2-128">SYNCSTATE</span></span>](syncstate.md)

