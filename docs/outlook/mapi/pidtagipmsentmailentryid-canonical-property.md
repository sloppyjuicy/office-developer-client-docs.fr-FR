---
title: Propriété canonique PidTagIpmSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fd29afc93bc952bb619dfac752fae232bf7991cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437321"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="1d7be-103">Propriété canonique PidTagIpmSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="1d7be-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1d7be-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d7be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d7be-105">Contient l’identificateur d’entrée du dossier Éléments envoyés du message interpersonnel standard (IPM).</span><span class="sxs-lookup"><span data-stu-id="1d7be-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d7be-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1d7be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d7be-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1d7be-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1d7be-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1d7be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d7be-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="1d7be-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="1d7be-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1d7be-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d7be-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1d7be-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1d7be-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1d7be-112">Area:</span></span>  <br/> |<span data-ttu-id="1d7be-113">Folder</span><span class="sxs-lookup"><span data-stu-id="1d7be-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d7be-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d7be-114">Remarks</span></span>

<span data-ttu-id="1d7be-115">Une fois envoyés, les messages interpersonnels sont généralement placés dans le dossier Éléments envoyés.</span><span class="sxs-lookup"><span data-stu-id="1d7be-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="1d7be-116">Un client peut utiliser cette propriété pour définir la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) sur un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="1d7be-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1d7be-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1d7be-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1d7be-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1d7be-118">Header files</span></span>

<span data-ttu-id="1d7be-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d7be-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d7be-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1d7be-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d7be-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1d7be-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1d7be-122">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="1d7be-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d7be-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d7be-123">See also</span></span>



[<span data-ttu-id="1d7be-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1d7be-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d7be-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1d7be-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d7be-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1d7be-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d7be-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1d7be-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

