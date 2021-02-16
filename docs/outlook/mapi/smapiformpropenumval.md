---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435410"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="56ab8-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="56ab8-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="56ab8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56ab8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56ab8-105">Cette propriété m’indique si une valeur d’un nom complet est un nom complet.</span><span class="sxs-lookup"><span data-stu-id="56ab8-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56ab8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="56ab8-106">Header file:</span></span>  <br/> |<span data-ttu-id="56ab8-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="56ab8-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="56ab8-108">Members</span><span class="sxs-lookup"><span data-stu-id="56ab8-108">Members</span></span>

 <span data-ttu-id="56ab8-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="56ab8-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="56ab8-110">Chaîne qui contient le nom complet de la valeur spécifiée dans le membre **nVal.**</span><span class="sxs-lookup"><span data-stu-id="56ab8-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="56ab8-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="56ab8-111">**nVal**</span></span>
  
> <span data-ttu-id="56ab8-112">Valeur d’éumération pour le nom complet pointé par le membre **pszDisplayName.**</span><span class="sxs-lookup"><span data-stu-id="56ab8-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="56ab8-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="56ab8-113">Remarks</span></span>

<span data-ttu-id="56ab8-114">Lorsqu’un utilisateur sélectionne un nom complet dans un formulaire, la valeur d’éumération correspondante du nom est stockée à l’aide de l’implémentation de l’interface [IMAPIProp](imapipropiunknown.md) associée au formulaire.</span><span class="sxs-lookup"><span data-stu-id="56ab8-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56ab8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56ab8-115">See also</span></span>



[<span data-ttu-id="56ab8-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="56ab8-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="56ab8-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="56ab8-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="56ab8-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="56ab8-118">MAPI Structures</span></span>](mapi-structures.md)

