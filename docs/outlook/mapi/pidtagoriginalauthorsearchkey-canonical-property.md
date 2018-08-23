---
title: Propriété canonique PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 225c0813139a74b735b5b8a3d5a729e630cd3511
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563337"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a><span data-ttu-id="6613e-103">Propriété canonique PidTagOriginalAuthorSearchKey</span><span class="sxs-lookup"><span data-stu-id="6613e-103">PidTagOriginalAuthorSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="6613e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6613e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6613e-105">Contient la clé de recherche de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="6613e-105">Contains the search key of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6613e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6613e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6613e-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="6613e-107">PR_ORIGINAL_AUTHOR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="6613e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6613e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6613e-109">0x0056</span><span class="sxs-lookup"><span data-stu-id="6613e-109">0x0056</span></span>  <br/> |
|<span data-ttu-id="6613e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6613e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6613e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6613e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6613e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6613e-112">Area:</span></span>  <br/> |<span data-ttu-id="6613e-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="6613e-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6613e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6613e-114">Remarks</span></span>

<span data-ttu-id="6613e-115">Cette propriété est une des propriétés d’adresse de l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="6613e-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="6613e-116">Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de la propriété[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_SEARCH_KEY**.</span><span class="sxs-lookup"><span data-stu-id="6613e-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) property.</span></span> <span data-ttu-id="6613e-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="6613e-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="6613e-118">Les propriétés de l’auteur d’origine autoriser pour la conservation des informations à partir de l’extérieur du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="6613e-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="6613e-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tels qu’à partir d’Internet, ces propriétés fournissent un moyen pour vous assurer que les informations d’origine ne sont pas perdues.</span><span class="sxs-lookup"><span data-stu-id="6613e-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6613e-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6613e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6613e-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6613e-121">Header files</span></span>

<span data-ttu-id="6613e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6613e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6613e-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6613e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6613e-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6613e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6613e-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6613e-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6613e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6613e-126">See also</span></span>



[<span data-ttu-id="6613e-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6613e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6613e-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6613e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6613e-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6613e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6613e-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6613e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

