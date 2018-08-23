---
title: Propriété canonique PidTagProviderSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571611"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="575e0-103">Propriété canonique PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="575e0-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="575e0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="575e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="575e0-105">Contient la date et l’heure de qu'un fournisseur de transport transmis un message à son système de messagerie sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="575e0-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="575e0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="575e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="575e0-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="575e0-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="575e0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="575e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="575e0-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="575e0-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="575e0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="575e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="575e0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="575e0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="575e0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="575e0-112">Area:</span></span>  <br/> |<span data-ttu-id="575e0-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="575e0-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="575e0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="575e0-114">Remarks</span></span>

<span data-ttu-id="575e0-115">Cette propriété est définie par le fournisseur de transport sortant au moment où qu'un message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="575e0-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="575e0-116">Cette propriété correspond à un attribut X.400 envoi enveloppe par message.</span><span class="sxs-lookup"><span data-stu-id="575e0-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="575e0-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="575e0-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="575e0-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="575e0-118">Header files</span></span>

<span data-ttu-id="575e0-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="575e0-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="575e0-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="575e0-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="575e0-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="575e0-121">Mapitags.h</span></span>
  
> <span data-ttu-id="575e0-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="575e0-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="575e0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="575e0-123">See also</span></span>



[<span data-ttu-id="575e0-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="575e0-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="575e0-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="575e0-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="575e0-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="575e0-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="575e0-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="575e0-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

