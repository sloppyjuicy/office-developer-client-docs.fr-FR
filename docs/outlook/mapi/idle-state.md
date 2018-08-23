---
title: État inactif
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591799"
---
# <a name="idle-state"></a><span data-ttu-id="a6297-103">État inactif</span><span class="sxs-lookup"><span data-stu-id="a6297-103">Idle State</span></span>

  
  
<span data-ttu-id="a6297-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6297-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a6297-105">Cette rubrique décrit le déroulement de l’état d’inactivité de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="a6297-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a6297-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a6297-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6297-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="a6297-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a6297-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="a6297-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="a6297-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="a6297-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="a6297-110">*None*</span><span class="sxs-lookup"><span data-stu-id="a6297-110">*None*</span></span>  <br/> |
|<span data-ttu-id="a6297-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="a6297-111">From this state:</span></span>  <br/> | <span data-ttu-id="a6297-112">*Non applicable*</span><span class="sxs-lookup"><span data-stu-id="a6297-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="a6297-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="a6297-113">To this state:</span></span>  <br/> |[<span data-ttu-id="a6297-114">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="a6297-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="a6297-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="a6297-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a6297-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="a6297-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a6297-117">Description</span><span class="sxs-lookup"><span data-stu-id="a6297-117">Description</span></span>

<span data-ttu-id="a6297-118">Rien ne se passe dans cet état.</span><span class="sxs-lookup"><span data-stu-id="a6297-118">Nothing happens in this state.</span></span> <span data-ttu-id="a6297-119">Un magasin local est dans cet état avant la réplication et une fois que la réplication est terminée.</span><span class="sxs-lookup"><span data-stu-id="a6297-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6297-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6297-120">See also</span></span>



[<span data-ttu-id="a6297-121">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="a6297-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a6297-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a6297-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a6297-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="a6297-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a6297-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a6297-124">SYNCSTATE</span></span>](syncstate.md)

