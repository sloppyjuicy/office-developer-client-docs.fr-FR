---
title: Propriété canonique PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361088"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="aa8f7-103">Propriété canonique PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="aa8f7-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="aa8f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa8f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa8f7-105">Contient la somme, en octets, des tailles de toutes les propriétés d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aa8f7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aa8f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aa8f7-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="aa8f7-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="aa8f7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aa8f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aa8f7-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="aa8f7-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="aa8f7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aa8f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="aa8f7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aa8f7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aa8f7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="aa8f7-112">Area:</span></span>  <br/> |<span data-ttu-id="aa8f7-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="aa8f7-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa8f7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aa8f7-114">Remarks</span></span>

<span data-ttu-id="aa8f7-115">Il est recommandé que les sous-objets des pièces jointes exposent la propriété **PR_ATTACH_SIZE** .</span><span class="sxs-lookup"><span data-stu-id="aa8f7-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="aa8f7-116">La somme contenue dans **PR_ATTACH_SIZE** inclut la taille de la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa8f7-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="aa8f7-117">Par conséquent, **PR_ATTACH_SIZE** est généralement plus volumineux que le contenu de la pièce jointe seule.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="aa8f7-118">Cette propriété peut être utilisée pour vérifier la taille approximative de la pièce jointe avant d'effectuer un transfert distant par modem et d'afficher des indicateurs de progression lors de l'enregistrement de la pièce jointe sur le disque.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="aa8f7-119">Elle est particulièrement utile avec les objets OLE attachés.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aa8f7-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="aa8f7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aa8f7-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="aa8f7-121">Protocol specifications</span></span>

<span data-ttu-id="aa8f7-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aa8f7-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aa8f7-123">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aa8f7-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="aa8f7-124">Header files</span></span>

<span data-ttu-id="aa8f7-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="aa8f7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="aa8f7-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="aa8f7-127">mapitags. h</span><span class="sxs-lookup"><span data-stu-id="aa8f7-127">mapitags.h</span></span>
  
> <span data-ttu-id="aa8f7-128">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="aa8f7-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa8f7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa8f7-129">See also</span></span>



[<span data-ttu-id="aa8f7-130">Propriété canonique PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="aa8f7-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="aa8f7-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aa8f7-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aa8f7-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aa8f7-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aa8f7-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aa8f7-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aa8f7-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="aa8f7-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

