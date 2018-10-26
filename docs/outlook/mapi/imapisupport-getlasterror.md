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
ms.openlocfilehash: 3e641842dd8264c0cd3556c498bd74c77bda32f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577505"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="812da-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="812da-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="812da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="812da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="812da-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur d’objet prise en charge précédente.</span><span class="sxs-lookup"><span data-stu-id="812da-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="812da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="812da-106">Parameters</span></span>

 <span data-ttu-id="812da-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="812da-107">_hResult_</span></span>
  
> <span data-ttu-id="812da-108">[in] Handle vers la valeur d’erreur généré dans l’appel de méthode précédent pour l’objet de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="812da-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="812da-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="812da-109">_ulFlags_</span></span>
  
> <span data-ttu-id="812da-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="812da-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="812da-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="812da-111">The following flag can be set:</span></span>
    
<span data-ttu-id="812da-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="812da-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="812da-113">Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="812da-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="812da-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="812da-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="812da-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="812da-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="812da-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="812da-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="812da-117">Le paramètre _lppMAPIError_ peut être défini sur NULL si une structure **MAPIERROR** avec des informations d’erreur approprié ne peut pas être fournie.</span><span class="sxs-lookup"><span data-stu-id="812da-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="812da-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="812da-118">Return value</span></span>

<span data-ttu-id="812da-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="812da-119">S_OK</span></span> 
  
> <span data-ttu-id="812da-120">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="812da-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="812da-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="812da-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="812da-122">Soit l’indicateur MAPI_UNICODE a été défini et MAPI ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et prend en charge MAPI uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="812da-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="812da-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="812da-123">Remarks</span></span>

<span data-ttu-id="812da-124">La méthode **IMAPISupport::GetLastError** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="812da-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="812da-125">Les appelants peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="812da-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="812da-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="812da-126">Notes to callers</span></span>

<span data-ttu-id="812da-127">Vous pouvez utiliser le pointeur vers la structure **MAPIERROR** , si MAPI fournit un, dans le paramètre _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="812da-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="812da-128">Parfois MAPI ne peut pas déterminer quelle était la dernière erreur, ou il a rien de plus à un rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="812da-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="812da-129">Dans ce cas, _lppMAPIError_ retourne un pointeur vers la valeur NULL à la place.</span><span class="sxs-lookup"><span data-stu-id="812da-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="812da-130">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="812da-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="812da-131">Pour libérer la mémoire allouée par MAPI, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour la structure **MAPIERROR** retournée.</span><span class="sxs-lookup"><span data-stu-id="812da-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="812da-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="812da-132">See also</span></span>



[<span data-ttu-id="812da-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="812da-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="812da-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="812da-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="812da-135">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="812da-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="812da-136">MAPI �tendue des erreurs</span><span class="sxs-lookup"><span data-stu-id="812da-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

