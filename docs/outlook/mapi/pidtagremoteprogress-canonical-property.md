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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e1f57fd95ff38ef102cd74b0035dbb6b553259c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569350"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="81510-103">Propriété canonique PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="81510-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="81510-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81510-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81510-105">Cette propriété contient un nombre qui indique l’état d’un transfert à distance.</span><span class="sxs-lookup"><span data-stu-id="81510-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81510-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="81510-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81510-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="81510-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="81510-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="81510-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81510-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="81510-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="81510-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="81510-110">Data type:</span></span>  <br/> |<span data-ttu-id="81510-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="81510-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="81510-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="81510-112">Area:</span></span>  <br/> |<span data-ttu-id="81510-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="81510-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81510-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="81510-114">Remarks</span></span>

<span data-ttu-id="81510-115">Si aucun transfert n’est en cours, cette propriété doit être définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="81510-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="81510-116">Si un transfert est en cours, il doit être défini sur une valeur comprise entre 0 et 100 indiquant le pourcentage de transfert d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="81510-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="81510-117">Le texte associé au code d’état numérique s’affiche dans la propriété **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="81510-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="81510-118">Les indicateurs suivants peuvent être définis pour cette propriété :</span><span class="sxs-lookup"><span data-stu-id="81510-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="81510-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="81510-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="81510-120">Le transfert des messages est supprimé.</span><span class="sxs-lookup"><span data-stu-id="81510-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="81510-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="81510-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="81510-122">Le transfert de messages est en cours.</span><span class="sxs-lookup"><span data-stu-id="81510-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="81510-123">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="81510-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="81510-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="81510-124">Header files</span></span>

<span data-ttu-id="81510-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81510-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="81510-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="81510-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="81510-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="81510-127">Mapitags.h</span></span>
  
> <span data-ttu-id="81510-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="81510-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81510-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81510-129">See also</span></span>



[<span data-ttu-id="81510-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="81510-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81510-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="81510-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81510-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="81510-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81510-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="81510-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

