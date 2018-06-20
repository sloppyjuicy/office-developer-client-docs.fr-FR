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
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785618"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="ffcbb-103">Propriété canonique PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="ffcbb-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="ffcbb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ffcbb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ffcbb-105">Met en cache de la licence d’utilisation pour le message électronique géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffcbb-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="ffcbb-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ffcbb-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="ffcbb-107">None</span></span>  <br/> |
|<span data-ttu-id="ffcbb-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="ffcbb-108">Property set:</span></span>  <br/> |<span data-ttu-id="ffcbb-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ffcbb-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="ffcbb-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="ffcbb-110">Property name:</span></span>  <br/> |<span data-ttu-id="ffcbb-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="ffcbb-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="ffcbb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ffcbb-112">Data type:</span></span>  <br/> |<span data-ttu-id="ffcbb-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="ffcbb-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="ffcbb-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="ffcbb-114">Area:</span></span>  <br/> |<span data-ttu-id="ffcbb-115">Messagerie sécurisée</span><span class="sxs-lookup"><span data-stu-id="ffcbb-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffcbb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffcbb-116">Remarks</span></span>

<span data-ttu-id="ffcbb-117">Si la propriété est présente dans un message électronique géré par des droits, la première valeur de cette propriété binaire plusieurs doit contenir la licence d’utilisation compressé ZLIB (comme spécifié dans [RFC1950]) pour le message électronique géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ffcbb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ffcbb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffcbb-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ffcbb-119">Protocol specifications</span></span>

<span data-ttu-id="ffcbb-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffcbb-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffcbb-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffcbb-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffcbb-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffcbb-123">Spécifie les propriétés des messages codés géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffcbb-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ffcbb-124">Header files</span></span>

<span data-ttu-id="ffcbb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffcbb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffcbb-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffcbb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffcbb-127">See also</span></span>



[<span data-ttu-id="ffcbb-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ffcbb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffcbb-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ffcbb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffcbb-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ffcbb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffcbb-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ffcbb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

