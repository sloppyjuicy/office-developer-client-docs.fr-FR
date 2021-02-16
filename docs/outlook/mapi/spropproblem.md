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
# <a name="spropproblem"></a><span data-ttu-id="df027-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="df027-103">SPropProblem</span></span>

  
  
<span data-ttu-id="df027-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df027-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df027-105">Décrit une erreur liée à une opération impliquant une propriété.</span><span class="sxs-lookup"><span data-stu-id="df027-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df027-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="df027-106">Header file:</span></span>  <br/> |<span data-ttu-id="df027-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df027-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="df027-108">Members</span><span class="sxs-lookup"><span data-stu-id="df027-108">Members</span></span>

 <span data-ttu-id="df027-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="df027-109">**ulIndex**</span></span>
  
> <span data-ttu-id="df027-110">Index dans un tableau de balises de propriétés.</span><span class="sxs-lookup"><span data-stu-id="df027-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="df027-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="df027-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="df027-112">Balise de propriété de la propriété qui présente l’erreur.</span><span class="sxs-lookup"><span data-stu-id="df027-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="df027-113">**scode**</span><span class="sxs-lookup"><span data-stu-id="df027-113">**scode**</span></span>
  
> <span data-ttu-id="df027-114">Valeur d’erreur décrivant le problème avec la propriété.</span><span class="sxs-lookup"><span data-stu-id="df027-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="df027-115">Cette valeur peut être n’importe quelle valeur [MAPI SCODE.](scode.md)</span><span class="sxs-lookup"><span data-stu-id="df027-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="df027-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="df027-116">Remarks</span></span>

<span data-ttu-id="df027-117">Un tableau de structures **SPropProblem** est renvoyé à partir des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="df027-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="df027-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="df027-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="df027-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="df027-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="df027-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="df027-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="df027-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="df027-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="df027-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="df027-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="df027-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="df027-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="df027-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="df027-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="df027-125">Une structure **SPropProblem** contient une valeur d’erreur **SCODE** qui résulte d’une opération de modification ou de suppression d’une propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="df027-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="df027-126">Pour plus d’informations sur le fonctionnement de la structure **SPropProblem** avec les erreurs liées aux propriétés, voir [PROPRIÉTÉS nommées MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="df027-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df027-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df027-127">See also</span></span>



[<span data-ttu-id="df027-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="df027-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="df027-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="df027-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="df027-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="df027-130">MAPI Structures</span></span>](mapi-structures.md)

