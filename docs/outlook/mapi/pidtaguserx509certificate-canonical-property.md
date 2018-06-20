---
title: Propriété canonique PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d27ef47a3ba387ae2e7acbcefc75b07ddd794e80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786911"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="46044-103">Propriété canonique PidTagUserX509Certificate</span><span class="sxs-lookup"><span data-stu-id="46044-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="46044-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46044-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46044-105">Contient les certificats de sécurité X.509 version 3 pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="46044-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46044-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="46044-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46044-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="46044-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="46044-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="46044-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46044-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="46044-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="46044-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="46044-110">Data type:</span></span>  <br/> |<span data-ttu-id="46044-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="46044-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="46044-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="46044-112">Area:</span></span>  <br/> |<span data-ttu-id="46044-113">Utilisateur de messagerie MAPI</span><span class="sxs-lookup"><span data-stu-id="46044-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46044-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="46044-114">Remarks</span></span>

<span data-ttu-id="46044-115">Cette propriété est utilisée par les applications qui utilisent la sécurité de clé publique.</span><span class="sxs-lookup"><span data-stu-id="46044-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="46044-116">Il conserve une représentation binaire d’un ou plusieurs certificats de sécurité 3 X.509 version.</span><span class="sxs-lookup"><span data-stu-id="46044-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="46044-117">Des clients et des applications différentes peuvent utiliser cette propriété leurs propres certificats de sécurité.</span><span class="sxs-lookup"><span data-stu-id="46044-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="46044-118">Le format des données X.509 binaire peut varier entre fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="46044-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="46044-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="46044-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46044-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="46044-120">Protocol specifications</span></span>

<span data-ttu-id="46044-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46044-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46044-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="46044-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46044-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46044-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46044-124">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="46044-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46044-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="46044-125">Header files</span></span>

<span data-ttu-id="46044-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46044-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="46044-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="46044-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="46044-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="46044-128">Mapitags.h</span></span>
  
> <span data-ttu-id="46044-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="46044-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46044-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46044-130">See also</span></span>



[<span data-ttu-id="46044-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="46044-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46044-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="46044-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46044-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="46044-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46044-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="46044-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

