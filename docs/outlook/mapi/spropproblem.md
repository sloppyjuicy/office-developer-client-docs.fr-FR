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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7c19cce33ec351a5627870782ebb4fe509a98be2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573284"
---
# <a name="spropproblem"></a><span data-ttu-id="16c96-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="16c96-103">SPropProblem</span></span>

  
  
<span data-ttu-id="16c96-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16c96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16c96-105">Décrit une erreur qui sont associées à une opération impliquant une propriété.</span><span class="sxs-lookup"><span data-stu-id="16c96-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16c96-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="16c96-106">Header file:</span></span>  <br/> |<span data-ttu-id="16c96-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16c96-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="16c96-108">Members</span><span class="sxs-lookup"><span data-stu-id="16c96-108">Members</span></span>

 <span data-ttu-id="16c96-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="16c96-109">**ulIndex**</span></span>
  
> <span data-ttu-id="16c96-110">Un index dans un tableau de balises de propriété.</span><span class="sxs-lookup"><span data-stu-id="16c96-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="16c96-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="16c96-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="16c96-112">Balise de propriété pour la propriété qui comporte l’erreur.</span><span class="sxs-lookup"><span data-stu-id="16c96-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="16c96-113">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="16c96-113">**scode**</span></span>
  
> <span data-ttu-id="16c96-114">Valeur d’erreur décrivant le problème avec la propriété.</span><span class="sxs-lookup"><span data-stu-id="16c96-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="16c96-115">Cette valeur peut être n’importe quelle valeur MAPI [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="16c96-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="16c96-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="16c96-116">Remarks</span></span>

<span data-ttu-id="16c96-117">Un tableau de structures **SPropProblem** est renvoyé à partir des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="16c96-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="16c96-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="16c96-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="16c96-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="16c96-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="16c96-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="16c96-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="16c96-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="16c96-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="16c96-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="16c96-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="16c96-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="16c96-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="16c96-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="16c96-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="16c96-125">Une structure **SPropProblem** contient une valeur d’erreur **SCODE** qui se traduit par une opération que vous tentez de modifier ou supprimer une propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="16c96-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="16c96-126">Pour plus d’informations sur le fonctionne de la structure **SPropProblem** avec des erreurs liées aux propriétés, voir [Les propriétés MAPI nommée](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="16c96-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16c96-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16c96-127">See also</span></span>



[<span data-ttu-id="16c96-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="16c96-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="16c96-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="16c96-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="16c96-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="16c96-130">MAPI Structures</span></span>](mapi-structures.md)

