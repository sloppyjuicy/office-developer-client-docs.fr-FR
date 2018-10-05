---
title: Propriété canonique PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397771"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="02c84-103">Propriété canonique PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="02c84-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="02c84-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02c84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02c84-105">Spécifie le nom complet deuxième qui correspond à l’adresse de messagerie spécifiée pour le contact.</span><span class="sxs-lookup"><span data-stu-id="02c84-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02c84-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="02c84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02c84-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="02c84-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="02c84-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="02c84-108">Property set:</span></span>  <br/> |<span data-ttu-id="02c84-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="02c84-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="02c84-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="02c84-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="02c84-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="02c84-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="02c84-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="02c84-112">Data type:</span></span>  <br/> |<span data-ttu-id="02c84-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="02c84-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="02c84-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="02c84-114">Area:</span></span>  <br/> |<span data-ttu-id="02c84-115">Contact</span><span class="sxs-lookup"><span data-stu-id="02c84-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02c84-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="02c84-116">Remarks</span></span>

<span data-ttu-id="02c84-117">Si la valeur de la propriété **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) est « SMTP », la valeur de la propriété **PidLidEmail2OriginalDisplayName** respective doit être égal à la valeur de la **respectifs dispidEmail2EmailAddress** propriété ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="02c84-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="02c84-118">L’objectif de cette propriété consiste à afficher une autre adresse conviviale qui est équivalente à celle de la **dispidEmail2EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="02c84-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="02c84-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="02c84-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02c84-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="02c84-120">Protocol specifications</span></span>

<span data-ttu-id="02c84-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02c84-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02c84-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="02c84-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02c84-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02c84-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02c84-124">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="02c84-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02c84-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="02c84-125">Header files</span></span>

<span data-ttu-id="02c84-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02c84-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="02c84-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="02c84-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02c84-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02c84-128">See also</span></span>



[<span data-ttu-id="02c84-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="02c84-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02c84-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="02c84-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02c84-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="02c84-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02c84-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="02c84-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

