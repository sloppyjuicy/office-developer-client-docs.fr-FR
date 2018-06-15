---
title: État inactif
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783663"
---
# <a name="idle-state"></a><span data-ttu-id="09e6e-103">État inactif</span><span class="sxs-lookup"><span data-stu-id="09e6e-103">Idle State</span></span>

  
  
<span data-ttu-id="09e6e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09e6e-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="09e6e-105">Cette rubrique décrit le déroulement de l’état d’inactivité de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="09e6e-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="09e6e-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="09e6e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09e6e-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="09e6e-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="09e6e-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="09e6e-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="09e6e-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="09e6e-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="09e6e-110">*None*</span><span class="sxs-lookup"><span data-stu-id="09e6e-110">*None*</span></span>  <br/> |
|<span data-ttu-id="09e6e-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="09e6e-111">From this state:</span></span>  <br/> | <span data-ttu-id="09e6e-112">*Non applicable*</span><span class="sxs-lookup"><span data-stu-id="09e6e-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="09e6e-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="09e6e-113">To this state:</span></span>  <br/> |[<span data-ttu-id="09e6e-114">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="09e6e-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="09e6e-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="09e6e-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="09e6e-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="09e6e-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="09e6e-117">Description</span><span class="sxs-lookup"><span data-stu-id="09e6e-117">Description</span></span>

<span data-ttu-id="09e6e-118">Rien ne se passe dans cet état.</span><span class="sxs-lookup"><span data-stu-id="09e6e-118">Nothing happens in this state.</span></span> <span data-ttu-id="09e6e-119">Un magasin local est dans cet état avant la réplication et une fois que la réplication est terminée.</span><span class="sxs-lookup"><span data-stu-id="09e6e-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09e6e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09e6e-120">See also</span></span>



[<span data-ttu-id="09e6e-121">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="09e6e-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="09e6e-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="09e6e-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="09e6e-123">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="09e6e-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="09e6e-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="09e6e-124">SYNCSTATE</span></span>](syncstate.md)

