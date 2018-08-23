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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7686f36ca105ab92161757d492a86b4b78461dfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564079"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="6e663-103">Propriété canonique PidTagUserX509Certificate</span><span class="sxs-lookup"><span data-stu-id="6e663-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="6e663-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e663-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e663-105">Contient les certificats de sécurité X.509 version 3 pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6e663-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e663-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6e663-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e663-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="6e663-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="6e663-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6e663-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e663-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="6e663-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="6e663-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6e663-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e663-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e663-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e663-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6e663-112">Area:</span></span>  <br/> |<span data-ttu-id="6e663-113">Utilisateur de messagerie MAPI</span><span class="sxs-lookup"><span data-stu-id="6e663-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e663-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e663-114">Remarks</span></span>

<span data-ttu-id="6e663-115">Cette propriété est utilisée par les applications qui utilisent la sécurité de clé publique.</span><span class="sxs-lookup"><span data-stu-id="6e663-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="6e663-116">Il conserve une représentation binaire d’un ou plusieurs certificats de sécurité 3 X.509 version.</span><span class="sxs-lookup"><span data-stu-id="6e663-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="6e663-117">Des clients et des applications différentes peuvent utiliser cette propriété leurs propres certificats de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6e663-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="6e663-118">Le format des données X.509 binaire peut varier entre fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="6e663-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e663-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6e663-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e663-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6e663-120">Protocol specifications</span></span>

<span data-ttu-id="6e663-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e663-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e663-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6e663-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e663-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e663-123">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e663-124">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="6e663-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e663-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6e663-125">Header files</span></span>

<span data-ttu-id="6e663-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e663-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e663-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6e663-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e663-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6e663-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6e663-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6e663-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e663-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e663-130">See also</span></span>



[<span data-ttu-id="6e663-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6e663-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e663-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6e663-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e663-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6e663-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e663-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6e663-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

