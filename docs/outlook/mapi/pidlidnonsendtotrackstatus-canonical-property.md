---
title: Propriété canonique PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cf9d11b7a53ee0b9911e32cb3c3e2a0a490e4729
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592786"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="ffce1-103">Propriété canonique PidLidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="ffce1-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="ffce1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffce1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffce1-105">Contient la valeur de chaque participant répertoriés dans la propriété **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ffce1-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffce1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ffce1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffce1-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="ffce1-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="ffce1-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="ffce1-108">Property set:</span></span>  <br/> |<span data-ttu-id="ffce1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ffce1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ffce1-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="ffce1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ffce1-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="ffce1-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="ffce1-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ffce1-112">Data type:</span></span>  <br/> |<span data-ttu-id="ffce1-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="ffce1-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="ffce1-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ffce1-114">Area:</span></span>  <br/> |<span data-ttu-id="ffce1-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="ffce1-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffce1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffce1-116">Remarks</span></span>

<span data-ttu-id="ffce1-117">Cette propriété est requise uniquement lorsque la valeur de la propriété **dispidNonSendableTo** .</span><span class="sxs-lookup"><span data-stu-id="ffce1-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="ffce1-118">Le nombre de valeurs dans cette propriété doit correspondre au nombre de valeurs dans **dispidNonSendableTo**.</span><span class="sxs-lookup"><span data-stu-id="ffce1-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="ffce1-119">Chaque valeur PT_LONG dans cette propriété correspond au participant de la propriété **dispidNonSendableTo** dans le même index.</span><span class="sxs-lookup"><span data-stu-id="ffce1-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ffce1-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ffce1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffce1-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ffce1-121">Protocol specifications</span></span>

<span data-ttu-id="ffce1-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffce1-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffce1-123">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="ffce1-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffce1-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffce1-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffce1-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="ffce1-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffce1-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ffce1-126">Header files</span></span>

<span data-ttu-id="ffce1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffce1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffce1-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ffce1-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffce1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffce1-129">See also</span></span>



[<span data-ttu-id="ffce1-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ffce1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffce1-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ffce1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffce1-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ffce1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffce1-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ffce1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

