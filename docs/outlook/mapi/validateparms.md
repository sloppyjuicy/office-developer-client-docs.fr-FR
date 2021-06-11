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
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436802"
---
# <a name="validateparms"></a><span data-ttu-id="c7a14-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="c7a14-103">ValidateParms</span></span>

  
  
<span data-ttu-id="c7a14-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7a14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7a14-105">Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmis aux fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="c7a14-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7a14-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c7a14-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7a14-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c7a14-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c7a14-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c7a14-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c7a14-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c7a14-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c7a14-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c7a14-110">Called by:</span></span>  <br/> |<span data-ttu-id="c7a14-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="c7a14-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="c7a14-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7a14-112">Parameters</span></span>

 <span data-ttu-id="c7a14-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="c7a14-113">_eMethod_</span></span>
  
> <span data-ttu-id="c7a14-114">[in] Spécifie, par l’éumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="c7a14-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="c7a14-115">_First_</span><span class="sxs-lookup"><span data-stu-id="c7a14-115">_First_</span></span>
  
> <span data-ttu-id="c7a14-116">[in] Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="c7a14-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7a14-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7a14-117">Return value</span></span>

<span data-ttu-id="c7a14-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7a14-118">S_OK</span></span> 
  
> <span data-ttu-id="c7a14-119">Tous les paramètres sont valides.</span><span class="sxs-lookup"><span data-stu-id="c7a14-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="c7a14-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c7a14-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="c7a14-121">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="c7a14-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7a14-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7a14-122">Remarks</span></span>

<span data-ttu-id="c7a14-123">Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés corrects et ne subissent une validation de débogage qu’avec la macro [CheckParms.](checkparms.md)</span><span class="sxs-lookup"><span data-stu-id="c7a14-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="c7a14-124">Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et fournisseur sont corrects.</span><span class="sxs-lookup"><span data-stu-id="c7a14-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="c7a14-125">Utilisez la macro **HR_FAILED** pour tester les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="c7a14-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="c7a14-126">**ValidateParms est** appelé différemment selon que le code appelant est C ou C++.</span><span class="sxs-lookup"><span data-stu-id="c7a14-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="c7a14-127">C++ transmet un paramètre implicite appelé « this  _»_ à chaque appel de méthode, qui devient explicite en C et qui est l’adresse de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c7a14-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="c7a14-128">Le premier paramètre,  _eMethod,_ est un éumérateur effectué à partir de l’interface et de la méthode en cours de validation et indique les paramètres à rechercher sur la pile.</span><span class="sxs-lookup"><span data-stu-id="c7a14-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="c7a14-129">Le deuxième paramètre est différent pour C et C++.</span><span class="sxs-lookup"><span data-stu-id="c7a14-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="c7a14-130">En C++, il s’agit du premier paramètre de la méthode en cours de validation.</span><span class="sxs-lookup"><span data-stu-id="c7a14-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="c7a14-131">Le deuxième paramètre du langage C,  _ppThis_, est l’adresse du premier paramètre de la méthode qui est toujours un pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="c7a14-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="c7a14-132">Dans les deux cas, le deuxième paramètre donne l’adresse du début de la liste des paramètres de la méthode et, en fonction de  _eMethod,_ descend la pile et valide les paramètres.</span><span class="sxs-lookup"><span data-stu-id="c7a14-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="c7a14-133">Les fournisseurs implémentant des interfaces courantes telles que **IMAPITable** et **IMAPIProp** doivent toujours vérifier les paramètres à l’aide de la fonction **ValidateParms** afin de s’assurer de la cohérence entre tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="c7a14-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="c7a14-134">Des fonctions de validation de paramètre supplémentaires ont été définies pour certains types de paramètres complexes à utiliser à la place.</span><span class="sxs-lookup"><span data-stu-id="c7a14-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="c7a14-135">Consultez les rubriques de référence pour les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7a14-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="c7a14-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="c7a14-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="c7a14-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="c7a14-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="c7a14-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="c7a14-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="c7a14-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="c7a14-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="c7a14-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="c7a14-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="c7a14-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="c7a14-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="c7a14-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="c7a14-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="c7a14-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="c7a14-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="c7a14-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="c7a14-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="c7a14-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c7a14-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="c7a14-146">Les méthodes héritées utilisent la même validation de paramètre que l’interface à partir de laquelle elles héritent.</span><span class="sxs-lookup"><span data-stu-id="c7a14-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="c7a14-147">Par exemple, la vérification des **paramètres IMessage** et **IMAPIProp** doit être la même.</span><span class="sxs-lookup"><span data-stu-id="c7a14-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7a14-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7a14-148">See also</span></span>



[<span data-ttu-id="c7a14-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="c7a14-149">UlValidateParms</span></span>](ulvalidateparms.md)

