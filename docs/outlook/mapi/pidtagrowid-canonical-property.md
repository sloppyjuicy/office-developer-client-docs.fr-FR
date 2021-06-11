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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8d58342e0460352bd9d260cb6e73de358cb2fc23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359534"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="32ddc-103">Propriété canonique PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="32ddc-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="32ddc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32ddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32ddc-105">Contient un identificateur unique pour un destinataire dans une table de destinataires ou une table d’état.</span><span class="sxs-lookup"><span data-stu-id="32ddc-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32ddc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="32ddc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32ddc-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="32ddc-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="32ddc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="32ddc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="32ddc-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="32ddc-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="32ddc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="32ddc-110">Data type:</span></span>  <br/> |<span data-ttu-id="32ddc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="32ddc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="32ddc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="32ddc-112">Area:</span></span>  <br/> |<span data-ttu-id="32ddc-113">MAPI courant</span><span class="sxs-lookup"><span data-stu-id="32ddc-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32ddc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="32ddc-114">Remarks</span></span>

<span data-ttu-id="32ddc-115">Cette propriété est une valeur temporaire qui n’est valide que pour la durée de vie de l’objet propriétaire de la table.</span><span class="sxs-lookup"><span data-stu-id="32ddc-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="32ddc-116">Il apparaît en tant que colonne de la table, mais n’est pas stocké.</span><span class="sxs-lookup"><span data-stu-id="32ddc-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="32ddc-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="32ddc-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32ddc-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="32ddc-118">Protocol specifications</span></span>

<span data-ttu-id="32ddc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32ddc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32ddc-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="32ddc-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32ddc-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32ddc-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32ddc-122">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="32ddc-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32ddc-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="32ddc-123">Header files</span></span>

<span data-ttu-id="32ddc-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32ddc-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="32ddc-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="32ddc-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="32ddc-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="32ddc-126">Mapitags.h</span></span>
  
> <span data-ttu-id="32ddc-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="32ddc-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32ddc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32ddc-128">See also</span></span>



[<span data-ttu-id="32ddc-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="32ddc-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="32ddc-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="32ddc-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="32ddc-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="32ddc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32ddc-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="32ddc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32ddc-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="32ddc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32ddc-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="32ddc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

