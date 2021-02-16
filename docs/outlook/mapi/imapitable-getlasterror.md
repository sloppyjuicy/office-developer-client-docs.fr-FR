---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419001"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="dacfb-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dacfb-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="dacfb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dacfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dacfb-105">Renvoie une [structure MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente sur le tableau.</span><span class="sxs-lookup"><span data-stu-id="dacfb-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="dacfb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dacfb-106">Parameters</span></span>

 <span data-ttu-id="dacfb-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="dacfb-107">_hResult_</span></span>
  
> <span data-ttu-id="dacfb-108">[in] HRESULT contenant l’erreur générée dans l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="dacfb-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="dacfb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dacfb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="dacfb-110">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="dacfb-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="dacfb-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="dacfb-111">The following flag can be set:</span></span>
    
<span data-ttu-id="dacfb-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dacfb-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dacfb-113">Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre  _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="dacfb-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="dacfb-114">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="dacfb-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="dacfb-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="dacfb-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="dacfb-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR renvoyée** contenant les informations de version, de composant et de contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dacfb-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="dacfb-117">Le  _paramètre lppMAPIError_ peut être définie sur NULL si une structure **MAPIERROR** avec les informations appropriées ne peut pas être fournie.</span><span class="sxs-lookup"><span data-stu-id="dacfb-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dacfb-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dacfb-118">Return value</span></span>

<span data-ttu-id="dacfb-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dacfb-119">S_OK</span></span> 
  
> <span data-ttu-id="dacfb-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="dacfb-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="dacfb-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="dacfb-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dacfb-122">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="dacfb-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dacfb-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="dacfb-123">Remarks</span></span>

<span data-ttu-id="dacfb-124">La **méthode IMAPITable::GetLastError** renvoie des informations détaillées, si elles sont disponibles, sur un appel de méthode antérieur qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="dacfb-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="dacfb-125">Ces informations peuvent être affichées dans un message ou une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dacfb-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dacfb-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="dacfb-126">Notes to callers</span></span>

<span data-ttu-id="dacfb-127">Appelez **GetLastError chaque** fois que vous avez besoin d’afficher des informations sur une erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dacfb-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="dacfb-128">Vous pouvez utiliser la structure [MAPIERROR](mapierror.md) pointée par le paramètre  _lppMAPIError_ si l’objet table en fournit un uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="dacfb-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="dacfb-129">Parfois, l’implémentation de la table ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler à propos de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dacfb-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="dacfb-130">Dans ce cas, le pointeur de  _lppMAPIError_ est définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="dacfb-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="dacfb-131">Pour libérer toute la mémoire allouée à la structure **MAPIERROR,** appelez la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="dacfb-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="dacfb-132">Pour plus d’informations **sur la méthode GetLastError,** voir [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="dacfb-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dacfb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dacfb-133">See also</span></span>



[<span data-ttu-id="dacfb-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="dacfb-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="dacfb-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dacfb-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dacfb-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dacfb-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

