---
title: Propriété canonique PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278892"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="a32cf-103">Propriété canonique PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="a32cf-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="a32cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a32cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a32cf-105">Contient un message qui indique l'état actuel d'une ressource de session.</span><span class="sxs-lookup"><span data-stu-id="a32cf-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a32cf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a32cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a32cf-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="a32cf-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="a32cf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a32cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a32cf-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="a32cf-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="a32cf-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a32cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="a32cf-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a32cf-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a32cf-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a32cf-112">Area:</span></span>  <br/> |<span data-ttu-id="a32cf-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="a32cf-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a32cf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a32cf-114">Remarks</span></span>

<span data-ttu-id="a32cf-115">Ces propriétés permettent aux fournisseurs de services et à l'interface MAPI de fournir des informations spécifiques sur l'état d'une ressource de session, comme le carnet d'adresses intégré ou un fournisseur de services particulier.</span><span class="sxs-lookup"><span data-stu-id="a32cf-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="a32cf-116">Cette propriété explique et fournit des informations supplémentaires sur un code d'État ou la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a32cf-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="a32cf-117">Tandis que **PR_STATUS_CODE** est requis pour tous les objets d'État, **PR_STATUS_STRING** et les propriétés associées sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="a32cf-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="a32cf-118">Lorsque le fournisseur de transport ne fournit pas de valeur, le spouleur MAPI fournit une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a32cf-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="a32cf-119">La chaîne est générée sur le même côté de l'appel de procédure distante que le spouleur MAPI; il transite par le biais de la mémoire partagée au lieu d'être marshalé dans une limite de processus.</span><span class="sxs-lookup"><span data-stu-id="a32cf-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a32cf-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a32cf-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a32cf-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a32cf-121">Header files</span></span>

<span data-ttu-id="a32cf-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a32cf-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="a32cf-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a32cf-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="a32cf-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a32cf-124">Mapitags.h</span></span>
  
> <span data-ttu-id="a32cf-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="a32cf-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a32cf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a32cf-126">See also</span></span>



[<span data-ttu-id="a32cf-127">Propriété canonique PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="a32cf-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="a32cf-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a32cf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a32cf-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a32cf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a32cf-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a32cf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a32cf-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a32cf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

