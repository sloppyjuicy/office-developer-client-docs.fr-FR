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
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578716"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="dea2a-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="dea2a-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="dea2a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dea2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dea2a-105">Mappe une valeur entière énumérée à un nom d’affichage pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="dea2a-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dea2a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dea2a-106">Header file:</span></span>  <br/> |<span data-ttu-id="dea2a-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="dea2a-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="dea2a-108">Members</span><span class="sxs-lookup"><span data-stu-id="dea2a-108">Members</span></span>

 <span data-ttu-id="dea2a-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="dea2a-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="dea2a-110">Chaîne qui contient le nom complet de la valeur spécifiée dans le membre **nVal** .</span><span class="sxs-lookup"><span data-stu-id="dea2a-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="dea2a-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="dea2a-111">**nVal**</span></span>
  
> <span data-ttu-id="dea2a-112">Une valeur d’énumération pour le nom complet vers laquelle pointe le membre **pszDisplayName** .</span><span class="sxs-lookup"><span data-stu-id="dea2a-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dea2a-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="dea2a-113">Remarks</span></span>

<span data-ttu-id="dea2a-114">Lorsqu’un utilisateur sélectionne un nom d’affichage d’un formulaire, la valeur d’énumération du nom correspondant est stocké à l’aide de l’implémentation d’interface [IMAPIProp](imapipropiunknown.md) qui est associée au formulaire.</span><span class="sxs-lookup"><span data-stu-id="dea2a-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dea2a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea2a-115">See also</span></span>



[<span data-ttu-id="dea2a-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="dea2a-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="dea2a-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dea2a-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="dea2a-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="dea2a-118">MAPI Structures</span></span>](mapi-structures.md)

