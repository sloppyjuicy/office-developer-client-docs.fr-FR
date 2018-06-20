---
title: Propriété canonique PidTagOriginalSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEmailAddress
api_type:
- COM
ms.assetid: cc86505c-e264-435f-ae21-4a10f0bbf082
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 02a057d6382394c947fa1f23c4408ff0ad2339de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786336"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="eb1f8-103">Propriété canonique PidTagOriginalSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="eb1f8-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="eb1f8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb1f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb1f8-105">Contient l’adresse de messagerie de l’expéditeur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="eb1f8-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb1f8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="eb1f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb1f8-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="eb1f8-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="eb1f8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="eb1f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb1f8-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="eb1f8-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="eb1f8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="eb1f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb1f8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb1f8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="eb1f8-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="eb1f8-112">Area:</span></span>  <br/> |<span data-ttu-id="eb1f8-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="eb1f8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb1f8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb1f8-114">Remarks</span></span>

<span data-ttu-id="eb1f8-115">Ces propriétés sont des exemples de propriétés d’adresse de l’expéditeur d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="eb1f8-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="eb1f8-116">Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eb1f8-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="eb1f8-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="eb1f8-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eb1f8-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="eb1f8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb1f8-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="eb1f8-119">Protocol specifications</span></span>

<span data-ttu-id="eb1f8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb1f8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb1f8-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="eb1f8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb1f8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb1f8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb1f8-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="eb1f8-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb1f8-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="eb1f8-124">Header files</span></span>

<span data-ttu-id="eb1f8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb1f8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb1f8-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="eb1f8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb1f8-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="eb1f8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="eb1f8-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="eb1f8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb1f8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb1f8-129">See also</span></span>



[<span data-ttu-id="eb1f8-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="eb1f8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb1f8-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="eb1f8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb1f8-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="eb1f8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb1f8-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="eb1f8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

