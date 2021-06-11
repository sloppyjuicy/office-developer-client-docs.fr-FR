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
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="a0fc4-103">Propriété canonique PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="a0fc4-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="a0fc4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0fc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0fc4-105">Contient TRUE si le client demande un champ d’en-tête X-MS-Exchange-Organization-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="a0fc4-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0fc4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a0fc4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0fc4-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="a0fc4-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="a0fc4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a0fc4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0fc4-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="a0fc4-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="a0fc4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a0fc4-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0fc4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a0fc4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a0fc4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a0fc4-112">Area:</span></span>  <br/> |<span data-ttu-id="a0fc4-113">Rapports généraux</span><span class="sxs-lookup"><span data-stu-id="a0fc4-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0fc4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0fc4-114">Remarks</span></span>

<span data-ttu-id="a0fc4-115">Si cette propriété est définie sur FALSE ou n’est pas utilisée, aucun champ d’en-tête X-MS-Exchange-Organization-AutoForwarded n’est créé.</span><span class="sxs-lookup"><span data-stu-id="a0fc4-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a0fc4-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a0fc4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0fc4-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a0fc4-117">Protocol specifications</span></span>

<span data-ttu-id="a0fc4-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0fc4-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0fc4-119">Définit chaque propriété utilisée dans les objets décrits par les documents préfixés MS-OXO.</span><span class="sxs-lookup"><span data-stu-id="a0fc4-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="a0fc4-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0fc4-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0fc4-121">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="a0fc4-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0fc4-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a0fc4-122">Header files</span></span>

<span data-ttu-id="a0fc4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0fc4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0fc4-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a0fc4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0fc4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0fc4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a0fc4-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a0fc4-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0fc4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0fc4-127">See also</span></span>



[<span data-ttu-id="a0fc4-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a0fc4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0fc4-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a0fc4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0fc4-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a0fc4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0fc4-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a0fc4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

