---
title: Propriété canonique PidTagOriginalSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385731"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="9bd23-103">Propriété canonique PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="9bd23-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="9bd23-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bd23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bd23-105">Contient la date de soumission d’origine et l’heure du message dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="9bd23-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bd23-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9bd23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bd23-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="9bd23-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="9bd23-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9bd23-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bd23-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="9bd23-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="9bd23-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9bd23-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bd23-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9bd23-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9bd23-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9bd23-112">Area:</span></span>  <br/> |<span data-ttu-id="9bd23-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="9bd23-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bd23-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9bd23-114">Remarks</span></span>

<span data-ttu-id="9bd23-115">Au premier envoi d’un message, une application cliente doit définir cette propriété à la valeur de la propriété **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9bd23-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="9bd23-116">Il n’est pas modifié lorsque le message est transféré.</span><span class="sxs-lookup"><span data-stu-id="9bd23-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="9bd23-117">Il est utilisé dans les rapports uniquement.</span><span class="sxs-lookup"><span data-stu-id="9bd23-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9bd23-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9bd23-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bd23-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9bd23-119">Protocol specifications</span></span>

<span data-ttu-id="9bd23-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bd23-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bd23-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="9bd23-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bd23-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bd23-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bd23-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="9bd23-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bd23-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9bd23-124">Header files</span></span>

<span data-ttu-id="9bd23-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bd23-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bd23-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9bd23-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bd23-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9bd23-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9bd23-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9bd23-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bd23-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bd23-129">See also</span></span>



[<span data-ttu-id="9bd23-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9bd23-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bd23-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9bd23-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bd23-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9bd23-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bd23-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9bd23-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

