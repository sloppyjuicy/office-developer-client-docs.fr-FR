---
title: Propriété canonique PidTagOriginatorCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 966af9b3b3cbe52031402450be324ab6821d53ac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586577"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="2a3c9-103">Propriété canonique PidTagOriginatorCertificate</span><span class="sxs-lookup"><span data-stu-id="2a3c9-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="2a3c9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a3c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a3c9-105">Contient un certificat ASN.1 pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a3c9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2a3c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a3c9-107">PR_ORIGINATOR_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="2a3c9-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="2a3c9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2a3c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a3c9-109">0 x 0022</span><span class="sxs-lookup"><span data-stu-id="2a3c9-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="2a3c9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2a3c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a3c9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a3c9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a3c9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2a3c9-112">Area:</span></span>  <br/> |<span data-ttu-id="2a3c9-113">MIME</span><span class="sxs-lookup"><span data-stu-id="2a3c9-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a3c9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a3c9-114">Remarks</span></span>

<span data-ttu-id="2a3c9-115">Cette propriété est une copie de la propriété **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2a3c9-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2a3c9-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2a3c9-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2a3c9-117">Header files</span></span>

<span data-ttu-id="2a3c9-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a3c9-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a3c9-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a3c9-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="2a3c9-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2a3c9-121">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a3c9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a3c9-122">See also</span></span>



[<span data-ttu-id="2a3c9-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2a3c9-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a3c9-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2a3c9-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a3c9-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2a3c9-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a3c9-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2a3c9-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

