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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787200"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="4c74b-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="4c74b-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="4c74b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c74b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c74b-105">Mappe une valeur entière énumérée à un nom d’affichage pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="4c74b-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c74b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4c74b-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c74b-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="4c74b-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="4c74b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4c74b-108">Members</span></span>

 <span data-ttu-id="4c74b-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="4c74b-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="4c74b-110">Chaîne qui contient le nom complet de la valeur spécifiée dans le membre **nVal** .</span><span class="sxs-lookup"><span data-stu-id="4c74b-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="4c74b-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="4c74b-111">**nVal**</span></span>
  
> <span data-ttu-id="4c74b-112">Une valeur d’énumération pour le nom complet vers laquelle pointe le membre **pszDisplayName** .</span><span class="sxs-lookup"><span data-stu-id="4c74b-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4c74b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c74b-113">Remarks</span></span>

<span data-ttu-id="4c74b-114">Lorsqu’un utilisateur sélectionne un nom d’affichage d’un formulaire, la valeur d’énumération du nom correspondant est stocké à l’aide de l’implémentation d’interface [IMAPIProp](imapipropiunknown.md) qui est associée au formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c74b-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c74b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c74b-115">See also</span></span>



[<span data-ttu-id="4c74b-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="4c74b-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="4c74b-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4c74b-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="4c74b-118">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="4c74b-118">MAPI Structures</span></span>](mapi-structures.md)

