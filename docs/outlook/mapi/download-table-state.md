---
title: Télécharger l’état de la table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395069"
---
# <a name="download-table-state"></a><span data-ttu-id="7ac12-103">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="7ac12-103">Download Table State</span></span>

  
  
<span data-ttu-id="7ac12-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ac12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7ac12-105">Cette rubrique décrit le déroulement de l’état du tableau de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="7ac12-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7ac12-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7ac12-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ac12-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="7ac12-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="7ac12-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="7ac12-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="7ac12-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="7ac12-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="7ac12-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="7ac12-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="7ac12-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="7ac12-111">From this state:</span></span>  <br/> |[<span data-ttu-id="7ac12-112">Synchroniser le contenu d’un état</span><span class="sxs-lookup"><span data-stu-id="7ac12-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="7ac12-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="7ac12-113">To this state:</span></span>  <br/> |<span data-ttu-id="7ac12-114">Synchroniser le contenu d’un état</span><span class="sxs-lookup"><span data-stu-id="7ac12-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="7ac12-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="7ac12-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="7ac12-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="7ac12-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="7ac12-117">Description</span><span class="sxs-lookup"><span data-stu-id="7ac12-117">Description</span></span>

<span data-ttu-id="7ac12-118">Cet état lance le téléchargement d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="7ac12-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="7ac12-119">Au cours de cet état, Outlook initialise la structure de données **DNTBL** associée avec des informations sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="7ac12-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="7ac12-120">Le client télécharge le contenu du dossier et du stockage local le dossier des mises à jour avec le nouveau contenu, les modifications ou les suppressions à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="7ac12-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="7ac12-121">Le processus de téléchargement adopte synchronisation modification incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ac12-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="7ac12-122">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ac12-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="7ac12-123">Lorsque cet état se termine, la banque locale renvoie à l’état du contenu synchroniser.</span><span class="sxs-lookup"><span data-stu-id="7ac12-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ac12-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ac12-124">See also</span></span>



[<span data-ttu-id="7ac12-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="7ac12-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7ac12-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7ac12-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7ac12-127">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="7ac12-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7ac12-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="7ac12-128">SYNCSTATE</span></span>](syncstate.md)

