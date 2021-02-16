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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ed3d84667d7be9c06d0ddf4d896b8888694edc12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355271"
---
# <a name="pidtagoriginalsenderemailaddress-canonical-property"></a><span data-ttu-id="8a9bf-103">Propriété canonique PidTagOriginalSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8a9bf-103">PidTagOriginalSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="8a9bf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a9bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a9bf-105">Contient l’adresse e-mail de l’expéditeur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou d’y répondre.</span><span class="sxs-lookup"><span data-stu-id="8a9bf-105">Contains the email address of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a9bf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8a9bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a9bf-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="8a9bf-107">PR_ORIGINAL_SENDER_EMAIL_ADDRESS, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_A, PR_ORIGINAL_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="8a9bf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8a9bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a9bf-109">0x0067</span><span class="sxs-lookup"><span data-stu-id="8a9bf-109">0x0067</span></span>  <br/> |
|<span data-ttu-id="8a9bf-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8a9bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a9bf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8a9bf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8a9bf-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8a9bf-112">Area:</span></span>  <br/> |<span data-ttu-id="8a9bf-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="8a9bf-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a9bf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a9bf-114">Remarks</span></span>

<span data-ttu-id="8a9bf-115">Ces propriétés sont des exemples des propriétés d’adresse de l’expéditeur d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="8a9bf-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="8a9bf-116">Lors de la première soumission du message, l’application cliente doit définir cette propriété sur la valeur **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8a9bf-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="8a9bf-117">Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue.</span><span class="sxs-lookup"><span data-stu-id="8a9bf-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a9bf-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8a9bf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a9bf-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8a9bf-119">Protocol specifications</span></span>

<span data-ttu-id="8a9bf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a9bf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a9bf-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="8a9bf-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a9bf-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a9bf-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a9bf-123">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="8a9bf-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a9bf-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8a9bf-124">Header files</span></span>

<span data-ttu-id="8a9bf-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a9bf-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a9bf-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8a9bf-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a9bf-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a9bf-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8a9bf-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="8a9bf-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a9bf-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a9bf-129">See also</span></span>



[<span data-ttu-id="8a9bf-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8a9bf-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a9bf-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8a9bf-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a9bf-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8a9bf-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a9bf-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8a9bf-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

