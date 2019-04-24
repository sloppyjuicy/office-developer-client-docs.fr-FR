---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2c83f7788d9c01ab02f1a2bc39a35abe2c5a21c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342146"
---
# <a name="imapiformfactorygetlasterror"></a><span data-ttu-id="3cdf6-103">IMAPIFormFactory::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3cdf6-103">IMAPIFormFactory::GetLastError</span></span>

  
  
<span data-ttu-id="3cdf6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cdf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cdf6-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet Factory de formulaire.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="3cdf6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cdf6-106">Parameters</span></span>

 <span data-ttu-id="3cdf6-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="3cdf6-107">_hResult_</span></span>
  
> <span data-ttu-id="3cdf6-108">dans Un type de données HRESULT qui contient la valeur d'erreur générée lors de l'appel de la méthode précédente.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="3cdf6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3cdf6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3cdf6-110">dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="3cdf6-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="3cdf6-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="3cdf6-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3cdf6-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3cdf6-113">Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="3cdf6-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="3cdf6-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="3cdf6-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="3cdf6-116">remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="3cdf6-117">Ce paramètre peut être défini sur NULL s'il n'existe aucune structure **MAPIERROR** à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3cdf6-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3cdf6-118">Return value</span></span>

<span data-ttu-id="3cdf6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3cdf6-119">S_OK</span></span> 
  
> <span data-ttu-id="3cdf6-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3cdf6-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3cdf6-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3cdf6-122">L'indicateur MAPI_UNICODE a été défini et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n'était pas défini et **GetLastError** prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3cdf6-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="3cdf6-123">Remarks</span></span>

<span data-ttu-id="3cdf6-124">La méthode **IMAPIFormFactory:: GetLastError** fournit des informations sur un appel de méthode précédent qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-124">The **IMAPIFormFactory::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="3cdf6-125">Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3cdf6-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="3cdf6-126">Notes to callers</span></span>

<span data-ttu-id="3cdf6-127">Vous pouvez utiliser la structure **MAPIERROR** vers laquelle pointe le paramètre _lppMAPIError_ si MAPI en fournit un uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="3cdf6-128">Parfois, MAPI ne peut pas déterminer quelle est la dernière erreur ou n'a rien d'autre pour signaler l'erreur.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="3cdf6-129">Dans ce cas, un pointeur vers une valeur NULL est renvoyé dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="3cdf6-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="3cdf6-130">Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [utilisation d'erreurs étendues](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="3cdf6-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3cdf6-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cdf6-131">See also</span></span>



[<span data-ttu-id="3cdf6-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3cdf6-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="3cdf6-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3cdf6-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3cdf6-134">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3cdf6-134">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

