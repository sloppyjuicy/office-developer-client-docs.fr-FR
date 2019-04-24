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
ms.openlocfilehash: 4e6446283116c39080271e5c2fb3ec128b25d32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360717"
---
# <a name="pidtaguserx509certificate-canonical-property"></a><span data-ttu-id="a8bb5-103">Propriété canonique PidTagUserX509Certificate</span><span class="sxs-lookup"><span data-stu-id="a8bb5-103">PidTagUserX509Certificate Canonical Property</span></span>

  
  
<span data-ttu-id="a8bb5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8bb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8bb5-105">Contient les certificats de sécurité de la version 3 de X. 509 pour un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-105">Contains X.509 version 3 security certificates for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8bb5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a8bb5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8bb5-107">PR_USER_X509_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="a8bb5-107">PR_USER_X509_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="a8bb5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a8bb5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8bb5-109">0x3A70</span><span class="sxs-lookup"><span data-stu-id="a8bb5-109">0x3A70</span></span>  <br/> |
|<span data-ttu-id="a8bb5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a8bb5-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8bb5-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="a8bb5-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="a8bb5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a8bb5-112">Area:</span></span>  <br/> |<span data-ttu-id="a8bb5-113">Utilisateur de messagerie MAPI</span><span class="sxs-lookup"><span data-stu-id="a8bb5-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8bb5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8bb5-114">Remarks</span></span>

<span data-ttu-id="a8bb5-115">Cette propriété est utilisée par les applications qui utilisent la sécurité à clé publique.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-115">This property is used by applications that utilize public-key security.</span></span> <span data-ttu-id="a8bb5-116">Il contient une représentation binaire d'un ou plusieurs certificats de sécurité X. 509 version 3.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-116">It holds a binary representation of one or more X.509 version 3 security certificates.</span></span> 
  
<span data-ttu-id="a8bb5-117">Plusieurs applications et clients peuvent utiliser cette propriété pour leurs propres certificats de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-117">Various applications and clients can use this property for their own security certificates.</span></span> <span data-ttu-id="a8bb5-118">Le format binaire des données X. 509 peut varier d'un fournisseur à l'autre.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-118">The binary format of the X.509 data can vary among vendors.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a8bb5-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a8bb5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8bb5-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a8bb5-120">Protocol specifications</span></span>

<span data-ttu-id="a8bb5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8bb5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8bb5-122">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a8bb5-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8bb5-123">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8bb5-124">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-124">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8bb5-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a8bb5-125">Header files</span></span>

<span data-ttu-id="a8bb5-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a8bb5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8bb5-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a8bb5-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a8bb5-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a8bb5-129">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="a8bb5-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8bb5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8bb5-130">See also</span></span>



[<span data-ttu-id="a8bb5-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a8bb5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8bb5-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a8bb5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8bb5-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a8bb5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8bb5-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a8bb5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

