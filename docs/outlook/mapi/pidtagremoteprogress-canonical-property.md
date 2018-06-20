---
title: Propriété canonique PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4e6495d5521e0f277ac4d501a987de0142d0960d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786562"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="ecce4-103">Propriété canonique PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="ecce4-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="ecce4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecce4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecce4-105">Cette propriété contient un nombre qui indique l’état d’un transfert à distance.</span><span class="sxs-lookup"><span data-stu-id="ecce4-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecce4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ecce4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecce4-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="ecce4-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="ecce4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ecce4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecce4-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="ecce4-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="ecce4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ecce4-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecce4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ecce4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ecce4-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ecce4-112">Area:</span></span>  <br/> |<span data-ttu-id="ecce4-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="ecce4-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecce4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ecce4-114">Remarks</span></span>

<span data-ttu-id="ecce4-115">Si aucun transfert n’est en cours, cette propriété doit être définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="ecce4-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="ecce4-116">Si un transfert est en cours, il doit être défini sur une valeur comprise entre 0 et 100 indiquant le pourcentage de transfert d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="ecce4-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="ecce4-117">Le texte associé au code d’état numérique s’affiche dans la propriété **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecce4-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ecce4-118">Les indicateurs suivants peuvent être définis pour cette propriété :</span><span class="sxs-lookup"><span data-stu-id="ecce4-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="ecce4-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="ecce4-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="ecce4-120">Le transfert des messages est supprimé.</span><span class="sxs-lookup"><span data-stu-id="ecce4-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="ecce4-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ecce4-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="ecce4-122">Le transfert de messages est en cours.</span><span class="sxs-lookup"><span data-stu-id="ecce4-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="ecce4-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ecce4-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ecce4-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ecce4-124">Header files</span></span>

<span data-ttu-id="ecce4-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecce4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecce4-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ecce4-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecce4-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ecce4-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ecce4-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ecce4-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecce4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecce4-129">See also</span></span>



[<span data-ttu-id="ecce4-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ecce4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecce4-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ecce4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecce4-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ecce4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecce4-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ecce4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

