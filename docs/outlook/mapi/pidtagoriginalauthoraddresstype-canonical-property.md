---
title: Propriété canonique PidTagOriginalAuthorAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bc3c06c38f8ff8121a8503341cdd1084c036e52d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589972"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a><span data-ttu-id="1f626-103">Propriété canonique PidTagOriginalAuthorAddressType</span><span class="sxs-lookup"><span data-stu-id="1f626-103">PidTagOriginalAuthorAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="1f626-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f626-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f626-105">Contient le type d’adresse de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="1f626-105">Contains the address type of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f626-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1f626-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f626-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="1f626-107">PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="1f626-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1f626-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f626-109">0x0079</span><span class="sxs-lookup"><span data-stu-id="1f626-109">0x0079</span></span>  <br/> |
|<span data-ttu-id="1f626-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1f626-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f626-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f626-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1f626-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1f626-112">Area:</span></span>  <br/> |<span data-ttu-id="1f626-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="1f626-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f626-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f626-114">Remarks</span></span>

<span data-ttu-id="1f626-115">Ces propriétés sont des exemples de propriétés d’adresse de l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="1f626-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="1f626-116">Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de la propriété **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f626-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="1f626-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="1f626-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="1f626-118">Les propriétés de l’auteur d’origine autoriser pour la conservation des informations à partir de l’extérieur du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="1f626-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="1f626-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tels qu’à partir d’Internet, ces propriétés fournissent un moyen pour vous assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="1f626-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1f626-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1f626-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1f626-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1f626-121">Header files</span></span>

<span data-ttu-id="1f626-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f626-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f626-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1f626-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f626-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1f626-124">Mapitags.h</span></span>
  
> <span data-ttu-id="1f626-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="1f626-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f626-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f626-126">See also</span></span>



[<span data-ttu-id="1f626-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1f626-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f626-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1f626-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f626-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1f626-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f626-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1f626-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

