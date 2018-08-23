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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 464db3d360f6e872ac28f8d7cbec842d8b521f7e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585114"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="5787b-103">Propriété canonique PidTagRecipientCertificate</span><span class="sxs-lookup"><span data-stu-id="5787b-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="5787b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5787b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5787b-105">Contient un certificat ASN.1 d’un destinataire de message pour une utilisation dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="5787b-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5787b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5787b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5787b-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="5787b-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="5787b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5787b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5787b-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="5787b-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="5787b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5787b-110">Data type:</span></span>  <br/> |<span data-ttu-id="5787b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5787b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5787b-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5787b-112">Area:</span></span>  <br/> |<span data-ttu-id="5787b-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="5787b-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5787b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5787b-114">Remarks</span></span>

<span data-ttu-id="5787b-115">Cette propriété est une copie de la propriété du destinataire **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) pour une utilisation dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="5787b-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="5787b-116">Il peut être utilisé pour prouver à l’expéditeur que le destinataire a effectivement reçu le message, un rapport de remise n’indique pas nécessairement.</span><span class="sxs-lookup"><span data-stu-id="5787b-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5787b-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5787b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5787b-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5787b-118">Header files</span></span>

<span data-ttu-id="5787b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5787b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="5787b-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5787b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="5787b-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5787b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="5787b-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5787b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5787b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5787b-123">See also</span></span>



[<span data-ttu-id="5787b-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5787b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5787b-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5787b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5787b-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5787b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5787b-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5787b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

