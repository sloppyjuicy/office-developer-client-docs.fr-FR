---
title: Propriété canonique PidLidEmail3OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ac90910e143d05c17b73aa6a1062cd0999b0d3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785152"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="89e37-103">Propriété canonique PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="89e37-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="89e37-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89e37-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89e37-105">Spécifie le nom complet tiers qui correspond à l’adresse de messagerie qui est spécifiée pour le contact.</span><span class="sxs-lookup"><span data-stu-id="89e37-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89e37-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="89e37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89e37-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="89e37-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="89e37-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="89e37-108">Property set:</span></span>  <br/> |<span data-ttu-id="89e37-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="89e37-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="89e37-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="89e37-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="89e37-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="89e37-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="89e37-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="89e37-112">Data type:</span></span>  <br/> |<span data-ttu-id="89e37-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89e37-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="89e37-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="89e37-114">Area:</span></span>  <br/> |<span data-ttu-id="89e37-115">Contact</span><span class="sxs-lookup"><span data-stu-id="89e37-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89e37-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="89e37-116">Remarks</span></span>

<span data-ttu-id="89e37-117">Si la valeur de la propriété **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) est « SMTP », la valeur de la propriété respectifs **dispidEmail3OriginalDisplayName** doit être égal à la valeur de la **respectifs dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89e37-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="89e37-118">L’objectif de cette propriété consiste à afficher une autre adresse conviviale qui est équivalente à celle de la **dispidEmail3EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="89e37-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="89e37-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="89e37-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="89e37-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="89e37-120">Protocol specifications</span></span>

<span data-ttu-id="89e37-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89e37-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89e37-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="89e37-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="89e37-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89e37-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89e37-124">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="89e37-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="89e37-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="89e37-125">Header files</span></span>

<span data-ttu-id="89e37-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89e37-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="89e37-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="89e37-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89e37-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89e37-128">See also</span></span>



[<span data-ttu-id="89e37-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="89e37-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89e37-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="89e37-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89e37-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="89e37-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89e37-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="89e37-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

