---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579717"
---
# <a name="validateparms"></a><span data-ttu-id="11b81-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="11b81-103">ValidateParms</span></span>

  
  
<span data-ttu-id="11b81-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11b81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11b81-105">Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="11b81-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11b81-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="11b81-106">Header file:</span></span>  <br/> |<span data-ttu-id="11b81-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="11b81-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="11b81-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="11b81-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11b81-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="11b81-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="11b81-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="11b81-110">Called by:</span></span>  <br/> |<span data-ttu-id="11b81-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="11b81-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="11b81-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11b81-112">Parameters</span></span>

 <span data-ttu-id="11b81-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="11b81-113">_eMethod_</span></span>
  
> <span data-ttu-id="11b81-114">[in] Spécifie, par l’énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="11b81-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="11b81-115">_Premier_</span><span class="sxs-lookup"><span data-stu-id="11b81-115">_First_</span></span>
  
> <span data-ttu-id="11b81-116">[in] Pointeur vers le premier argument dans la pile.</span><span class="sxs-lookup"><span data-stu-id="11b81-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11b81-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11b81-117">Return value</span></span>

<span data-ttu-id="11b81-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="11b81-118">S_OK</span></span> 
  
> <span data-ttu-id="11b81-119">Tous les paramètres sont valides.</span><span class="sxs-lookup"><span data-stu-id="11b81-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="11b81-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="11b81-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="11b81-121">Un ou plusieurs des paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="11b81-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11b81-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="11b81-122">Remarks</span></span>

<span data-ttu-id="11b81-123">Paramètres passés entre MAPI et service fournisseurs sont supposés être correct et sont soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="11b81-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="11b81-124">Fournisseurs doivent vérifier tous les paramètres passés par les applications clientes, mais les clients doivent supposer que MAPI et le fournisseur de paramètres sont corrects.</span><span class="sxs-lookup"><span data-stu-id="11b81-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="11b81-125">Utilisez la macro **HR_FAILED** pour tester les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="11b81-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="11b81-126">**ValidateParms** est appelé différemment selon que le code appelant est C ou C++.</span><span class="sxs-lookup"><span data-stu-id="11b81-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="11b81-127">C++ transmet un paramètre implicite appelé _cette_ à chaque appel de méthode, qui est explicite dans C et l’adresse de l’objet.</span><span class="sxs-lookup"><span data-stu-id="11b81-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="11b81-128">Le premier paramètre, _eMethod_, est un énumérateur à partir de l’interface et la méthode en cours de validation et indique quels paramètres s’attendent à trouver sur la pile.</span><span class="sxs-lookup"><span data-stu-id="11b81-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="11b81-129">Le deuxième paramètre est différent de C et C++.</span><span class="sxs-lookup"><span data-stu-id="11b81-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="11b81-130">En C++, elle est appelée _premier_, et il est le premier paramètre à la méthode en cours de validation.</span><span class="sxs-lookup"><span data-stu-id="11b81-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="11b81-131">Le deuxième paramètre de la langue C, _ppThis_, est l’adresse du premier paramètre à la méthode qui est toujours un pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="11b81-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="11b81-132">Dans les deux cas, le deuxième paramètre donne l’adresse de début de la liste des paramètres de la méthode et en fonction de _eMethod_, déplace vers le bas de la pile et valide les paramètres.</span><span class="sxs-lookup"><span data-stu-id="11b81-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="11b81-133">Fournisseurs d’implémentation des interfaces courants tels que **IMAPITable** et **IMAPIProp** doivent toujours vérifier les paramètres à l’aide de la fonction **ValidateParms** afin d’assurer cohérence entre tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="11b81-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="11b81-134">Fonctions de validation de paramètre supplémentaire ont été définies pour certains types de paramètre complexe à la place, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="11b81-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="11b81-135">Consultez les rubriques de référence pour les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="11b81-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="11b81-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="11b81-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="11b81-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="11b81-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="11b81-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="11b81-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="11b81-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="11b81-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="11b81-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="11b81-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="11b81-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="11b81-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="11b81-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="11b81-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="11b81-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="11b81-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="11b81-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="11b81-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="11b81-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="11b81-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="11b81-146">Méthodes héritées utilisent la validation de la même paramètre que l’interface à partir de laquelle ils héritent.</span><span class="sxs-lookup"><span data-stu-id="11b81-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="11b81-147">Par exemple, la vérification des paramètres des **IMessage** et **IMAPIProp** doivent être la même.</span><span class="sxs-lookup"><span data-stu-id="11b81-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11b81-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11b81-148">See also</span></span>



[<span data-ttu-id="11b81-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="11b81-149">UlValidateParms</span></span>](ulvalidateparms.md)

