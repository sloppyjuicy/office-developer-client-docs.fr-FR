---
title: Propriété canonique PidTagInternetMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3ce5de883d28d7575a8abb83ec48454752ea7ba6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580480"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="f53f7-103">Propriété canonique PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="f53f7-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="f53f7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f53f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f53f7-105">Correspond au champ ID de message tel que spécifié dans [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="f53f7-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f53f7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f53f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f53f7-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="f53f7-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="f53f7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f53f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f53f7-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="f53f7-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="f53f7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f53f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="f53f7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f53f7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f53f7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f53f7-112">Area:</span></span>  <br/> |<span data-ttu-id="f53f7-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f53f7-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f53f7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f53f7-114">Remarks</span></span>

<span data-ttu-id="f53f7-115">Ces propriétés doivent être présentes sur tous les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="f53f7-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f53f7-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f53f7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f53f7-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f53f7-117">Protocol specifications</span></span>

<span data-ttu-id="f53f7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f53f7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f53f7-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="f53f7-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f53f7-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f53f7-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f53f7-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="f53f7-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f53f7-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f53f7-122">Header files</span></span>

<span data-ttu-id="f53f7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f53f7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f53f7-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f53f7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f53f7-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f53f7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f53f7-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f53f7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f53f7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f53f7-127">See also</span></span>



[<span data-ttu-id="f53f7-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f53f7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f53f7-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f53f7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f53f7-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f53f7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f53f7-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f53f7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

