---
title: Propriété canonique PidLidHasPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357749"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="865c5-103">Propriété canonique PidLidHasPicture</span><span class="sxs-lookup"><span data-stu-id="865c5-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="865c5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="865c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="865c5-105">Spécifie s’il existe une pièce jointe pour un contact.</span><span class="sxs-lookup"><span data-stu-id="865c5-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="865c5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="865c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="865c5-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="865c5-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="865c5-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="865c5-108">Property set:</span></span>  <br/> |<span data-ttu-id="865c5-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="865c5-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="865c5-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="865c5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="865c5-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="865c5-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="865c5-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="865c5-112">Data type:</span></span>  <br/> |<span data-ttu-id="865c5-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="865c5-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="865c5-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="865c5-114">Area:</span></span>  <br/> |<span data-ttu-id="865c5-115">Contact</span><span class="sxs-lookup"><span data-stu-id="865c5-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="865c5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="865c5-116">Remarks</span></span>

<span data-ttu-id="865c5-117">Si cette propriété existe et est définie sur TRUE, la table des pièces jointes du contact contient une pièce jointe avec la propriété **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="865c5-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="865c5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="865c5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="865c5-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="865c5-119">Protocol specifications</span></span>

<span data-ttu-id="865c5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="865c5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="865c5-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="865c5-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="865c5-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="865c5-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="865c5-123">Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="865c5-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="865c5-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="865c5-124">Header files</span></span>

<span data-ttu-id="865c5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="865c5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="865c5-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="865c5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="865c5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="865c5-127">See also</span></span>



[<span data-ttu-id="865c5-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="865c5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="865c5-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="865c5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="865c5-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="865c5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="865c5-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="865c5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

