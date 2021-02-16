---
title: Propriété canonique PidTagAutoForwarded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326613"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="9aa5e-103">Propriété canonique PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="9aa5e-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="9aa5e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9aa5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9aa5e-105">Contient TRUE si le client demande un champ d’en-tête X-MS-Exchange-Organization-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9aa5e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9aa5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9aa5e-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="9aa5e-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="9aa5e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9aa5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9aa5e-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="9aa5e-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="9aa5e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9aa5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9aa5e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9aa5e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9aa5e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9aa5e-112">Area:</span></span>  <br/> |<span data-ttu-id="9aa5e-113">Rapports généraux</span><span class="sxs-lookup"><span data-stu-id="9aa5e-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9aa5e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9aa5e-114">Remarks</span></span>

<span data-ttu-id="9aa5e-115">Si cette propriété est définie sur FALSE ou n’est pas utilisée, aucun champ d’en-tête X-MS-Exchange-Organization-AutoForwarded n’est créé.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9aa5e-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9aa5e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9aa5e-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9aa5e-117">Protocol specifications</span></span>

<span data-ttu-id="9aa5e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9aa5e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9aa5e-119">Définit chaque propriété utilisée dans les objets décrits par les documents préfixés MS-OXO.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="9aa5e-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9aa5e-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9aa5e-121">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9aa5e-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9aa5e-122">Header files</span></span>

<span data-ttu-id="9aa5e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9aa5e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9aa5e-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9aa5e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9aa5e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9aa5e-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9aa5e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9aa5e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9aa5e-127">See also</span></span>



[<span data-ttu-id="9aa5e-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9aa5e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9aa5e-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9aa5e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9aa5e-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9aa5e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9aa5e-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9aa5e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

