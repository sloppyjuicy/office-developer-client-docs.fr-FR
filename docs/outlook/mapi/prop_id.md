---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328573"
---
# <a name="propid"></a><span data-ttu-id="dec9c-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="dec9c-103">PROP_ID</span></span>

  
  
<span data-ttu-id="dec9c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dec9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dec9c-105">Renvoie l'identificateur de propriété d'une balise de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dec9c-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dec9c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dec9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="dec9c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dec9c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dec9c-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="dec9c-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="dec9c-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dec9c-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="dec9c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dec9c-110">Parameters</span></span>

 <span data-ttu-id="dec9c-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="dec9c-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="dec9c-112">Balise de propriété qui contient l'identificateur à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="dec9c-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dec9c-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="dec9c-113">Remarks</span></span>

<span data-ttu-id="dec9c-114">Chaque balise de propriété contient le type de propriété dans le mot de poids faible (bits 0 à 15) et l'identificateur de la propriété dans le mot de poids fort (bits 16 à 31).</span><span class="sxs-lookup"><span data-stu-id="dec9c-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="dec9c-115">La macro **PROP_ID** extrait l'identificateur de propriété et le place dans les bits 0 à 15 de l'entier à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="dec9c-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="dec9c-116">Les autres bits de la valeur de retour sont définis sur zéros.</span><span class="sxs-lookup"><span data-stu-id="dec9c-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="dec9c-117">La macro **PROP_ID** peut être utilisée, par exemple, pour récupérer un identificateur à transmettre à [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="dec9c-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="dec9c-118">**GetNamesFromIDs** récupère le nom de la propriété associée à un identificateur pour une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="dec9c-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dec9c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dec9c-119">See also</span></span>



[<span data-ttu-id="dec9c-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dec9c-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="dec9c-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="dec9c-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

