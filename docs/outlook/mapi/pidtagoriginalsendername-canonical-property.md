---
title: Propriété canonique PidTagOriginalSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 521fb544152dcb903450ff7dbd05ecbac808afe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342608"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="8b672-103">Propriété canonique PidTagOriginalSenderName</span><span class="sxs-lookup"><span data-stu-id="8b672-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="8b672-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b672-105">Contient le nom complet de l'expéditeur de la première version d'un message, c'est-à-dire le message avant son transfert ou sa réponse.</span><span class="sxs-lookup"><span data-stu-id="8b672-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b672-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8b672-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b672-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8b672-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8b672-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8b672-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b672-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="8b672-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="8b672-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8b672-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b672-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8b672-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8b672-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8b672-112">Area:</span></span>  <br/> |<span data-ttu-id="8b672-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="8b672-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b672-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b672-114">Remarks</span></span>

<span data-ttu-id="8b672-115">Ces propriétés sont des exemples de propriétés d'adresse pour l'expéditeur d'origine d'un message.</span><span class="sxs-lookup"><span data-stu-id="8b672-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="8b672-116">Lors de la première soumission du message, une application cliente doit définir ces propriétés sur la valeur de la propriété **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8b672-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="8b672-117">Il n'est jamais modifié lorsque le message est transféré ou renvoyé.</span><span class="sxs-lookup"><span data-stu-id="8b672-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b672-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="8b672-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b672-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8b672-119">Protocol specifications</span></span>

<span data-ttu-id="8b672-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b672-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b672-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="8b672-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b672-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b672-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b672-123">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="8b672-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b672-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="8b672-124">Header files</span></span>

<span data-ttu-id="8b672-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8b672-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b672-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8b672-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b672-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8b672-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8b672-128">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="8b672-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b672-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b672-129">See also</span></span>



[<span data-ttu-id="8b672-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8b672-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b672-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8b672-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b672-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8b672-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b672-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8b672-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

