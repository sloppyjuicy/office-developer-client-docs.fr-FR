---
title: Propriété canonique PidLidCommonEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fc3849ac972ce7e3efbfa981ff950ee3615cb533
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571464"
---
# <a name="pidlidcommonend-canonical-property"></a><span data-ttu-id="56143-103">Propriété canonique PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="56143-103">PidLidCommonEnd Canonical Property</span></span>

  
  
<span data-ttu-id="56143-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56143-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56143-105">Représente la date de fin et l’heure d’un message.</span><span class="sxs-lookup"><span data-stu-id="56143-105">Represents the end date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56143-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="56143-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56143-107">dispidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="56143-107">dispidCommonEnd</span></span>  <br/> |
|<span data-ttu-id="56143-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="56143-108">Property set:</span></span>  <br/> |<span data-ttu-id="56143-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="56143-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="56143-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="56143-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="56143-111">0x00008517</span><span class="sxs-lookup"><span data-stu-id="56143-111">0x00008517</span></span>  <br/> |
|<span data-ttu-id="56143-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="56143-112">Data type:</span></span>  <br/> |<span data-ttu-id="56143-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="56143-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="56143-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="56143-114">Area:</span></span>  <br/> |<span data-ttu-id="56143-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="56143-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56143-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="56143-116">Remarks</span></span>

<span data-ttu-id="56143-117">Cette propriété indique l’heure de fin d’un élément.</span><span class="sxs-lookup"><span data-stu-id="56143-117">This property indicates the end time for an item.</span></span> <span data-ttu-id="56143-118">Il doit être supérieure ou égale à la valeur de la propriété **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56143-118">It must be greater than or equal to the value of the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="56143-119">Cette valeur doit être l’équivalent temps universel coordonné (UTC) de la propriété **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56143-119">This value must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="56143-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="56143-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56143-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="56143-121">Protocol specifications</span></span>

<span data-ttu-id="56143-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56143-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56143-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="56143-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56143-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56143-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56143-125">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="56143-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="56143-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56143-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56143-127">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="56143-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56143-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="56143-128">Header files</span></span>

<span data-ttu-id="56143-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56143-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="56143-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="56143-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56143-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56143-131">See also</span></span>



[<span data-ttu-id="56143-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="56143-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56143-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="56143-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56143-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="56143-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56143-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="56143-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

