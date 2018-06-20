---
title: Propriété canonique PidTagRowid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e8d0e79e01040c1cc3d46e73a7e6a456a915a67f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786609"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="08940-103">Propriété canonique PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="08940-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="08940-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08940-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08940-105">Contient un identificateur unique pour un destinataire d’une table de destinataire ou de la table d’état.</span><span class="sxs-lookup"><span data-stu-id="08940-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08940-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="08940-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08940-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="08940-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="08940-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="08940-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08940-109">0 x 3000</span><span class="sxs-lookup"><span data-stu-id="08940-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="08940-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="08940-110">Data type:</span></span>  <br/> |<span data-ttu-id="08940-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="08940-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="08940-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="08940-112">Area:</span></span>  <br/> |<span data-ttu-id="08940-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="08940-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08940-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="08940-114">Remarks</span></span>

<span data-ttu-id="08940-115">Cette propriété est une valeur temporaire est valide uniquement pour la durée de vie de l’objet auquel appartient la table.</span><span class="sxs-lookup"><span data-stu-id="08940-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="08940-116">Il s’affiche en tant que colonne de la table, mais n’est pas stocké.</span><span class="sxs-lookup"><span data-stu-id="08940-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08940-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="08940-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08940-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="08940-118">Protocol specifications</span></span>

<span data-ttu-id="08940-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08940-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08940-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="08940-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08940-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08940-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08940-122">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="08940-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08940-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="08940-123">Header files</span></span>

<span data-ttu-id="08940-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08940-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="08940-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="08940-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="08940-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="08940-126">Mapitags.h</span></span>
  
> <span data-ttu-id="08940-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="08940-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08940-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08940-128">See also</span></span>



[<span data-ttu-id="08940-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="08940-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="08940-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="08940-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="08940-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="08940-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08940-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="08940-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08940-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="08940-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08940-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="08940-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

