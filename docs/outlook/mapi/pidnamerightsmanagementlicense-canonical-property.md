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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1f528332c52664ac472670566c905d36dac65bfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565528"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="ca54f-103">Propriété canonique PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="ca54f-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="ca54f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca54f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca54f-105">Met en cache de la licence d’utilisation pour le message électronique géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="ca54f-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca54f-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="ca54f-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="ca54f-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="ca54f-107">None</span></span>  <br/> |
|<span data-ttu-id="ca54f-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="ca54f-108">Property set:</span></span>  <br/> |<span data-ttu-id="ca54f-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ca54f-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="ca54f-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="ca54f-110">Property name:</span></span>  <br/> |<span data-ttu-id="ca54f-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="ca54f-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="ca54f-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ca54f-112">Data type:</span></span>  <br/> |<span data-ttu-id="ca54f-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="ca54f-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="ca54f-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ca54f-114">Area:</span></span>  <br/> |<span data-ttu-id="ca54f-115">Messagerie sécurisée</span><span class="sxs-lookup"><span data-stu-id="ca54f-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca54f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca54f-116">Remarks</span></span>

<span data-ttu-id="ca54f-117">Si la propriété est présente dans un message électronique géré par des droits, la première valeur de cette propriété binaire plusieurs doit contenir la licence d’utilisation compressé ZLIB (comme spécifié dans [RFC1950]) pour le message électronique géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="ca54f-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca54f-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ca54f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca54f-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ca54f-119">Protocol specifications</span></span>

<span data-ttu-id="ca54f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca54f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca54f-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="ca54f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca54f-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca54f-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca54f-123">Spécifie les propriétés des messages codés géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="ca54f-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca54f-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ca54f-124">Header files</span></span>

<span data-ttu-id="ca54f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca54f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca54f-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ca54f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca54f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca54f-127">See also</span></span>



[<span data-ttu-id="ca54f-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ca54f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca54f-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ca54f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca54f-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ca54f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca54f-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ca54f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

