---
title: État inactif
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419477"
---
# <a name="idle-state"></a><span data-ttu-id="ef442-103">État inactif</span><span class="sxs-lookup"><span data-stu-id="ef442-103">Idle State</span></span>

  
  
<span data-ttu-id="ef442-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef442-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ef442-105">Cette rubrique décrit ce qui se produit pendant l’état d’inactivité de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="ef442-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ef442-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ef442-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef442-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="ef442-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ef442-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="ef442-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="ef442-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="ef442-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="ef442-110">*Aucune*</span><span class="sxs-lookup"><span data-stu-id="ef442-110">*None*</span></span>  <br/> |
|<span data-ttu-id="ef442-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="ef442-111">From this state:</span></span>  <br/> | <span data-ttu-id="ef442-112">*Non applicable*</span><span class="sxs-lookup"><span data-stu-id="ef442-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="ef442-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="ef442-113">To this state:</span></span>  <br/> |[<span data-ttu-id="ef442-114">Synchronisation de l’état</span><span class="sxs-lookup"><span data-stu-id="ef442-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="ef442-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="ef442-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ef442-116">Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="ef442-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ef442-117">Description</span><span class="sxs-lookup"><span data-stu-id="ef442-117">Description</span></span>

<span data-ttu-id="ef442-118">Rien ne se passe dans cet état.</span><span class="sxs-lookup"><span data-stu-id="ef442-118">Nothing happens in this state.</span></span> <span data-ttu-id="ef442-119">Un magasin local est dans cet état avant le début de la réplication et une fois la réplication terminée.</span><span class="sxs-lookup"><span data-stu-id="ef442-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef442-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef442-120">See also</span></span>



[<span data-ttu-id="ef442-121">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="ef442-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ef442-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ef442-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ef442-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="ef442-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ef442-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="ef442-124">SYNCSTATE</span></span>](syncstate.md)

