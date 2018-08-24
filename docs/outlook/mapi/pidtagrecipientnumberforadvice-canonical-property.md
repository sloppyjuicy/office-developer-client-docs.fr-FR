---
title: Propriété canonique PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3f23a332ee6778f71ce0809dfae8c0b6a92246a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595145"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="0fbc6-103">Propriété canonique PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="0fbc6-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="0fbc6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fbc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fbc6-105">Cette propriété contient le numéro de téléphone du destinataire du message à appeler pour signaler la remise physique d’un message.</span><span class="sxs-lookup"><span data-stu-id="0fbc6-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fbc6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0fbc6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fbc6-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="0fbc6-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="0fbc6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0fbc6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0fbc6-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="0fbc6-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="0fbc6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0fbc6-110">Data type:</span></span>  <br/> |<span data-ttu-id="0fbc6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0fbc6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0fbc6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0fbc6-112">Area:</span></span>  <br/> |<span data-ttu-id="0fbc6-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="0fbc6-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fbc6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0fbc6-114">Remarks</span></span>

<span data-ttu-id="0fbc6-115">Ces propriétés sont destinées à être utilisées conjointement avec la remise vers une destination physique, plutôt qu’une boîte aux lettres électronique, lorsque le destinataire humain n’est pas censé être présent à la remise.</span><span class="sxs-lookup"><span data-stu-id="0fbc6-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="0fbc6-116">Le numéro de téléphone sur une page de garde est un exemple.</span><span class="sxs-lookup"><span data-stu-id="0fbc6-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0fbc6-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0fbc6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0fbc6-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0fbc6-118">Header files</span></span>

<span data-ttu-id="0fbc6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0fbc6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fbc6-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0fbc6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0fbc6-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0fbc6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0fbc6-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="0fbc6-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fbc6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fbc6-123">See also</span></span>



[<span data-ttu-id="0fbc6-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0fbc6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fbc6-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0fbc6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fbc6-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0fbc6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fbc6-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0fbc6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

