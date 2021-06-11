---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430772"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="2436f-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2436f-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="2436f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2436f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2436f-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur un objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="2436f-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="2436f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2436f-106">Parameters</span></span>

 <span data-ttu-id="2436f-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="2436f-107">_hResult_</span></span>
  
> <span data-ttu-id="2436f-108">[in] Type de données HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="2436f-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="2436f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2436f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2436f-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="2436f-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="2436f-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="2436f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2436f-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2436f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2436f-113">Les chaînes de la structure [MAPIERROR renvoyées](mapierror.md) dans le paramètre  _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="2436f-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="2436f-114">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="2436f-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="2436f-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2436f-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="2436f-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2436f-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="2436f-117">Le  _paramètre lppMAPIError_ peut avoir la valeur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="2436f-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2436f-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2436f-118">Return value</span></span>

<span data-ttu-id="2436f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2436f-119">S_OK</span></span> 
  
> <span data-ttu-id="2436f-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="2436f-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2436f-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2436f-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2436f-122">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="2436f-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2436f-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="2436f-123">Remarks</span></span>

<span data-ttu-id="2436f-124">La **méthode IProfAdmin::GetLastError** récupère des informations sur la dernière erreur renvoyée par un appel de méthode pour l’objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="2436f-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2436f-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="2436f-125">Notes to callers</span></span>

<span data-ttu-id="2436f-126">Vous pouvez utiliser la structure **MAPIERROR,** si MAPI en fournit un, pointée par le paramètre  _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="2436f-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="2436f-127">Parfois, MAPI ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2436f-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="2436f-128">Dans ce cas, un pointeur vers NULL est renvoyé dans  _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="2436f-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="2436f-129">Pour libérer toute la mémoire allouée par MAPI pour la structure **MAPIERROR,** appelez la [fonction MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="2436f-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="2436f-130">Pour plus d’informations sur **la méthode GetLastError,** voir [Using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="2436f-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2436f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2436f-131">See also</span></span>



[<span data-ttu-id="2436f-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2436f-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2436f-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2436f-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2436f-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2436f-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

