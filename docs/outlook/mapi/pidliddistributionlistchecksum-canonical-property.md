---
title: Propriété canonique PidLidDistributionListChecksum
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357609"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="9ea82-103">Propriété canonique PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="9ea82-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="9ea82-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ea82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ea82-105">Spécifie la somme de contrôle polynomiale de vérification de redondance cyclique (CRC-32) 32 bits pour une liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="9ea82-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ea82-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9ea82-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ea82-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="9ea82-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="9ea82-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="9ea82-108">Property set:</span></span>  <br/> |<span data-ttu-id="9ea82-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="9ea82-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="9ea82-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="9ea82-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9ea82-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="9ea82-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="9ea82-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9ea82-112">Data type:</span></span>  <br/> |<span data-ttu-id="9ea82-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9ea82-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9ea82-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9ea82-114">Area:</span></span>  <br/> |<span data-ttu-id="9ea82-115">Contact</span><span class="sxs-lookup"><span data-stu-id="9ea82-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ea82-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ea82-116">Remarks</span></span>

<span data-ttu-id="9ea82-117">La valeur de cette propriété peut être utilisée pour détecter la date de mise à jour de la propriété **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) sans mettre à jour les autres propriétés de membre de liste de distribution personnelle en calculant le CRC-32 sur le valeur de **dispidDLMembers** et en la comparant avec la valeur de la propriété **dispidDLChecksum** .</span><span class="sxs-lookup"><span data-stu-id="9ea82-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9ea82-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="9ea82-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ea82-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9ea82-119">Protocol specifications</span></span>

<span data-ttu-id="9ea82-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ea82-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ea82-121">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="9ea82-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ea82-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ea82-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ea82-123">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="9ea82-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ea82-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="9ea82-124">Header files</span></span>

<span data-ttu-id="9ea82-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ea82-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ea82-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9ea82-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ea82-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ea82-127">See also</span></span>



[<span data-ttu-id="9ea82-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea82-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ea82-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea82-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ea82-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea82-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ea82-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9ea82-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

