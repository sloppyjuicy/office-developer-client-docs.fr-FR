---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438546"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="dd625-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dd625-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="dd625-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd625-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd625-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur de l'objet de prise en charge précédent.</span><span class="sxs-lookup"><span data-stu-id="dd625-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="dd625-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd625-106">Parameters</span></span>

 <span data-ttu-id="dd625-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="dd625-107">_hResult_</span></span>
  
> <span data-ttu-id="dd625-108">dans Handle de la valeur d'erreur générée dans l'appel de méthode précédent pour l'objet support.</span><span class="sxs-lookup"><span data-stu-id="dd625-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="dd625-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd625-109">_ulFlags_</span></span>
  
> <span data-ttu-id="dd625-110">dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="dd625-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="dd625-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="dd625-111">The following flag can be set:</span></span>
    
<span data-ttu-id="dd625-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd625-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dd625-113">Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd625-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="dd625-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="dd625-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="dd625-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="dd625-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="dd625-116">remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="dd625-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="dd625-117">Le paramètre _lppMAPIError_ peut être défini sur null si une structure **MAPIERROR** avec des informations d'erreur appropriées ne peut pas être fournie.</span><span class="sxs-lookup"><span data-stu-id="dd625-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dd625-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd625-118">Return value</span></span>

<span data-ttu-id="dd625-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd625-119">S_OK</span></span> 
  
> <span data-ttu-id="dd625-120">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="dd625-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="dd625-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="dd625-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dd625-122">L'indicateur MAPI_UNICODE a été défini et MAPI ne prend pas en charge Unicode, ou MAPI_UNICODE n'est pas défini et MAPI ne prend en charge que l'Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd625-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd625-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd625-123">Remarks</span></span>

<span data-ttu-id="dd625-124">La méthode **IMAPISupport:: GetLastError** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dd625-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="dd625-125">Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dd625-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dd625-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="dd625-126">Notes to callers</span></span>

<span data-ttu-id="dd625-127">Vous pouvez utiliser le pointeur vers la structure **MAPIERROR** , si MAPI en fournit un, uniquement dans le paramètre _lppMAPIError_ si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="dd625-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="dd625-128">Parfois, MAPI ne peut pas déterminer la dernière erreur ou il n'a rien de plus à signaler à propos de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="dd625-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="dd625-129">Dans ce cas, _lppMAPIError_ renvoie un pointeur vers null à la place.</span><span class="sxs-lookup"><span data-stu-id="dd625-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="dd625-130">Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="dd625-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="dd625-131">Pour libérer toute la mémoire allouée par MAPI, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour la structure **MAPIERROR** renvoyée.</span><span class="sxs-lookup"><span data-stu-id="dd625-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd625-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd625-132">See also</span></span>



[<span data-ttu-id="dd625-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="dd625-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="dd625-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dd625-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dd625-135">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd625-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="dd625-136">Erreurs étendues MAPI</span><span class="sxs-lookup"><span data-stu-id="dd625-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

