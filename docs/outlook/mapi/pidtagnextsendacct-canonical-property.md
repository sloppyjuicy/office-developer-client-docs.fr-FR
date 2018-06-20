---
title: Propriété canonique PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 517d0900e968ea55cedf6b17b31d97795fcf61c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786261"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="7113b-103">Propriété canonique PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="7113b-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="7113b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7113b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7113b-105">Spécifie le serveur qui tente actuellement un client à utiliser pour envoyer un message électronique.</span><span class="sxs-lookup"><span data-stu-id="7113b-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7113b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7113b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7113b-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="7113b-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="7113b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7113b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7113b-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="7113b-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="7113b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7113b-110">Data type:</span></span>  <br/> |<span data-ttu-id="7113b-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7113b-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7113b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="7113b-112">Area:</span></span>  <br/> |<span data-ttu-id="7113b-113">Application Outlook</span><span class="sxs-lookup"><span data-stu-id="7113b-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7113b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7113b-114">Remarks</span></span>

<span data-ttu-id="7113b-115">Le format de cette propriété est dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="7113b-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="7113b-116">Cette propriété peut être utilisée par le client pour déterminer quel serveur pour diriger le courrier électronique à, mais est facultative et la valeur est dépourvu de signification sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7113b-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7113b-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7113b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7113b-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="7113b-118">Protocol specifications</span></span>

<span data-ttu-id="7113b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7113b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7113b-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="7113b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7113b-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7113b-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7113b-122">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="7113b-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7113b-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7113b-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7113b-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="7113b-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7113b-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7113b-125">Header files</span></span>

<span data-ttu-id="7113b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7113b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7113b-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7113b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7113b-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="7113b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7113b-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="7113b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7113b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7113b-130">See also</span></span>



[<span data-ttu-id="7113b-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7113b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7113b-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7113b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7113b-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7113b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7113b-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="7113b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

