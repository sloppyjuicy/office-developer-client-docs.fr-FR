---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439848"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="a3f22-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a3f22-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="a3f22-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3f22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3f22-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet d'administration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a3f22-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="a3f22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3f22-106">Parameters</span></span>

 <span data-ttu-id="a3f22-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a3f22-107">_hResult_</span></span>
  
> <span data-ttu-id="a3f22-108">dans Un type de données HRESULT qui contient la valeur d'erreur générée lors de l'appel de la méthode précédente.</span><span class="sxs-lookup"><span data-stu-id="a3f22-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="a3f22-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3f22-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a3f22-110">dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="a3f22-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="a3f22-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="a3f22-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a3f22-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a3f22-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a3f22-113">Les chaînes dans le **MAPIERROR** renvoyé dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="a3f22-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="a3f22-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="a3f22-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a3f22-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a3f22-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a3f22-116">remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="a3f22-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="a3f22-117">Le paramètre _lppMAPIError_ peut être défini sur null s'il n'y a pas de **MAPIERROR** à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="a3f22-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3f22-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a3f22-118">Return value</span></span>

<span data-ttu-id="a3f22-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3f22-119">S_OK</span></span> 
  
> <span data-ttu-id="a3f22-120">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="a3f22-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="a3f22-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a3f22-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a3f22-122">L'indicateur MAPI_UNICODE a été défini et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n'était pas défini et **GetLastError** prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="a3f22-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a3f22-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3f22-123">Remarks</span></span>

<span data-ttu-id="a3f22-124">La méthode **IProviderAdmin:: GetLastError** fournit des informations sur un appel de méthode précédent qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="a3f22-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="a3f22-125">Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a3f22-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3f22-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="a3f22-126">Notes to callers</span></span>

<span data-ttu-id="a3f22-127">Vous pouvez utiliser la structure **MAPIERROR** , si MAPI en fournit un, que le paramètre _LppMAPIError_ uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="a3f22-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="a3f22-128">Parfois, MAPI ne peut pas déterminer quelle est la dernière erreur ou n'a rien d'autre pour signaler l'erreur.</span><span class="sxs-lookup"><span data-stu-id="a3f22-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="a3f22-129">Dans ce cas, un pointeur vers une valeur NULL est renvoyé dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="a3f22-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="a3f22-130">Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [utilisation d'erreurs étendues](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="a3f22-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3f22-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f22-131">See also</span></span>



[<span data-ttu-id="a3f22-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a3f22-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a3f22-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a3f22-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a3f22-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3f22-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

