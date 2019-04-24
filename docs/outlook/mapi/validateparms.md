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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329574"
---
# <a name="validateparms"></a><span data-ttu-id="38265-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="38265-103">ValidateParms</span></span>

  
  
<span data-ttu-id="38265-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38265-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38265-105">Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmises aux fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="38265-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38265-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="38265-106">Header file:</span></span>  <br/> |<span data-ttu-id="38265-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="38265-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="38265-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="38265-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="38265-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38265-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38265-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="38265-110">Called by:</span></span>  <br/> |<span data-ttu-id="38265-111">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="38265-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="38265-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38265-112">Parameters</span></span>

 <span data-ttu-id="38265-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="38265-113">_eMethod_</span></span>
  
> <span data-ttu-id="38265-114">dans Spécifie, par énumération, la méthode à valider.</span><span class="sxs-lookup"><span data-stu-id="38265-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="38265-115">_First_</span><span class="sxs-lookup"><span data-stu-id="38265-115">_First_</span></span>
  
> <span data-ttu-id="38265-116">dans Pointeur vers le premier argument de la pile.</span><span class="sxs-lookup"><span data-stu-id="38265-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38265-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38265-117">Return value</span></span>

<span data-ttu-id="38265-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="38265-118">S_OK</span></span> 
  
> <span data-ttu-id="38265-119">Tous les paramètres sont valides.</span><span class="sxs-lookup"><span data-stu-id="38265-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="38265-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="38265-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="38265-121">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="38265-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38265-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="38265-122">Remarks</span></span>

<span data-ttu-id="38265-123">Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés être corrects et soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="38265-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="38265-124">Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et de fournisseur sont corrects.</span><span class="sxs-lookup"><span data-stu-id="38265-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="38265-125">Utilisez la macro **HR_FAILED** pour tester les valeurs renvoyées.</span><span class="sxs-lookup"><span data-stu-id="38265-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="38265-126">**ValidateParms** est appelé différemment selon que le code appelant est C ou C++.</span><span class="sxs-lookup"><span data-stu-id="38265-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="38265-127">C++ transmet un paramètre implicite appelé _This_ à chaque appel de méthode, qui devient explicite dans C et est l'adresse de l'objet.</span><span class="sxs-lookup"><span data-stu-id="38265-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="38265-128">Le premier paramètre, _eMethod_, est un énumérateur créé à partir de l'interface et de la méthode en cours de validation et indique les paramètres à rechercher dans la pile.</span><span class="sxs-lookup"><span data-stu-id="38265-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="38265-129">Le deuxième paramètre est différent pour C et C++.</span><span class="sxs-lookup"><span data-stu-id="38265-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="38265-130">En C++, il est appelé en _premier_, et il s'agit du premier paramètre de la méthode en cours de validation.</span><span class="sxs-lookup"><span data-stu-id="38265-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="38265-131">Le deuxième paramètre de la langue C, _ppThis_, est l'adresse du premier paramètre de la méthode qui est toujours un pointeur d'objet.</span><span class="sxs-lookup"><span data-stu-id="38265-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="38265-132">Dans les deux cas, le deuxième paramètre indique l'adresse du début de la liste des paramètres de la méthode et s'appuie sur _eMethod_, se déplace vers le bas de la pile et valide les paramètres.</span><span class="sxs-lookup"><span data-stu-id="38265-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="38265-133">Les fournisseurs qui implémentent des interfaces communes, telles que **IMAPITable** et **IMAPIProp** , doivent toujours vérifier les paramètres à l'aide de la fonction **ValidateParms** afin de s'assurer de la cohérence entre tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="38265-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="38265-134">Des fonctions de validation de paramètres supplémentaires ont été définies pour certains types de paramètres complexes à utiliser à la place, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="38265-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="38265-135">Consultez les rubriques de référence pour les fonctions suivantes:</span><span class="sxs-lookup"><span data-stu-id="38265-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="38265-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="38265-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="38265-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="38265-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="38265-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="38265-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="38265-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="38265-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="38265-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="38265-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="38265-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="38265-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="38265-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="38265-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="38265-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="38265-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="38265-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="38265-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="38265-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="38265-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="38265-146">Les méthodes héritées utilisent la même validation de paramètre que l'interface dont elles héritent.</span><span class="sxs-lookup"><span data-stu-id="38265-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="38265-147">Par exemple, le contrôle de paramètre pour **IMessage** et **IMAPIProp** doit être le même.</span><span class="sxs-lookup"><span data-stu-id="38265-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38265-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38265-148">See also</span></span>



[<span data-ttu-id="38265-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="38265-149">UlValidateParms</span></span>](ulvalidateparms.md)

