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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399745"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="2c578-103">Propriété canonique PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="2c578-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="2c578-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c578-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c578-105">Contient les fonctions sum, en octets, des tailles de toutes les propriétés sur une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2c578-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c578-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2c578-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c578-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="2c578-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="2c578-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2c578-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c578-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="2c578-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="2c578-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2c578-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c578-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2c578-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2c578-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2c578-112">Area:</span></span>  <br/> |<span data-ttu-id="2c578-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="2c578-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c578-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2c578-114">Remarks</span></span>

<span data-ttu-id="2c578-115">Il est recommandé que les pièces jointes sous-objets exposent la propriété **PR_ATTACH_SIZE** .</span><span class="sxs-lookup"><span data-stu-id="2c578-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="2c578-116">La somme contenue dans **PR_ATTACH_SIZE** inclut la taille de la **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c578-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="2c578-117">En conséquence, **PR_ATTACH_SIZE** est généralement plus volumineux que le contenu de la pièce jointe uniquement.</span><span class="sxs-lookup"><span data-stu-id="2c578-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="2c578-118">Cette propriété peut être utilisée pour vérifier la taille approximative de la pièce jointe avant d’effectuer un transfert à distance par modem et pour afficher les indicateurs de progression lors de l’enregistrement de la pièce jointe sur le disque.</span><span class="sxs-lookup"><span data-stu-id="2c578-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="2c578-119">Il est particulièrement utile avec les objets OLE attachés.</span><span class="sxs-lookup"><span data-stu-id="2c578-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2c578-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2c578-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c578-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="2c578-121">Protocol specifications</span></span>

<span data-ttu-id="2c578-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c578-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c578-123">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2c578-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c578-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2c578-124">Header files</span></span>

<span data-ttu-id="2c578-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c578-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c578-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2c578-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c578-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="2c578-127">mapitags.h</span></span>
  
> <span data-ttu-id="2c578-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="2c578-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c578-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c578-129">See also</span></span>



[<span data-ttu-id="2c578-130">Propriété canonique PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="2c578-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="2c578-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2c578-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c578-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2c578-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c578-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2c578-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c578-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2c578-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

