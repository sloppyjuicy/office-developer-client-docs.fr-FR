---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435830"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="b0066-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b0066-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="b0066-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0066-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0066-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente.</span><span class="sxs-lookup"><span data-stu-id="b0066-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b0066-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b0066-106">Parameters</span></span>

 <span data-ttu-id="b0066-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b0066-107">_hResult_</span></span>
  
> <span data-ttu-id="b0066-108">[in] Handle vers le code d’erreur généré dans l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="b0066-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="b0066-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0066-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b0066-110">[in] Masque de bits d’indicateurs qui indique le format du texte renvoyé dans la structure **MAPIERROR** pointée par  _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="b0066-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="b0066-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="b0066-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b0066-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b0066-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b0066-113">Les chaînes doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="b0066-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="b0066-114">Si l’MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="b0066-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="b0066-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b0066-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b0066-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b0066-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b0066-117">Le  _paramètre lppMAPIError_ peut être définie sur NULL s’il n’existe aucune information d’erreur à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="b0066-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b0066-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0066-118">Return value</span></span>

<span data-ttu-id="b0066-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0066-119">S_OK</span></span> 
  
> <span data-ttu-id="b0066-120">Les informations d’erreur ont été renvoyées.</span><span class="sxs-lookup"><span data-stu-id="b0066-120">The error information was returned.</span></span>
    
<span data-ttu-id="b0066-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b0066-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b0066-122">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="b0066-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0066-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0066-123">Remarks</span></span>

<span data-ttu-id="b0066-124">La **méthode IMAPIProp::GetLastError** fournit des informations sur un appel de méthode antérieur qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="b0066-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="b0066-125">Les clients peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b0066-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="b0066-126">Toutes les implémentations de **GetLastError** fournies par MAPI sont des implémentations ANSI, à l’exception de l’implémentation [IAddrBook.](iaddrbookimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="b0066-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="b0066-127">La **méthode GetLastError incluse** dans **IAddrBook** prend en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="b0066-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b0066-128">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b0066-128">Notes to implementers</span></span>

<span data-ttu-id="b0066-129">Les détails de l’implémentation de cette méthode par un fournisseur de transport distant et les messages qu’elle renvoie sont dus au fournisseur de transport, car les conditions d’erreur particulières qui entraînent diverses valeurs HRESULT seront différentes pour différents fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="b0066-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b0066-130">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="b0066-130">Notes to callers</span></span>

<span data-ttu-id="b0066-131">Vous pouvez utiliser la structure **MAPIERROR** pointée par le paramètre  _lppMAPIError,_ si **GetLastError** en fournit un, uniquement si la valeur de retour est S_OK.</span><span class="sxs-lookup"><span data-stu-id="b0066-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="b0066-132">Parfois, **GetLastError ne** peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler à propos de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b0066-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="b0066-133">Dans ce cas, un pointeur vers NULL est renvoyé dans  _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="b0066-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="b0066-134">Pour libérer la mémoire de la structure **MAPIERROR,** appelez la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="b0066-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b0066-135">Pour plus d’informations **sur la méthode GetLastError,** voir [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b0066-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0066-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0066-136">See also</span></span>



[<span data-ttu-id="b0066-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b0066-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="b0066-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b0066-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b0066-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b0066-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b0066-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0066-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="b0066-141">Erreurs étendues MAPI</span><span class="sxs-lookup"><span data-stu-id="b0066-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

