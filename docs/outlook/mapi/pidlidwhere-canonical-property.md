---
title: Propriété canonique PidLidWhere
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 19c3ed57d2a0bdd6902a93ca5f29deb91418b8ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360430"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="23d19-103">Propriété canonique PidLidWhere</span><span class="sxs-lookup"><span data-stu-id="23d19-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="23d19-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23d19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23d19-105">Spécifie l’emplacement d’un événement.</span><span class="sxs-lookup"><span data-stu-id="23d19-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23d19-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="23d19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23d19-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="23d19-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="23d19-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="23d19-108">Property set:</span></span>  <br/> |<span data-ttu-id="23d19-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="23d19-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="23d19-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="23d19-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="23d19-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="23d19-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="23d19-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="23d19-112">Data type:</span></span>  <br/> |<span data-ttu-id="23d19-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="23d19-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="23d19-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="23d19-114">Area:</span></span>  <br/> |<span data-ttu-id="23d19-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="23d19-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23d19-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="23d19-116">Remarks</span></span>

<span data-ttu-id="23d19-117">La valeur de cette propriété doit être identique à la valeur de la propriété **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) de la réunion associée.</span><span class="sxs-lookup"><span data-stu-id="23d19-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="23d19-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="23d19-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23d19-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="23d19-119">Protocol specifications</span></span>

<span data-ttu-id="23d19-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23d19-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23d19-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="23d19-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23d19-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23d19-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23d19-123">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="23d19-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23d19-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="23d19-124">Header files</span></span>

<span data-ttu-id="23d19-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23d19-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="23d19-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="23d19-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23d19-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23d19-127">See also</span></span>



[<span data-ttu-id="23d19-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="23d19-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23d19-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="23d19-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23d19-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="23d19-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23d19-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="23d19-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

