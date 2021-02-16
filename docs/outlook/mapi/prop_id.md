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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409131"
---
# <a name="prop_id"></a><span data-ttu-id="18ff0-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="18ff0-103">PROP_ID</span></span>

  
  
<span data-ttu-id="18ff0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18ff0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18ff0-105">Renvoie l’identificateur de propriété d’une balise de propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="18ff0-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18ff0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="18ff0-106">Header file:</span></span>  <br/> |<span data-ttu-id="18ff0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18ff0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="18ff0-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="18ff0-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="18ff0-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="18ff0-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="18ff0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18ff0-110">Parameters</span></span>

 <span data-ttu-id="18ff0-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="18ff0-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="18ff0-112">Balise de propriété qui contient l’identificateur à retourner.</span><span class="sxs-lookup"><span data-stu-id="18ff0-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18ff0-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="18ff0-113">Remarks</span></span>

<span data-ttu-id="18ff0-114">Chaque balise de propriété contient le type de propriété dans le mot de bas ordre (bits 0 à 15) et l’identificateur de propriété dans le mot de haut niveau (bits 16 à 31).</span><span class="sxs-lookup"><span data-stu-id="18ff0-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="18ff0-115">La **PROP_ID** macro extrait l’identificateur de propriété et le place en bits 0 à 15 de l’ensemble à retourner.</span><span class="sxs-lookup"><span data-stu-id="18ff0-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="18ff0-116">Les autres bits de la valeur de retour sont des zéros.</span><span class="sxs-lookup"><span data-stu-id="18ff0-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="18ff0-117">La **macro PROP_ID** peut être utilisée, par exemple, pour récupérer un identificateur à transmettre à [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="18ff0-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="18ff0-118">**GetNamesFromIDs** récupère le nom de propriété associé à un identificateur pour une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="18ff0-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="18ff0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18ff0-119">See also</span></span>



[<span data-ttu-id="18ff0-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="18ff0-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="18ff0-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="18ff0-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

