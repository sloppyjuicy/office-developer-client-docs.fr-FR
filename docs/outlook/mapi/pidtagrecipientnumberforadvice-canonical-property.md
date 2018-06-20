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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ac4da2d4082cac632548594411528b7bf1d6dc64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786523"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="ab2aa-103">Propriété canonique PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="ab2aa-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="ab2aa-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab2aa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab2aa-105">Cette propriété contient le numéro de téléphone du destinataire du message à appeler pour signaler la remise physique d’un message.</span><span class="sxs-lookup"><span data-stu-id="ab2aa-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab2aa-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ab2aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab2aa-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="ab2aa-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="ab2aa-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ab2aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab2aa-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="ab2aa-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="ab2aa-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ab2aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab2aa-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab2aa-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ab2aa-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ab2aa-112">Area:</span></span>  <br/> |<span data-ttu-id="ab2aa-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="ab2aa-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab2aa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab2aa-114">Remarks</span></span>

<span data-ttu-id="ab2aa-115">Ces propriétés sont destinées à être utilisées conjointement avec la remise vers une destination physique, plutôt qu’une boîte aux lettres électronique, lorsque le destinataire humain n’est pas censé être présent à la remise.</span><span class="sxs-lookup"><span data-stu-id="ab2aa-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="ab2aa-116">Le numéro de téléphone sur une page de garde est un exemple.</span><span class="sxs-lookup"><span data-stu-id="ab2aa-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ab2aa-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ab2aa-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ab2aa-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ab2aa-118">Header files</span></span>

<span data-ttu-id="ab2aa-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab2aa-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab2aa-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ab2aa-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab2aa-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ab2aa-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ab2aa-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ab2aa-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab2aa-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab2aa-123">See also</span></span>



[<span data-ttu-id="ab2aa-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ab2aa-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab2aa-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ab2aa-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab2aa-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ab2aa-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab2aa-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ab2aa-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

