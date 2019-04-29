---
title: Propriété canonique PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b6900cbacc2bea6c5519efdc4281ca98629b23bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425672"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="a18bc-103">Propriété canonique PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="a18bc-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="a18bc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a18bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a18bc-105">Contient une étiquette de sécurité pour un message.</span><span class="sxs-lookup"><span data-stu-id="a18bc-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a18bc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a18bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a18bc-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="a18bc-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="a18bc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a18bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a18bc-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="a18bc-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="a18bc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a18bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="a18bc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a18bc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a18bc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a18bc-112">Area:</span></span>  <br/> |<span data-ttu-id="a18bc-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="a18bc-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a18bc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a18bc-114">Remarks</span></span>

<span data-ttu-id="a18bc-115">Cette propriété indique la base sur laquelle la propriété **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protège un message.</span><span class="sxs-lookup"><span data-stu-id="a18bc-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="a18bc-116">Son association avec le contenu du message est garantie par le jeton.</span><span class="sxs-lookup"><span data-stu-id="a18bc-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a18bc-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a18bc-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a18bc-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a18bc-118">Header files</span></span>

<span data-ttu-id="a18bc-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a18bc-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="a18bc-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a18bc-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="a18bc-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a18bc-121">Mapitags.h</span></span>
  
> <span data-ttu-id="a18bc-122">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="a18bc-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a18bc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a18bc-123">See also</span></span>



[<span data-ttu-id="a18bc-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a18bc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a18bc-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a18bc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a18bc-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a18bc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a18bc-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a18bc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

