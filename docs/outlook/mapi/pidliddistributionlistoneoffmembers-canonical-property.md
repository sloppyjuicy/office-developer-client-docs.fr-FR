---
title: Propriété canonique PidLidDistributionListOneOffMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ef60c13923753eb7e349b91a5a4727958ebb73e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580235"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="0d248-103">Propriété canonique PidLidDistributionListOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="0d248-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="0d248-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d248-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d248-105">Spécifie la liste des ID d’entrée uniques qui correspondre aux membres de la liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="0d248-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d248-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0d248-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d248-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="0d248-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="0d248-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0d248-108">Property set:</span></span>  <br/> |<span data-ttu-id="0d248-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="0d248-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="0d248-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="0d248-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0d248-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="0d248-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="0d248-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0d248-112">Data type:</span></span>  <br/> |<span data-ttu-id="0d248-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="0d248-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="0d248-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0d248-114">Area:</span></span>  <br/> |<span data-ttu-id="0d248-115">Contact</span><span class="sxs-lookup"><span data-stu-id="0d248-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d248-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d248-116">Remarks</span></span>

<span data-ttu-id="0d248-117">Ces ID d’entrée uniques encapsulent les noms complets et les adresses de messagerie des membres de liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="0d248-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="0d248-118">Si le client ou le serveur de définie cette propriété, il doit être synchronisé avec la propriété **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) : pour chaque entrée dans la propriété **dispidDLOneOffMembers** , doit être une entrée dans la même position dans la propriété **dispidDLMembers** .</span><span class="sxs-lookup"><span data-stu-id="0d248-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="0d248-119">Lors de la définition de **dispidDLOneOffMembers**, le client ou le serveur doit vérifier que sa taille est inférieure à 15 000 octets.</span><span class="sxs-lookup"><span data-stu-id="0d248-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0d248-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0d248-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d248-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0d248-121">Protocol specifications</span></span>

<span data-ttu-id="0d248-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d248-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d248-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0d248-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d248-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d248-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d248-125">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="0d248-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d248-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0d248-126">Header files</span></span>

<span data-ttu-id="0d248-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d248-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d248-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0d248-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d248-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d248-129">See also</span></span>



[<span data-ttu-id="0d248-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0d248-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d248-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0d248-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d248-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0d248-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d248-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0d248-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

