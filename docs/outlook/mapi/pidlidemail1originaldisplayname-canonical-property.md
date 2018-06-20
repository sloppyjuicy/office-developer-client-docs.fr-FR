---
title: Propriété canonique PidLidEmail1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7d09830f471fbaa0e8ed6ae70420dfea6428b9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785136"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="1f4d1-103">Propriété canonique PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="1f4d1-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="1f4d1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f4d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f4d1-105">Spécifie le premier nom complet qui correspond à l’adresse de messagerie qui est spécifiée pour le contact.</span><span class="sxs-lookup"><span data-stu-id="1f4d1-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f4d1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1f4d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f4d1-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="1f4d1-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="1f4d1-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="1f4d1-108">Property set:</span></span>  <br/> |<span data-ttu-id="1f4d1-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="1f4d1-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="1f4d1-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="1f4d1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1f4d1-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="1f4d1-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="1f4d1-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1f4d1-112">Data type:</span></span>  <br/> |<span data-ttu-id="1f4d1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f4d1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1f4d1-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="1f4d1-114">Area:</span></span>  <br/> |<span data-ttu-id="1f4d1-115">Contact</span><span class="sxs-lookup"><span data-stu-id="1f4d1-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f4d1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f4d1-116">Remarks</span></span>

<span data-ttu-id="1f4d1-117">Si la valeur de la propriété **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) est « SMTP », la valeur de la propriété respectifs **dispidEmail1OriginalDisplayName** doit être égal à la valeur de la **respectifs dispidEmail1EmailAddress** propriété ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f4d1-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="1f4d1-118">Cette propriété affiche une autre adresse conviviale qui est équivalente à celle de la propriété **dispidEmail1EmailAddress** .</span><span class="sxs-lookup"><span data-stu-id="1f4d1-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f4d1-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1f4d1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f4d1-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1f4d1-120">Protocol specifications</span></span>

<span data-ttu-id="1f4d1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f4d1-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f4d1-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="1f4d1-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f4d1-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f4d1-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f4d1-124">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="1f4d1-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f4d1-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1f4d1-125">Header files</span></span>

<span data-ttu-id="1f4d1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f4d1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f4d1-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1f4d1-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f4d1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f4d1-128">See also</span></span>



[<span data-ttu-id="1f4d1-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1f4d1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f4d1-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1f4d1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f4d1-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1f4d1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f4d1-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="1f4d1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

