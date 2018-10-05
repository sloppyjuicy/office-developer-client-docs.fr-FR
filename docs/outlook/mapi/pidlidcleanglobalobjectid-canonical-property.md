---
title: Propriété canonique PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400215"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="63820-103">Propriété canonique PidLidCleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="63820-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="63820-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63820-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63820-105">Spécifie nettoyage global **ObjectID**.</span><span class="sxs-lookup"><span data-stu-id="63820-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63820-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="63820-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63820-107">dispidCleanGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="63820-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="63820-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="63820-108">Property set:</span></span>  <br/> |<span data-ttu-id="63820-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="63820-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="63820-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="63820-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63820-111">0 x 00000023</span><span class="sxs-lookup"><span data-stu-id="63820-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="63820-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="63820-112">Data type:</span></span>  <br/> |<span data-ttu-id="63820-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="63820-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="63820-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="63820-114">Area:</span></span>  <br/> |<span data-ttu-id="63820-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="63820-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63820-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="63820-116">Remarks</span></span>

<span data-ttu-id="63820-117">Le format de cette propriété est la même que celle du **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63820-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="63820-118">La valeur de cette propriété doit être égale à la valeur de **LID_GLOBAL_OBJID**, à l’exception de la YH, YL M, et les champs D doivent être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="63820-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="63820-119">Tous les objets qui font référence à une Instance d’une série périodique (y compris une instance orpheline), ainsi que la série périodique lui-même, aura la même valeur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="63820-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63820-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="63820-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63820-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="63820-121">Protocol specifications</span></span>

<span data-ttu-id="63820-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63820-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63820-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="63820-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63820-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63820-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63820-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="63820-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63820-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="63820-126">Header files</span></span>

<span data-ttu-id="63820-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63820-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="63820-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="63820-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63820-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63820-129">See also</span></span>



[<span data-ttu-id="63820-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="63820-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63820-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="63820-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63820-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="63820-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63820-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="63820-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

