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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 03dcc9a1f929bc6f99ca9e1dd9f75f3fb9c3dcb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562966"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="38956-103">Propriété canonique PidTagOriginalAuthorEntryId</span><span class="sxs-lookup"><span data-stu-id="38956-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="38956-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38956-105">Contient l’identificateur d’entrée de l’auteur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="38956-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38956-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="38956-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38956-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="38956-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="38956-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="38956-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38956-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="38956-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="38956-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="38956-110">Data type:</span></span>  <br/> |<span data-ttu-id="38956-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="38956-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="38956-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="38956-112">Area:</span></span>  <br/> |<span data-ttu-id="38956-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="38956-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38956-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="38956-114">Remarks</span></span>

<span data-ttu-id="38956-115">Cette propriété est une des propriétés d’adresse de l’auteur d’un message.</span><span class="sxs-lookup"><span data-stu-id="38956-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="38956-116">Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38956-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="38956-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="38956-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="38956-118">Permet à la propriété author d’origine pour la conservation des informations à partir de l’extérieur du domaine de messagerie local.</span><span class="sxs-lookup"><span data-stu-id="38956-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="38956-119">Lorsqu’un message arrive à partir d’un autre domaine de messagerie, tels que depuis Internet, cette propriété fournit un moyen pour que les informations d’origine n’est pas perdue.</span><span class="sxs-lookup"><span data-stu-id="38956-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38956-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="38956-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="38956-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="38956-121">Header files</span></span>

<span data-ttu-id="38956-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38956-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="38956-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="38956-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="38956-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="38956-124">Mapitags.h</span></span>
  
> <span data-ttu-id="38956-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="38956-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38956-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38956-126">See also</span></span>



[<span data-ttu-id="38956-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="38956-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38956-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="38956-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38956-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="38956-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38956-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="38956-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

