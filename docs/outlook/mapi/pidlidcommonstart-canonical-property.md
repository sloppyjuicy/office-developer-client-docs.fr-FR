---
title: Propriété canonique PidLidCommonStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCommonStart
api_type:
- COM
ms.assetid: d999852d-ce98-4c3c-a772-87f5db4aa04e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ec7c213d7eec9ab0ef5766442e3de59a24811d37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345485"
---
# <a name="pidlidcommonstart-canonical-property"></a><span data-ttu-id="27fba-103">Propriété canonique PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="27fba-103">PidLidCommonStart Canonical Property</span></span>

  
  
<span data-ttu-id="27fba-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27fba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27fba-105">Représente la date et l'heure de début d'un message.</span><span class="sxs-lookup"><span data-stu-id="27fba-105">Represents the start date and time of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27fba-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="27fba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27fba-107">dispidCommonStart</span><span class="sxs-lookup"><span data-stu-id="27fba-107">dispidCommonStart</span></span>  <br/> |
|<span data-ttu-id="27fba-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="27fba-108">Property set:</span></span>  <br/> |<span data-ttu-id="27fba-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="27fba-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="27fba-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="27fba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="27fba-111">0x00008516</span><span class="sxs-lookup"><span data-stu-id="27fba-111">0x00008516</span></span>  <br/> |
|<span data-ttu-id="27fba-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="27fba-112">Data type:</span></span>  <br/> |<span data-ttu-id="27fba-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="27fba-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="27fba-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="27fba-114">Area:</span></span>  <br/> |<span data-ttu-id="27fba-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="27fba-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27fba-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="27fba-116">Remarks</span></span>

<span data-ttu-id="27fba-117">Cette propriété indique l'heure de début d'un élément.</span><span class="sxs-lookup"><span data-stu-id="27fba-117">This property indicates the start time for an item.</span></span> <span data-ttu-id="27fba-118">Il doit être inférieur ou égal à la valeur de la propriété **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="27fba-118">It must be less than or equal to the value of the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="27fba-119">La valeur de cette propriété doit être l'équivalent du temps universel coordonné (UTC) de la propriété **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="27fba-119">The value of this property must be the Coordinated Universal Time (UTC) equivalent of the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27fba-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="27fba-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27fba-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="27fba-121">Protocol specifications</span></span>

<span data-ttu-id="27fba-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27fba-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27fba-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="27fba-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27fba-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27fba-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27fba-125">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="27fba-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="27fba-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27fba-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27fba-127">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="27fba-127">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27fba-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="27fba-128">Header files</span></span>

<span data-ttu-id="27fba-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="27fba-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="27fba-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="27fba-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27fba-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27fba-131">See also</span></span>



[<span data-ttu-id="27fba-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="27fba-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27fba-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="27fba-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27fba-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="27fba-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27fba-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="27fba-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

