---
title: Propriété canonique PidTagUserCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 53ee4019752cf717840199d4a51cbc90133b8636
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393886"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="be155-103">Propriété canonique PidTagUserCertificate</span><span class="sxs-lookup"><span data-stu-id="be155-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="be155-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be155-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be155-105">Contient un certificat d’authentification ASN.1 pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="be155-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be155-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="be155-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="be155-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="be155-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="be155-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="be155-108">Identifier:</span></span>  <br/> |<span data-ttu-id="be155-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="be155-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="be155-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="be155-110">Data type:</span></span>  <br/> |<span data-ttu-id="be155-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="be155-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="be155-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="be155-112">Area:</span></span>  <br/> |<span data-ttu-id="be155-113">Utilisateur de messagerie MAPI</span><span class="sxs-lookup"><span data-stu-id="be155-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be155-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="be155-114">Remarks</span></span>

<span data-ttu-id="be155-115">Un certificat d’authentification est similaire à une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="be155-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="be155-116">Plusieurs propriétés MAPI fournissent ASN.1 certificats.</span><span class="sxs-lookup"><span data-stu-id="be155-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="be155-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="be155-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="be155-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="be155-118">Protocol specifications</span></span>

<span data-ttu-id="be155-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be155-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be155-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="be155-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="be155-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be155-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="be155-122">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="be155-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="be155-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="be155-123">Header files</span></span>

<span data-ttu-id="be155-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be155-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="be155-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="be155-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="be155-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="be155-126">Mapitags.h</span></span>
  
> <span data-ttu-id="be155-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="be155-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="be155-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be155-128">See also</span></span>



[<span data-ttu-id="be155-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="be155-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="be155-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="be155-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="be155-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="be155-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="be155-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="be155-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

