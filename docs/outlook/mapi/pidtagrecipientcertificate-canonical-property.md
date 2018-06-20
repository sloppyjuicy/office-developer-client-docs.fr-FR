---
title: Propriété canonique PidTagRecipientCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786532"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="6db13-103">Propriété canonique PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="6db13-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="6db13-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6db13-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6db13-105">Contient un certificat ASN.1 d’un destinataire de message pour une utilisation dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="6db13-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6db13-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6db13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6db13-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="6db13-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="6db13-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6db13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6db13-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="6db13-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="6db13-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6db13-110">Data type:</span></span>  <br/> |<span data-ttu-id="6db13-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6db13-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6db13-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6db13-112">Area:</span></span>  <br/> |<span data-ttu-id="6db13-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="6db13-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6db13-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6db13-114">Remarks</span></span>

<span data-ttu-id="6db13-115">Cette propriété est une copie de la propriété du destinataire **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) pour une utilisation dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="6db13-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="6db13-116">Il peut être utilisé pour prouver à l’expéditeur que le destinataire a effectivement reçu le message, un rapport de remise n’indique pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="6db13-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6db13-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6db13-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6db13-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6db13-118">Header files</span></span>

<span data-ttu-id="6db13-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6db13-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6db13-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6db13-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6db13-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6db13-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6db13-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6db13-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6db13-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db13-123">See also</span></span>



[<span data-ttu-id="6db13-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6db13-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6db13-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6db13-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6db13-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6db13-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6db13-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6db13-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

