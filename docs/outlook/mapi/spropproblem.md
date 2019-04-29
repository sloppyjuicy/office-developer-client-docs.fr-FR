---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407773"
---
# <a name="spropproblem"></a><span data-ttu-id="54f9d-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="54f9d-103">SPropProblem</span></span>

  
  
<span data-ttu-id="54f9d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54f9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54f9d-105">Décrit une erreur liée à une opération impliquant une propriété.</span><span class="sxs-lookup"><span data-stu-id="54f9d-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54f9d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="54f9d-106">Header file:</span></span>  <br/> |<span data-ttu-id="54f9d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="54f9d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="54f9d-108">Members</span><span class="sxs-lookup"><span data-stu-id="54f9d-108">Members</span></span>

 <span data-ttu-id="54f9d-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="54f9d-109">**ulIndex**</span></span>
  
> <span data-ttu-id="54f9d-110">Index dans un tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="54f9d-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="54f9d-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="54f9d-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="54f9d-112">Balise de propriété de la propriété présentant l'erreur.</span><span class="sxs-lookup"><span data-stu-id="54f9d-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="54f9d-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="54f9d-113">**scode**</span></span>
  
> <span data-ttu-id="54f9d-114">Valeur d'erreur décrivant le problème lié à la propriété.</span><span class="sxs-lookup"><span data-stu-id="54f9d-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="54f9d-115">Cette valeur peut être n'importe quelle valeur [SCODE](scode.md) MAPI.</span><span class="sxs-lookup"><span data-stu-id="54f9d-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54f9d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="54f9d-116">Remarks</span></span>

<span data-ttu-id="54f9d-117">Un tableau de structures **SPropProblem** est renvoyé à partir des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="54f9d-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="54f9d-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="54f9d-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="54f9d-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="54f9d-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="54f9d-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="54f9d-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="54f9d-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="54f9d-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="54f9d-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="54f9d-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="54f9d-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="54f9d-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="54f9d-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="54f9d-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="54f9d-125">Une structure **SPropProblem** contient une valeur d'erreur **SCODE** qui résulte d'une opération tentant de modifier ou de supprimer une propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="54f9d-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="54f9d-126">Pour plus d'informations sur la façon dont la structure **SPropProblem** fonctionne avec les erreurs liées aux propriétés, consultez la rubrique [MAPI named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="54f9d-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54f9d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54f9d-127">See also</span></span>



[<span data-ttu-id="54f9d-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="54f9d-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="54f9d-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="54f9d-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="54f9d-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="54f9d-130">MAPI Structures</span></span>](mapi-structures.md)

