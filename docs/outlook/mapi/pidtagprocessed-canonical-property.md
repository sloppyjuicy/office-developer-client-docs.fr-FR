---
title: Propriété canonique PidTagProcessed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5d84e9cb693cbe732295ee1891b4219450eb09ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351435"
---
# <a name="pidtagprocessed-canonical-property"></a><span data-ttu-id="4f6ae-103">Propriété canonique PidTagProcessed</span><span class="sxs-lookup"><span data-stu-id="4f6ae-103">PidTagProcessed Canonical Property</span></span>

  
  
<span data-ttu-id="4f6ae-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f6ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f6ae-105">Valeur TRUE lorsque la demande de réunion a été traitée.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-105">Set to TRUE when the meeting request has been processed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f6ae-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4f6ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f6ae-107">PR_PROCESSED</span><span class="sxs-lookup"><span data-stu-id="4f6ae-107">PR_PROCESSED</span></span>  <br/> |
|<span data-ttu-id="4f6ae-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4f6ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f6ae-109">0x7D01</span><span class="sxs-lookup"><span data-stu-id="4f6ae-109">0x7D01</span></span>  <br/> |
|<span data-ttu-id="4f6ae-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4f6ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f6ae-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4f6ae-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4f6ae-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4f6ae-112">Area:</span></span>  <br/> |<span data-ttu-id="4f6ae-113">Calendrier</span><span class="sxs-lookup"><span data-stu-id="4f6ae-113">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f6ae-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4f6ae-114">Remarks</span></span>

<span data-ttu-id="4f6ae-115">Cette propriété permet de s'assurer que les demandes de réunion sont traitées une seule fois.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-115">This property ensures that meeting requests get processed once.</span></span> <span data-ttu-id="4f6ae-116">Le créateur de la demande doit définir cette propriété sur FALSe et le destinataire doit lui affecter la valeur TRUE une fois la demande dans le calendrier.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-116">The creator of the request should set this property to FALSE and the receiver should set it to TRUE once the request is in the calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4f6ae-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="4f6ae-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4f6ae-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="4f6ae-118">Protocol specifications</span></span>

<span data-ttu-id="4f6ae-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f6ae-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f6ae-120">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4f6ae-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f6ae-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f6ae-122">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="4f6ae-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f6ae-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4f6ae-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de liste de distribution personnelle et de contact.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-124">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4f6ae-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="4f6ae-125">Header files</span></span>

<span data-ttu-id="4f6ae-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4f6ae-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f6ae-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f6ae-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4f6ae-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4f6ae-129">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="4f6ae-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f6ae-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f6ae-130">See also</span></span>



[<span data-ttu-id="4f6ae-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4f6ae-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f6ae-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4f6ae-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f6ae-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4f6ae-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f6ae-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4f6ae-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

