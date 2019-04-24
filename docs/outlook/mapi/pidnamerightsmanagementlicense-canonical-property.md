---
title: Propriété canonique PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315021"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="a98c4-103">Propriété canonique PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="a98c4-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="a98c4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a98c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a98c4-105">Met en cache la licence d'utilisation pour le message électronique géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="a98c4-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a98c4-106">Noms conviviaux:</span><span class="sxs-lookup"><span data-stu-id="a98c4-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="a98c4-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="a98c4-107">None</span></span>  <br/> |
|<span data-ttu-id="a98c4-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="a98c4-108">Property set:</span></span>  <br/> |<span data-ttu-id="a98c4-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="a98c4-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="a98c4-110">Nom de la propriété:</span><span class="sxs-lookup"><span data-stu-id="a98c4-110">Property name:</span></span>  <br/> |<span data-ttu-id="a98c4-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="a98c4-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="a98c4-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a98c4-112">Data type:</span></span>  <br/> |<span data-ttu-id="a98c4-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="a98c4-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="a98c4-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a98c4-114">Area:</span></span>  <br/> |<span data-ttu-id="a98c4-115">Messagerie sécurisée</span><span class="sxs-lookup"><span data-stu-id="a98c4-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a98c4-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a98c4-116">Remarks</span></span>

<span data-ttu-id="a98c4-117">Si la propriété est présente dans un message électronique géré par des droits, la première valeur de cette propriété multiple Binary doit contenir la licence ZLIB (comme spécifié dans [RFC1950]) utilisation compressée pour le message électronique géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="a98c4-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a98c4-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a98c4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a98c4-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a98c4-119">Protocol specifications</span></span>

<span data-ttu-id="a98c4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a98c4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a98c4-121">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a98c4-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a98c4-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a98c4-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a98c4-123">Spécifie les propriétés des messages codés gérés par des droits.</span><span class="sxs-lookup"><span data-stu-id="a98c4-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a98c4-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a98c4-124">Header files</span></span>

<span data-ttu-id="a98c4-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a98c4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a98c4-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a98c4-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a98c4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a98c4-127">See also</span></span>



[<span data-ttu-id="a98c4-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a98c4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a98c4-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a98c4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a98c4-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a98c4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a98c4-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a98c4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

