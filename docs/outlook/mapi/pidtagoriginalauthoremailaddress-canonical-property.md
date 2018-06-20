---
title: Propriété canonique PidTagOriginalAuthorEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1954e1760fead9cbe13f0f2394f8095cab7f26ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786304"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="f50d0-103">Propriété canonique PidTagOriginalAuthorEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f50d0-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="f50d0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f50d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f50d0-105">Contient l’adresse de messagerie de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="f50d0-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f50d0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f50d0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f50d0-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="f50d0-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="f50d0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f50d0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f50d0-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="f50d0-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="f50d0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f50d0-110">Data type:</span></span>  <br/> |<span data-ttu-id="f50d0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f50d0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f50d0-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="f50d0-112">Area:</span></span>  <br/> |<span data-ttu-id="f50d0-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="f50d0-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f50d0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f50d0-114">Remarks</span></span>

<span data-ttu-id="f50d0-115">Ces propriétés sont des exemples de propriétés d’adresse de l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="f50d0-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="f50d0-116">Au premier envoi du message, l’application cliente doit définir ces propriétés à la valeur de la propriété **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f50d0-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="f50d0-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="f50d0-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="f50d0-118">Les propriétés de l’auteur d’origine autoriser pour la conservation des informations à partir de l’extérieur du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="f50d0-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="f50d0-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tels qu’à partir d’Internet, ces propriétés fournissent un moyen pour vous assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="f50d0-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f50d0-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f50d0-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f50d0-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f50d0-121">Header files</span></span>

<span data-ttu-id="f50d0-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f50d0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f50d0-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f50d0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f50d0-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f50d0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f50d0-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="f50d0-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f50d0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f50d0-126">See also</span></span>



[<span data-ttu-id="f50d0-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f50d0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f50d0-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f50d0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f50d0-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f50d0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f50d0-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f50d0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

