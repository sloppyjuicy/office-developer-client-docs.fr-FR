---
title: Propriété canonique PidTagOriginalAuthorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 866c28bc08f669d18487c99c9a13bc7347b605fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425588"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="3d84f-103">Propriété canonique PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="3d84f-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3d84f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d84f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d84f-105">Contient l’identificateur d’entrée de l’auteur de la première version d’un message, c’est-à-dire le message avant d’être transmis ou de répondre.</span><span class="sxs-lookup"><span data-stu-id="3d84f-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d84f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3d84f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d84f-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3d84f-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3d84f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3d84f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d84f-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="3d84f-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="3d84f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3d84f-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d84f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3d84f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3d84f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3d84f-112">Area:</span></span>  <br/> |<span data-ttu-id="3d84f-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="3d84f-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d84f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d84f-114">Remarks</span></span>

<span data-ttu-id="3d84f-115">Cette propriété est l’une des propriétés d’adresse de l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="3d84f-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="3d84f-116">Lors de la première soumission du message, l’application cliente doit définir cette propriété sur la valeur **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3d84f-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="3d84f-117">Elle n’est jamais modifiée lorsque le message est transmis ou à qui une réponse est répondue.</span><span class="sxs-lookup"><span data-stu-id="3d84f-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="3d84f-118">La propriété d’auteur d’origine permet la conservation des informations en dehors du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="3d84f-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="3d84f-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tel qu’Internet, cette propriété permet de s’assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="3d84f-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d84f-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3d84f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3d84f-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3d84f-121">Header files</span></span>

<span data-ttu-id="3d84f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d84f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d84f-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3d84f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d84f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d84f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3d84f-125">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="3d84f-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d84f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d84f-126">See also</span></span>



[<span data-ttu-id="3d84f-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3d84f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d84f-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3d84f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d84f-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3d84f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d84f-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3d84f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

